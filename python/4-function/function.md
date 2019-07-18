# �򥻤���

	���(function)�O�@�ذϰ쫬���N�X,���Q�I�s�ɷ|���椺�e,������|��^�D�{�ǩΦ^�ǭ�,�򥻧Φ���:
	
	def *function_name*(*parameter(s)*):
		statement

1. ���楲���Hdef�}�Y,��������ƦW,�A�̦b()���w�q�Ѽ�,�i�H0�өΦh��,�H�r���Ϲj,�̫�H�_������
2. ���楲���b�}�Y�Y��,�_�h���ǤJ��Ƥ�

# �Ѽ�(parameter)�M�޼�(argument)

* �ѼƬO����Ƥ��ҩw�q���ܼ�,���ܼƦW�q�`�L�k�b��ƥ~���ϰ�ϥ�

	��J:
	def plus(parameter):
	   parameter += 1
	   print(parameter)
	plus(1)
	print(parameter)

	��X:
	Traceback (most recent call last):
	  File "python.py", line 5, in <module>
		print(parameter)
	NameError: name 'parameter' is not defined

* �޼ƬO���~���ǤJ��Ʒ�@�Ѽƪ���,��Q�ޤJ���ܼƬO�i�ܪ�(mutable)��,��ȥi��|����

��1:
	��J:
	def plus(parameter):
	   parameter += 1
	a = 1
	plus(a)
	print(a)

	��X:
	1
��2:
	��J:
	def plus(parameter):
	   parameter.append(1)
	a = []
	plus(a)
	print(a)

	��X:
	[1]

# �ѼƩM�޼ƪ����A

* ���ݰѼ� required parameter

	�b�]�w��Ʈɥi�ۭq�Ѽ�,�b�I�s��Ʈ�,�Ѽƥ��ݦ���������,�_�h�|����,�]���٬����ݰѼ�

	��J:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1)

	��X:
	Traceback (most recent call last):
	  File "python.py", line 5, in <module>
		printwords(1)
	TypeError: printwords() missing 1 required positional argument: 'b'


* ����r�޼� keyword argument

	�b�D�{�Ǥ��I�s��Ʈ�,�Y�Q�ΰѼƦW�]�w�޼ƭ�,�h�i�٬�����r�޼�,���ɤ޼ƭȥH�W�٬��D,�ӫD����

	��J:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1, 2)
	printwords(b=4, a=3)

	��X:
	a: 1
	b: 2
	a: 3
	b: 4

* �q�{�Ѽ� default parameter

	�b�]�w�ѼƮɥi�H�]�w�q�{��,�٬��q�{�Ѽ�,���ƳQ�I�s��,�Y�S���޼�,�h�ϥ��q�{�Ѽ�

	��J:	
	def plus(a=2, b=2):
		print("a+b:", a+b)

	plus()
	plus(a=3)
	plus(3,3)

	��X:
	a+b: 4
	a+b: 5
	a+b: 6

* ���w�ƶq�Ѽ�

	�Y��J���޼Ƽƶq�i��h��Ѽƪ��ƶq��,�i�b�Ѽƫe�[�@�ӬP��\*,�h�h�󪺤޼Ʒ|�H���ժ��覡�ޤJ
	�Y�b�Ѽƫe�[��ӬP��,�h�h�󪺤޼Ʒ|�H�r�媺�覡�ޤJ
	
	��J:
	def printwords(x, *y, **z):
		print("x:", x)
		print("y:", y)
		print("z:", z)

	printwords(10,20,30,'apple','banana', cat=10, dog='egg')

	��X:
	x: 10
	y: (20, 30, 'apple', 'banana')
	z: {'cat': 10, 'dog': 'egg'}

# �^�ǭ� return

	�b��Ƥ��ϥ�return�i�H������ƨöǥX��,�q�{�Ȭ�None,��None�N��S�����󪫥�

# �¨�� pure function

* �¨�ƬO����Ƥ����Ҧ��ܼƤΰѼƬO�ϰ�ʪ�,����W���v�T�~�����ܼ�

	def pure(x, y):
	  add = x + y
	  return add*x + y

* ���¨��(impure function)�O����ƪ����ޥΥ~�����ܼ�,�ɭP����ɼv�T�~�����ܼ�

	list1 = [1,2]

	def impure(x):
	  some_list.append(x)

* �¨�ƪ��S�I

	1. �e���z�ѻP����
	2. ����W���Ĳv
	3. �P�D�{�ǥ���B��

# ��ƪ����

	�bPython��,��Ƥ@�˥i�H�Q��@����ϥ�

1. ��ƦW�ǻ�
	
	�i�H�N��ƦW�������ܼ�,�Ϩ��ܦ����

	��J:
	def add(a, b):
	return a+b

	plus = add
	print(plus(1,2))
	
	��X:
	3

2. ��@�Ѽ�

	��Ƥ��i�H�N�ѼƦW��@��ƦW,�ϱo����ƥi�ޤJ��L���

	��J:	
	def multiply(x, y):
	  return x*y

	def add(func, x, y):
	  return func(x, y) + func(x, y)

	a = 3
	b = 7
	print(add(multiply, a, b))

	��X:
	42







