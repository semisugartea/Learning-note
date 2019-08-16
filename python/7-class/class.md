# �򥻤���

	���O(class)�O�W������(object)���ŹϡA�Z�O�����ݩ�(attribute)�Τ�k (method) ���n�b���O���w�q�A�y�k�p�U:

		class ClassName:
			<statement-1>
			.
			.
			.
			<statement-N>

# ���O���򥻷���

	�������H�U������:
	
��J:	
	
	class fruit:
	  num = 7
	  def f(self):
	   return 'hello'

	apple = fruit()
	print(type(apple))
	print(apple.num)
	print(apple.f())

��X:

	<class '__main__.fruit'>
	7
	hello	
	
1. �b�Ҥl��,�����Q��class�w�q���Ofruit, �A�Q��fruit���O���غc�l(constructor)�إߪ����O����������ܼ�apple, �ҿ׫غc�l�O�����O�W�٥[�W�p�A��
2. ��type()�i�ݥX�ܼ�apple�O__main__�@�ΰ�U��fruit���A
3. ���O�����ܼƥi�������O�ݩ�(class attribute), �i�Q��obj.name���覡�ޥX�ݩʤ��e
4. ���O������ƳQ�٬���k(method), �P�˥i�Q��obj.name���覡�ޥX���, �b�إߤ�k�ɥ������@���B�~���ѼƦW��, �q�`���ϥ�self

# ����self���ϥ�
	
	* �b��k�����Ĥ@�ӰѼ�self�N�����O������

��J:	
		class fruit:
			def show(self):
				print(self)
		 
		a = fruit()
		a.show()	
��X:			
		<__main__.fruit object at 0x00000237A6F459E8>	
	

	* �Ĥ@�ӰѼƦW�i�H�O��L�r

��J:	
		class fruit:
			def show(apple):
				print(apple)
		 
		a = fruit()
		a.show()	
��X:	
		<__main__.fruit object at 0x000001D232EE5E80>	

	* �b���P��k�����Ĥ@�ӰѼƨ�곣���V�P�@����
	
��J:
		class fruit:
			def show(apple):
				print(apple)
			
			def show2(banana):
				print(banana)

		a = fruit()
		a.show()
		a.show2()	
��X: 	
		<__main__.fruit object at 0x0000029EB8045EF0>
		<__main__.fruit object at 0x0000029EB8045EF0>	
	

	
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
	
	
	
	
	
	
	
