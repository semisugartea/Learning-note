# ���ɦr�Ŧ� DocStrings

	�b��Ƥ��i�ϥΤ@��T�Ӥ޸�'''�@����,�i�ϥ�print(*function_name*.__doc__)��ܤ��e

	��J:
	def hello():
		'''hello world
		'''
		print('apple')
	 
	print(hello.__doc__)

	��X:
	hello world
	
# �˹��� decorator

	�˹����O�w�q��ƩΤ�k���@��²�ƻy�k�A�D�n�O���s�w�q����ơA�i�H���Ĵ���c�ƪ��Ψ�Ʒ�ѼơA�άO��Ʀ^�Ǩ�ƪ��g�k�C

�H�U����,�D�{�ǤW��rose�N��f1(f2),�Ө��f1���@�άO�ǤJ���f2�A�ǥX���flower,f2�ܦ�f1���Ѽ�

	def f1(func):
		def flower(color2):
			print('flower')
			return 'color:'+func(color2)				#3	�Ѽ�func�O��f1�ǤJ��f2,�Ѽ�color2�h�O�޼�arg
		return flower								#2	f1(func))(arg)�ܦ�flower(arg), ����ڤWflower�ݭn�ǤJ���

	def f2(color1):
		return color1

	rose = f1(f2)
	print(rose('red'))							#1	������print((f1(f2))('red'))
	
�Y�bf2�e�[�W�˹���,�Y@��ƦW,�hf2���\��N�|��rose�@��,�Ѧ��ٲ��Nf2�]��f1���Ѽƪ��B�J
	
	def f1(func):
	def flower(color2):
		print('flower')
		return 'color:'+func(color2)
	return flower

	@f1
	def f2(color1):
		return color1

	print(f2('red'))
	
# ���;� generator


# ���j recursion




