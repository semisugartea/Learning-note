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

# ���j recursion

* ���j�O����ƩI�s�ۤv����ƦW,���ɩI�s�̼Ȱ��õ��ݦ^�ǭ�,����Q�I�s��,�^�Ǧ��Ī��ȫ�A����I�s��,�H�U�Q�ζ�����Ƭ���

	��J:
	def fac(n):
		print(n)
		if n == 1:
			return 1
		else: 
			a = n * fac(n-1)
			print(n)
			return a
		
	print(fac(3))

	��X:
	3
	2
	1
	2
	3
	6

* �Y���]�w���I��,�|�ɭPRuntimeError���ҥ~

	��J:
	def fac(n):
		return n * fac(n-1)

	��X:
	RuntimeError: maximum recursion depth exceeded

* ���j�i�H�O������,�Y��ƩI�s�O����ƦW,�ӸӨ�ƩI�s�ۤv����ƦW



