# 基本介紹

	while迴圈用於重複相同步驟直到判斷條件為假或被break中斷，語法形式為:
	
	while *condition*：
		statement(s)

# 使用方式

* 在迴圈前設定變數並在迴圈中控制變數以使判斷條件為假

	輸入:
	i = 1
	while i <=5:
		print(i)
		i += 1
	
	輸出:
	1
	2
	3
	4
	5

* 若不使判斷條件為假,則會產生無限迴圈(infinite loop)

	輸入:
	i = 1
	while i == 1:
		print(i)
	
	輸出:
	1
	1
	1
	...重複輸出1

* 可以有巢狀結構,內層結束後才換外層

	輸入:
	i = 1
	while i <= 3:
		j = 1
		while j <= 4:
			print(i*j, end=' ')
			j +=1
		print('\n')
		i+=1
	
	輸出:
	1 2 3 4 

	2 4 6 8 

	3 6 9 12

* continue 與 break

	在while迴圈中,執行到關鍵字*continue*時,會直接跳回判斷條件,因此若不在*continue*控制變數,會導致無限迴圈;執行到關鍵字*break*時,會中斷迴圈進行

	輸入:
	i = 0
	while i < 9:
		i = i + 1
		if i == 3:
			continue
		elif i == 5:
			break
		print(i)

	輸出:
	1
	2
	4

* else

	while...else有特殊用法,寫法上else要在while迴圈之後,且縮排要與while對齊
	
	* 當while迴圈正常結束時,會執行else的敘述:

	輸入:
	i = 1
	while i <=5:
		print(i)
		i += 1
	else:
		print("else")	

	輸出:
	1
	2
	3
	4
	5
	else


	* 當while迴圈因break中斷時,不會執行else的敘述:
	
	輸入:
	i = 1
	while i <=5:
		print(i)
		if i == 3:
			break
		i += 1
	else:
		print("else")	

	輸出:
	1
	2
	3
	
	
	