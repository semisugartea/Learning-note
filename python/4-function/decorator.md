# 裝飾器 decorator

	裝飾器是定義函數或方法的一種簡化語法，主要是讓新定義的函數，可以有效減少繁複的用函數當參數，或是函數回傳函數的寫法。

以下為例,主程序上用rose代稱f1(f2),而函數f1的作用是傳入函數f2再傳出函數flower,f2變成f1的參數

	def f1(func):
		def flower(color2):
			print('flower')
			return 'color:'+func(color2)				#3	參數func是由f1傳入的f2,參數color2則是引數arg
		return flower								#2	f1(func))(arg)變成flower(arg), 但實際上flower需要傳入函數

	def f2(color1):
		return color1

	rose = f1(f2)
	print(rose('red'))							#1	等價於print((f1(f2))('red'))
	
若在f2前加上裝飾器,即@函數名,則f2的功能就會跟f1(f2)一樣,也就是將f2擴充成不使用裝飾器的f1(f2),由def f2()的內容做為函數傳入f1(),省略將f2設為f1的參數的步驟
	
	def f1(func):
	def flower(color2):
		print('flower')
		return 'color:'+func(color2)
	return flower

	@f1
	def f2(color1):
		return color1

	print(f2('red'))

裝飾器可以不只一個,依順序由外而內,被@的函數必須在裝飾器前,下例的f2的功能就會跟不使用裝飾器的f3(f1(f2))一樣

	def f1(func):
		def flower(color2):
			print('flower')
			return 'color:'+func(color2)
		return flower

	def f3(func):
		def description(color3):
			return 'description:'+func(color3)
		return description

	@f3
	@f1
	def f2(color1):
		return color1

	print(f2('red'))