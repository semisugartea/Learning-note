# �򥻤���

	while�j��Ω󭫽ƬۦP�B�J����P�_���󬰰��γQbreak���_�A�y�k�Φ���:
	
	while *condition*�G
		statement(s)

# �ϥΤ覡

* �b�j��e�]�w�ܼƨæb�j�餤�����ܼƥH�ϧP�_���󬰰�

	��J:
	i = 1
	while i <=5:
		print(i)
		i += 1
	
	��X:
	1
	2
	3
	4
	5

* �Y���ϧP�_���󬰰�,�h�|���͵L���j��(infinite loop)

	��J:
	i = 1
	while i == 1:
		print(i)
	
	��X:
	1
	1
	1
	...���ƿ�X1

* �i�H���_�����c,���h������~���~�h

	��J:
	i = 1
	while i <= 3:
		j = 1
		while j <= 4:
			print(i*j, end=' ')
			j +=1
		print('\n')
		i+=1
	
	��X:
	1 2 3 4 

	2 4 6 8 

	3 6 9 12

* continue �P break

	�bwhile�j�餤,���������r*continue*��,�|�������^�P�_����,�]���Y���b*continue*�����ܼ�,�|�ɭP�L���j��;���������r*break*��,�|���_�j��i��

	��J:
	i = 0
	while i < 9:
		i = i + 1
		if i == 3:
			continue
		elif i == 5:
			break
		print(i)

	��X:
	1
	2
	4

* else

	while...else���S��Ϊk,�g�k�Welse�n�bwhile�j�餧��,�B�Y�ƭn�Pwhile���
	
	* ��while�j�饿�`������,�|����else���ԭz:

	��J:
	i = 1
	while i <=5:
		print(i)
		i += 1
	else:
		print("else")	

	��X:
	1
	2
	3
	4
	5
	else


	* ��while�j��]break���_��,���|����else���ԭz:
	
	��J:
	i = 1
	while i <=5:
		print(i)
		if i == 3:
			break
		i += 1
	else:
		print("else")	

	��X:
	1
	2
	3
	
	
	