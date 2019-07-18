# raise
	
* raise用來發起例外,進而中斷程式,透過在指定的例外後用字串補充說明,便可在raise發起時在例外後顯示說明文:

	輸入:
	number = 100
	if number > 10:
		raise ValueError("Too big!")
	print(number)

	輸出:
	Traceback (most recent call last):
	  File "python.py", line 3, in <module>
		raise ValueError("Too big!")
	ValueError: Too big!

* 當raise用於try的敘述時,發起的例外會程序執行不指定的except的敘述

	輸入:
	try:
		number = 1 / 1
		raise Exception
	except ZeroDivisionError:   
		print("An error occurred")
	except:
		print(number)

	輸出:
	1.0

* 當raise用於except的敘述時,raise可說明例外內容

	輸入:
	try:
		number = 1 / 0
	except :   
		print("Error")
		raise

	輸出:
	Error
	Traceback (most recent call last):
	  File "python.py", line 2, in <module>
		number = 1 / 0
	ZeroDivisionError: division by zero

**進階**

* 可以自行定義例外,但必須直接或間接繼承自Exception類