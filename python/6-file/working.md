# �ҥ~�B�z

* try/finally

	���קK�ɮ�Ū�����ѵo�ͪ��ҥ~,�i�ϥ�try/finally�ӥ��}���
	
	try:
	   file = open("test.txt")
	   print(file.read())
	finally:
	   file.close()

* with ..as

	�ϥ�with�y�y�i²�ƤW��,�|�۰������ɮ�,�y�k�� with *���W* [as *�ܼƦW*]
	
	with "test.txt" as file:
		print(file.read())

	�]�i�HŪ���h�ɮ�:
	
	with "test1.txt" as file1, "test2.txt" as file2:
		print(file1.read())
		print(file2.read())

