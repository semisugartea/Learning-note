# raise
	
* raise�Ψӵo�_�ҥ~,�i�Ӥ��_�{��,�z�L�b���w���ҥ~��Φr��ɥR����,�K�i�braise�o�_�ɦb�ҥ~����ܻ�����:

	��J:
	number = 100
	if number > 10:
		raise ValueError("Too big!")
	print(number)

	��X:
	Traceback (most recent call last):
	  File "python.py", line 3, in <module>
		raise ValueError("Too big!")
	ValueError: Too big!

* ��raise�Ω�try���ԭz��,�o�_���ҥ~�|�{�ǰ��椣���w��except���ԭz

	��J:
	try:
		number = 1 / 1
		raise Exception
	except ZeroDivisionError:   
		print("An error occurred")
	except:
		print(number)

	��X:
	1.0

* ��raise�Ω�except���ԭz��,raise�i�����ҥ~���e

	��J:
	try:
		number = 1 / 0
	except :   
		print("Error")
		raise

	��X:
	Error
	Traceback (most recent call last):
	  File "python.py", line 2, in <module>
		number = 1 / 0
	ZeroDivisionError: division by zero

**�i��**

* �i�H�ۦ�w�q�ҥ~,�����������ζ����~�Ӧ�Exception��