# �򥻤���

	assert�Ω�P�_���󦡪��u��,�Y���󦡬��u�h���L,�_�h�o�_AssertionError,��y�k��
	
	assert condition[, arguments]
	
	�䵥����
	
	if not expression:
		raise AssertionError(arguments)

�Ҥl1:

	��J:
	print(1)
	assert 1 + 1 == 2
	print(2)
	assert 2 + 2 == 3
	print(3)

	��X:
	1
	2
	Traceback (most recent call last):
	  File "python.py", line 4, in <module>
		assert 2 + 2 == 3
	AssertionError

�Ҥl2:

	��J:
	a, b = 1, 2
	assert a > b, 'a<b'
	print(a,'&',b)

	��X:
	Traceback (most recent call last):
	  File "python.py", line 2, in <module>
		assert a > b, 'a<b'
	AssertionError: a<b
