# 基本介紹

函數(function)是一種區域型的代碼,當其被呼叫時會執行內容,結束後會返回主程序或回傳值,基本形式為:
	
		def *function_name*(*parameter(s)*):
			statement

1. 首行必須以def開頭,中間為函數名,再者在()內定義參數,可以0個或多個,以逗號區隔,最後以冒號結尾
2. 次行必須在開頭縮排,否則不納入函數中

# 參數(parameter)和引數(argument)

*   參數是指函數內所定義的變數,其變數名通常無法在函數外的區域使用

		輸入:
		def plus(parameter):
		   parameter += 1
		   print(parameter)
		plus(1)
		print(parameter)

		輸出:
		Traceback (most recent call last):
		  File "python.py", line 5, in <module>
			print(parameter)
		NameError: name 'parameter' is not defined

* 引數是指外部傳入函數當作參數的值,當被引入的變數是可變的(mutable)時,其值可能會改變

例1:

	輸入:
	def plus(parameter):
	   parameter += 1
	a = 1
	plus(a)
	print(a)

	輸出:
	1
	
例2:

	輸入:
	def plus(parameter):
	   parameter.append(1)
	a = []
	plus(a)
	print(a)

	輸出:
	[1]

# 參數和引數的型態

* 必需參數 required parameter

 在設定函數時可自訂參數,在呼叫函數時,參數必需有相應的值,否則會報錯,因此稱為必需參數

	輸入:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1)

	輸出:
	Traceback (most recent call last):
	  File "python.py", line 5, in <module>
		printwords(1)
	TypeError: printwords() missing 1 required positional argument: 'b'


* 關鍵字引數 keyword argument

 在主程序中呼叫函數時,若利用參數名設定引數值,則可稱為關鍵字引數,此時引數值以名稱為主,而非順序

	輸入:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1, 2)
	printwords(b=4, a=3)

	輸出:
	a: 1
	b: 2
	a: 3
	b: 4

* 默認參數 default parameter

 在設定參數時可以設定默認值,稱為默認參數,當函數被呼叫時,若沒有引數,則使用默認參數

	輸入:	
	def plus(a=2, b=2):
		print("a+b:", a+b)

	plus()
	plus(a=3)
	plus(3,3)

	輸出:
	a+b: 4
	a+b: 5
	a+b: 6

* 不定數量參數

 若輸入的引數數量可能多於參數的數量時,可在參數前加一個星號\*,則多於的引數會以元組的方式引入
 若在參數前加兩個星號,則多於的引數會以字典的方式引入
	
	輸入:
	def printwords(x, *y, **z):
		print("x:", x)
		print("y:", y)
		print("z:", z)

	printwords(10,20,30,'apple','banana', cat=10, dog='egg')

	輸出:
	x: 10
	y: (20, 30, 'apple', 'banana')
	z: {'cat': 10, 'dog': 'egg'}

# 回傳值 return

在函數中使用return可以結束函數並傳出值,默認值為None,而None代表沒有任何物件

# 純函數 pure function

*   純函數是指函數中的所有變數及參數是區域性的,執行上不影響外面的變數

		def pure(x, y):
		  add = x + y
		  return add*x + y

*   不純函數(impure function)是指函數直接引用外面的變數,導致執行時影響外面的變數

		list1 = [1,2]

		def impure(x):
		  some_list.append(x)

* 純函數的特點

	1. 容易理解與測試
	2. 執行上有效率
	3. 與主程序平行運算

# 函數物件化

在Python中,函數一樣可以被當作物件使用

1. 函數名傳遞
	
 可以將函數名指派給變數,使其變成函數

	輸入:
	def add(a, b):
	return a+b

	plus = add
	print(plus(1,2))
	
	輸出:
	3

2. 當作參數

 函數中可以將參數名當作函數名,使得此函數可引入其他函數

	輸入:	
	def multiply(x, y):
	  return x*y

	def add(func, x, y):
	  return func(x, y) + func(x, y)

	a = 3
	b = 7
	print(add(multiply, a, b))

	輸出:
	42







