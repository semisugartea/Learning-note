# 基本介紹

for迴圈用於遍歷序列的每一個元素,語法形式為:
	
		for iterating_var in sequence:
			statement(s)

# 使用方式
	
* 與range()的使用

與range()使用會每次只使用一個值直到結束

	>>> for i in range(5):
	...  print(i)
	...
	0
	1
	2
	3
	4

* 與字串的使用

與字串使用會每次只使用一個字元直到結束
	
	>>> for i in 'hello':
	...  print(i)
	...
	h
	e
	l
	l
	o

* 與資料結構的使用

與資料結構使用會每次只使用一個元素直到結束

	>>> list1=['apple','banana','cat',123,[1,2]]
	>>> for i in list1:
	...  print(i)
	...
	apple
	banana
	cat
	123
	[1, 2]

* 可以有巢狀結構,內層結束後才換外層

		>>> for i in range(1,3):
		...  for j in range(1,4):
		...   print(i*j, end=' ')
		...  print('\n')
		...
		1 2 3

		2 4 6

* continue 與 break

在for迴圈中,執行到關鍵字*continue*時,會直接跳至下一個元素;執行到關鍵字*break*時,會中斷迴圈進行

	輸入:
	for i in range(1,10):
		if i == 3:
			continue
		elif i == 5:
			break
		print(i)

	輸出:
	1
	2
	4

# else

for...else有特殊用法,寫法上else要在for迴圈之後,且縮排要與for對齊
	
*   當for迴圈正常結束時,會執行else的敘述:

		輸入:
		for i in range(1,6):
			print(i)
		else:
			print("else")

		輸出:
		1
		2
		3
		4
		5
		else

*   當for迴圈因break中斷時,不會執行else的敘述:

		輸入:	
		for i in range(1,6):
			if i == 3:
				break
			print(i)
		else:
			print("else")

		輸出:
		1
		2


