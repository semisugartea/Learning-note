# ����(instance)

* �Q�ΦW��__init__()����k�i�H�b���O���إ߹���, ����k�Q�٬��غc�l(constructor)

��J:

	class fruit:
		def __init__(self):
			self.name = 'apple'
			self.color = 'red'
	 
	a = fruit()
	print(a.name)
	print(a.color)

��X:
	
	apple

�b�Ҥl��,�b__init__()���إ��ݩ�name, ���ݩʤS�Q�٬������ݩ�(instance attribute), �P�˥i�Q��obj.name���覡�ޥX�ݩʤ��e

* �]�i�H��__init__()��k���Ѽƨӳ]�w�A���ɴN�n�b�إߪ�����骺�ɭԴ��ѰѼ�(parameter)�A�ӳ]�w���ĤG�ӰѼƤ~�O��J���Ĥ@�ӰѼ�

��J:

	class fruit:
		def __init__(self, name, color):
			self.name = name
			self.color = color
	 
	a = fruit('apple', 'red')
	print(a.name)
	print(a.color)
	
��X:
	
	apple
	red

* �����ݩʥi�H�b��k���ϥ�

��J:

	class fruit:
		def __init__(self, name, color):
			self.name = name
			self.color = color

		def good(self):
			print('Good', self.name)

	a = fruit('apple', 'red')
	a.good()

��X:

	good apple

* �p�P���,�Ѽƪ��ȥi�H�Q�]�w

��J:

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

��X:

	I have 1 apple
	I have 2 apple
	I have 3 apple

