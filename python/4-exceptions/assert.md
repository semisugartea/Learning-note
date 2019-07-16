# 基本介紹

	assert用於判斷條件式的真假,若條件式為真則跳過,否則發起AssertionError,其語法為
	
	assert condition[, arguments]
	
	其等價為
	
	if not expression:
		raise AssertionError(arguments)

例子1:

	輸入:
	print(1)
	assert 1 + 1 == 2
	print(2)
	assert 2 + 2 == 3
	print(3)

	輸出:
	1
	2
	Traceback (most recent call last):
	  File "python.py", line 4, in <module>
		assert 2 + 2 == 3
	AssertionError

例子2:

	輸入:
	a, b = 1, 2
	assert a > b, 'a<b'
	print(a,'&',b)

	輸出:
	Traceback (most recent call last):
	  File "python.py", line 2, in <module>
		assert a > b, 'a<b'
	AssertionError: a<b
