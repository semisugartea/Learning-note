# �|�N�� iterator

�|�a(iteration):�Q�ΰj��M����H���������ʧ@
�i�|�a��H(iterable):�i�Q�M����������H
�|�N��(iterator):�i�����|�a���{��

* iter(obj)			�Q�Ϊ���ͦ��|�N��

* next(iterator)	Ū���|�N�����U�@�Ӷ���,��Ū���쪫���,�|����StopIteration���ҥ~

	��J:
	list1=[1,2,3,4]
	a = iter(list1)
	print(next(a))
	print(next(a))
	print(next(a))
	print(next(a))
	print(next(a))

	��X:
	1
	2
	3
	4
	Traceback (most recent call last):
	  File "python.py", line 7, in <module>
		print(next(a))
	StopIteration

# yield

	�b��Ƥ��ϥ�yield��,�i�H���ͤ@�ժ���,�æ^�Ǫ��󪺦�}��Ȱ�,���Ʀb�Q�I�s���~��,�i�H���@�P�D�{�ǥ���B�@,�Ӧ���ƥi�H�ܦ��|�N��
	
* for�j��
	
	�i�Q��for�j��Ū������,���Ƶ����ɰj�鵲��

	��J:
	def count(n):
		i =1
		print('start')
		while i <=n:
			print('hello')
			yield i
			print('world')
			i += 1
		yield 'finish'

	print(count(2))
	for j in count(2):
		print(j)
		print('pause')

	��X:
	<generator object count at 0x00000175C31EB5E8>
	start
	hello
	1
	pause
	world
	hello
	2
	pause
	world
	finish
	pause

* next()

	�i�Q�Ψ��next()���i����Ū������,��Ū���쪫���,�|����StopIteration���ҥ~

	��J:
	def count(n):
		i =1
		while i <=n:
			yield i
			i += 1

	a = count(3)
	print(next(a))
	print(next(a))
	print(next(a))
	print(next(a))

	��X:
	1
	2
	3
	Traceback (most recent call last):
	  File "python.py", line 11, in <module>
		print(next(a))
	StopIteration

* �Preturn���t��

	�b���ͤ@�ӧǦC�W,return�����@���إ߾�ӧǦC,��yield�u�n�@���إߤ@��,�۹�٫ܦh�Ŷ�,�H�U�Q�ζO��ƦC����

return:
	��J:
	def fab(n): 
		count, a, b = 0, 0, 1 
		seq = [] 
		while count < n: 
			seq.append(b) 
			a, b = b, a + b 
			count = count + 1 
		return seq

	print(len(fab(6)))

	��X:
	[1, 1, 2, 3, 5, 8]
	1
	1
	2
	3
	5
	8

yield:
	��J:
	def fab(n): 
		count, a, b = 0, 0, 1 
		while count < n: 
			yield b
			a, b = b, a + b 
			count = count + 1 

	print(fab(6))
	for i in fab(6):
		print(i)

	��X:
	<generator object fab at 0x00000257AE58B5E8>
	1
	1
	2
	3
	5
	8

