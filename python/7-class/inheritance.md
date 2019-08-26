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

* 繼承可以是間接的

輸入:

	class A:
		def method_a(self):
			print("A method")

	class B(A):
		def method_b(self):
			print("B method")

	class C(B):
		def method_c(self):
			print("C method")

	c = C()
	c.method_a()
	c.method_b()
	c.method_c()

輸出:

	A method
	B method
	C method

# 函數super()

* 在子類別中使用和父類別相同識別字命名屬性時,會以子類別為優先

輸入:

	class A:
		color = 'black'
		def show(self):
			print('class A')

	class B(A):
		color = 'yellow'
		def show(self):
			print('class B')

	banana = B()
	print(banana.color)
	banana.show()

輸出:

	yellow
	class B

* 使用super()可調用父類別的屬性,一般語法為super(**類別名**[, 實體名])

輸入:

	class A:
		color = 'black'
		def show(self):
			print('class A')

	class B(A):
		color = 'yellow'
		def show(self):
			print('class B')

	banana = B()
	print(super(B, banana).color)
	super(B, banana).show()

輸出:

	black
	class A

* 在建立**方法**時,可直接使用super()調用父類別的方法

輸入:

	class A:
		def show(self, x):
			y = x + 2
			print(y)

	class B(A):
		def show(self, z):
			super().show(z)

	banana = B()
	banana.show(1)

輸出:

	3
