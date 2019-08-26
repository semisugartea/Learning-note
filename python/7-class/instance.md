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

