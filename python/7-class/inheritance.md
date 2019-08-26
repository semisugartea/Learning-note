# �~��(Inheritance)

* �~�ӥi�H�Ϥ@�����O�ϥΨ�t�@�����O���ݩ�,�H�U����,���Oapple�~�����Ofruit,���ɺ����Oapple��**�l���O**,�����Ofruit��**�����O**

��J:

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

��X:

	home
	red
	cheap

* �~�ӥi�H�O������

��J:

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

��X:

	A method
	B method
	C method

# ���super()

* �b�l���O���ϥΩM�����O�ۦP�ѧO�r�R�W�ݩʮ�,�|�H�l���O���u��

��J:

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

��X:

	yellow
	class B

* �ϥ�super()�i�եΤ����O���ݩ�,�@��y�k��super(**���O�W**[, ����W])

��J:

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

��X:

	black
	class A

* �b�إ�**��k**��,�i�����ϥ�super()�եΤ����O����k

��J:

	class A:
		def show(self, x):
			y = x + 2
			print(y)

	class B(A):
		def show(self, z):
			super().show(z)

	banana = B()
	banana.show(1)

��X:

	3
