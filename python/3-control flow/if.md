# �򥻤���

	Python�i�z�Lif�y�y�@�y�{����,��P�_���󬰯u�ɰ���ԭz,�䧹��y�k�Φ���:

	if condition_1:
		statement_block_1
	elif condition_2:
		statement_block_2
	else:
		statement_block_3

# �ϥΤ覡

* �u�ϥ�if�����p

	�i�H�u�ϥ�if,�P�_���󬰯u�ɰ���ԭz,�P�_���󬰰��ɸ��L

	��J:
	i,j = 1, 1
	if i == 1:
		print('i = ',i)
	if j == 2:
		print('j = ',j)
	print("Finished")

	��X:
	i =  1
	Finished

* �ϥ�if-else�����p

	�ϥ�if-else��,�Yif���P�_���󬰯u�ɰ���if���ԭz,�P�_���󬰰��ɰ���else���ԭz

	��J:
	i,j = 1, 1
	if i == 2:
		print('i = ',i)
	else:
		print('j = ',j)
	print("Finished")

	��X:
	j =  1
	Finished

* �ϥ�elif�����p

	elif�N��else if ���N��,�Yif���P�_���󬰰��ɷ|������elif���P�_,���󬰯u�ɰ���elif���ԭz�ᵲ���P�_,���󬰰��ɷ|�ѤU�@��elif�P�_�ΰ���else���ԭz
	elif��i����else,�����i�belse�ᱵelif,�_�h�|�ɭPSyntaxError

	��J:
	i,j = 1, 1
	if i == 2:
		print('i = ',i)
	elif i ==1:
		print('i+j =',i+j)
	else:
		print('j = ',j)
	print("Finished")
	��X:
	i+j = 2
	Finished

* �i�H���_�����c,���h������~���~�h

# �`�ιB��l

�B��l	|�\��	|�d��
---------- | :-----------:  | :-----------: 
<	|�p��	|a < b
>	|�j��	|a > b
<=	|�p�󵥩�	|a <= b
>=	|�j�󵥩�	|a >= b
==	|�۵�	|a == b
!=	|���۵�	|a != b

# �T���B��l Ternary Operator

	�z�L�T���B��l�i�H²�Ʊԭz,�Ω�Q�α�������ܼ�

	variable = obj1 if *condition* else obj2

	���P��

	if *condition*:
		variable = obj1
	else:
		variable = obj2

