# 基本介紹

	Python可透過if語句作流程控制,當判斷條件為真時執行敘述,其完整語法形式為:

	if condition_1:
		statement_block_1
	elif condition_2:
		statement_block_2
	else:
		statement_block_3

# 使用方式

* 只使用if的情況

	可以只使用if,判斷條件為真時執行敘述,判斷條件為假時跳過

	輸入:
	i,j = 1, 1
	if i == 1:
		print('i = ',i)
	if j == 2:
		print('j = ',j)
	print("Finished")

	輸出:
	i =  1
	Finished

* 使用if-else的情況

	使用if-else時,若if的判斷條件為真時執行if的敘述,判斷條件為假時執行else的敘述

	輸入:
	i,j = 1, 1
	if i == 2:
		print('i = ',i)
	else:
		print('j = ',j)
	print("Finished")

	輸出:
	j =  1
	Finished

* 使用elif的情況

	elif代表else if 的意思,若if的判斷條件為假時會先執行elif的判斷,條件為真時執行elif的敘述後結束判斷,條件為假時會由下一個elif判斷或執行else的敘述
	elif後可不接else,但不可在else後接elif,否則會導致SyntaxError

	輸入:
	i,j = 1, 1
	if i == 2:
		print('i = ',i)
	elif i ==1:
		print('i+j =',i+j)
	else:
		print('j = ',j)
	print("Finished")
	輸出:
	i+j = 2
	Finished

* 可以有巢狀結構,內層結束後才換外層

# 常用運算子

運算子	|功能	|範例
---------- | :-----------:  | :-----------: 
<	|小於	|a < b
>	|大於	|a > b
<=	|小於等於	|a <= b
>=	|大於等於	|a >= b
==	|相等	|a == b
!=	|不相等	|a != b

# 三元運算子 Ternary Operator

	透過三元運算子可以簡化敘述,用於利用條件指派變數

	variable = obj1 if *condition* else obj2

	等同於

	if *condition*:
		variable = obj1
	else:
		variable = obj2

