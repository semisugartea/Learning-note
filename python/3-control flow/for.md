# �򥻤���

	for�j��Ω�M���ǦC���C�@�Ӥ���,�y�k�Φ���:
	
	for iterating_var in sequence:
		statements(s)
	
* �Prange()���ϥ�

	�Prange()�ϥη|�C���u�ϥΤ@�ӭȪ��쵲��

	>>> for i in range(5):
	...  print(i)
	...
	0
	1
	2
	3
	4

* �P�r�ꪺ�ϥ�

	�P�r��ϥη|�C���u�ϥΤ@�Ӧr�����쵲��
	
	>>> for i in 'hello':
	...  print(i)
	...
	h
	e
	l
	l
	o

* �P��Ƶ��c���ϥ�

	�P��Ƶ��c�ϥη|�C���u�ϥΤ@�Ӥ������쵲��

	>>> list1=['apple','banana','cat',123,[1,2]]
	>>> for i in list1:
	...  print(i)
	...
	apple
	banana
	cat
	123
	[1, 2]

* �i�H���_�����c,���h������~���~�h

	>>> for i in range(1,3):
	...  for j in range(1,4):
	...   print(i*j, end=' ')
	...  print('\n')
	...
	1 2 3

	2 4 6

* continue �P break

	�bfor�j�餤,���������r*continue*��,�|�������ܤU�@�Ӥ���;���������r*break*��,�|���_�j��i��

	>>> for i in range(1,10):
	...     if i == 3:
	...             continue
	...     elif i ==5:
	...             break
	...     print(i)
	...
	1
	2
	4

* else

	for...else���S��Ϊk,�g�k�Welse�n�bfor�j�餧��,�B�Y�ƭn�Pfor���
	
	* ��for�j�饿�`������,�|����else���ԭz:

	��J:
	for i in range(1,6):
		print(i)
	else:
		print("else")

	��X:
	1
	2
	3
	4
	5
	else

	* ��for�j��]break���_��,���|����else���ԭz:

	��J:	
	for i in range(1,6):
		if i == 3:
			break
		print(i)
	else:
		print("else")

	��X:
	1
	2


























