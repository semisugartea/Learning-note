# 疊代器 iterator

疊帶(iteration):利用迴圈遍歷對象的元素的動作
可疊帶對象(iterable):可被遍歷元素的對象
疊代器(iterator):可執行疊帶的程序

* iter(obj)			利用物件生成疊代器

*   next(iterator)	讀取疊代器的下一個項目,當讀不到物件時,會產生StopIteration的例外

		輸入:
		list1=[1,2,3,4]
		a = iter(list1)
		print(next(a))
		print(next(a))
		print(next(a))
		print(next(a))
		print(next(a))

		輸出:
		1
		2
		3
		4
		Traceback (most recent call last):
		  File "python.py", line 7, in <module>
			print(next(a))
		StopIteration

# yield

在函數中使用yield時,可以產生一組物件,並回傳物件的位址後暫停,當函數在被呼叫時繼續,可以視作與主程序平行運作,而此函數可以變成疊代器
	
* for迴圈
	
可利用for迴圈讀取物件,當函數結束時迴圈結束

	輸入:
	def count(n):
		i =1
		print('start')
		while i <=n:
			print('hello')
			yield i
			print('world')
			i += 1
		yield 'finish'

	print(count(2))
	for j in count(2):
		print(j)
		print('pause')

	輸出:
	<generator object count at 0x00000175C31EB5E8>
	start
	hello
	1
	pause
	world
	hello
	2
	pause
	world
	finish
	pause

* next()

可利用函數next()漸進式的讀取物件,當讀不到物件時,會產生StopIteration的例外

	輸入:
	def count(n):
		i =1
		while i <=n:
			yield i
			i += 1

	a = count(3)
	print(next(a))
	print(next(a))
	print(next(a))
	print(next(a))

	輸出:
	1
	2
	3
	Traceback (most recent call last):
	  File "python.py", line 11, in <module>
		print(next(a))
	StopIteration

* 與return的差異

在產生一個序列上,return必須一次建立整個序列,而yield只要一次建立一個,相對省很多空間,以下利用費氏數列為例

return:

	輸入:
	def fab(n): 
		count, a, b = 0, 0, 1 
		seq = [] 
		while count < n: 
			seq.append(b) 
			a, b = b, a + b 
			count = count + 1 
		return seq

	print(len(fab(6)))

	輸出:
	[1, 1, 2, 3, 5, 8]
	1
	1
	2
	3
	5
	8

yield:

	輸入:
	def fab(n): 
		count, a, b = 0, 0, 1 
		while count < n: 
			yield b
			a, b = b, a + b 
			count = count + 1 

	print(fab(6))
	for i in fab(6):
		print(i)

	輸出:
	<generator object fab at 0x00000257AE58B5E8>
	1
	1
	2
	3
	5
	8

