# �ݩ�(attribute)

�b���O���������O�ݩʻP�����ݩ�,�H�U�����t��

# �ݩʪ��ѧO�r

* �����O�ݩʻP�����ݩʨϥάۦP�ѧO�r��,�h�L�k�ι��骫��s�����O�ݩ�

��J:

	class fruit:
		x = 0		#���O�ݩ�

		def __init__(self, x):
			self.x = x 	#�����ݩ�
			fruit.x += 1  	#�C��إߤ@�ӹ���,���O�ݩ�+1

	f1 = fruit(123)
	print(f1.x)
	print(fruit.x)
	f2 = fruit(456)
	print(f2.x)
	print(fruit.x)

��X:

	123
	1
	456
	2

* �����O�ݩʻP�����ݩʨϥΤ��P�ѧO�r��,�h�i�ι��骫��s�����O�ݩ�

��J:

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

��X:

	1
	123
	1
	2
	456
	2

# �ݩʨҥ~(AttributeError)

* ���ݩʤ��s�b��,�|�����ݩʨҥ~

��J:

	class fruit:
		def __init__(self):
			self.name = 'apple'
			self.color = 'red'

	a = fruit()
	print(a.price)

��X:

	AttributeError: 'fruit' object has no attribute 'price'