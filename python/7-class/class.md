# 基本介紹

類別(class)是規劃物件(object)的藍圖，凡是物件的屬性(attribute)及方法 (method) 都要在類別中定義，語法如下:

	class ClassName:
		<statement-1>
		.
		.
		.
		<statement-N>

# 類別的基本概念

直接先以下面為例:
	
輸入:	
	
	class fruit:
	  num = 7
	  def f(self):
	   return 'hello'

	apple = fruit()
	print(type(apple))
	print(apple.num)
	print(apple.f())

輸出:

	<class '__main__.fruit'>
	7
	hello	
	
1. 在例子中,首先利用class定義類別fruit, 再利用fruit類別的建構子(constructor)建立的類別物件指派給變數apple, 所謂建構子是用類別名稱加上小括弧
2. 由type()可看出變數apple是__main__作用域下的fruit型態
3. 類別中的變數可視為類別屬性(class attribute), 可利用obj.name的方式引出屬性內容
4. 類別中的函數被稱為方法(method), 同樣可利用obj.name的方式引出函數, 在建立方法時必須有一個額外的參數名稱, 通常都使用self

# 關於self的使用
	
* 在方法中的第一個參數self代表類別的物件

輸入:	

	class fruit:
		def show(self):
			print(self)
		 
	a = fruit()
	a.show()
	
輸出:		

	<__main__.fruit object at 0x00000237A6F459E8>	
	
* 第一個參數名可以是其他字

輸入:	

	class fruit:
		def show(apple):
			print(apple)
		 
	a = fruit()
	a.show()	
	
輸出:	

	<__main__.fruit object at 0x000001D232EE5E80>	

* 在不同方法中的第一個參數其實都指向同一物件
	
輸入:

	class fruit:
		def show(apple):
			print(apple)
			
		def show2(banana):
			print(banana)

	a = fruit()
	a.show()
	a.show2()	
	
輸出: 	

	<__main__.fruit object at 0x0000029EB8045EF0>
	<__main__.fruit object at 0x0000029EB8045EF0>	

	
# 實體(instance)

* 利用名為__init__()的方法可以在類別中建立實體, 此方法被稱為建構子(constructor)

輸入:

	class fruit:
		def __init__(self):
			self.name = 'apple'
			self.color = 'red'
	 
	a = fruit()
	print(a.name)
	print(a.color)

輸出:
	
	apple

在例子中,在__init__()中建立屬性name, 此屬性又被稱為實體屬性(instance attribute), 同樣可利用obj.name的方式引出屬性內容

* 也可以用__init__()方法的參數來設定，此時就要在建立物件實體的時候提供參數(parameter)，而設定的第二個參數才是輸入的第一個參數

輸入:

	class fruit:
		def __init__(self, name, color):
			self.name = name
			self.color = color
	 
	a = fruit('apple', 'red')
	print(a.name)
	print(a.color)
	
輸出:
	
	apple
	red

* 實體屬性可以在方法中使用

輸入:

	class fruit:
		def __init__(self, name, color):
			self.name = name
			self.color = color

		def good(self):
			print('Good', self.name)

	a = fruit('apple', 'red')
	a.good()

輸出:

	good apple

* 如同函數,參數的值可以被設定

輸入:

	class fruit:
		def __init__(self, name, num = 3):
			self.name = name
			self.num = num

		def check(self):
			num = 1
			while num <= self.num:
				print('I have', num, self.name)
				num += 1

	a = fruit('apple')
	a.check()

輸出:

	I have 1 apple
	I have 2 apple
	I have 3 apple

# 屬性的識別字

* 當類別屬性與實體屬性使用相同識別字時,則無法用實體物件存取類別屬性

輸入:

	class fruit:
		x = 0		#類別屬性

		def __init__(self, x):
			self.x = x 	#實體屬性
			fruit.x += 1  	#每當建立一個實體,類別屬性+1

	f1 = fruit(123)
	print(f1.x)
	print(fruit.x)
	f2 = fruit(456)
	print(f2.x)
	print(fruit.x)

輸出:

	123
	1
	456
	2

* 當類別屬性與實體屬性使用不同識別字時,則可用實體物件存取類別屬性

輸入:

	class fruit:
		x = 0 

		def __init__(self, y):
			self.y = y 
			fruit.x += 1

	f1 = fruit(123)
	print(f1.x)
	print(f1.y)
	print(fruit.x)
	f2 = fruit(456)
	print(f2.x)
	print(f2.y)
	print(fruit.x)

輸出:

	1
	123
	1
	2
	456
	2

# 屬性例外(AttributeError)

* 當屬性不存在時,會產生屬性例外

輸入:

	class fruit:
		def __init__(self):
			self.name = 'apple'
			self.color = 'red'

	a = fruit()
	print(a.price)

輸出:

	AttributeError: 'fruit' object has no attribute 'price'

# 繼承(Inheritance)

* 繼承可以使一個類別使用到另一個類別的屬性,以下為例,類別apple繼承類別fruit,此時稱類別apple為**子類別**,而類別fruit為**父類別**

輸入:

	class fruit:
		def __init__(self, name, color):
			self.name = name
			self.color = color

	class apple(fruit):
		def price(self):
			print('cheap')

	home = apple('home', 'red')
	print(home.name)
	print(home.color)
	home.price()

輸出:

	home
	red
	cheap



