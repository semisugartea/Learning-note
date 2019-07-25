# 讀取 reading

* read()方法

在文件變數後加上.read()可以讀取文件內容

test.txt內容:
	applebananacatdog
	123456
	hello world
	
輸入:
	file = open("test.txt", "r")
	content = file.read()
	print(content)
	file.close()

輸出:
	applebananacatdog
	123456
	hello world

正式語法為read(*size*),*size*代表讀取的字數,下例可看出讀取只往前不回頭的

輸入:

	file = open("test.txt", "r")
	print(file.read(5))
	print(file.read(8))
	print(file.read(13))
	print(file.read())
	file.close()

輸出:

	apple
	bananaca
	tdog
	123456
	h
	ello world

一個文件在一次開啟中只能讀取一次

輸入:

	file = open("test.txt", "r")
	file.read()
	print('read again')
	print(file.read())
	print('stop')
	file.close()

輸出:

	read again

	stop

* readline() 和 readline()方法
	
	使用readline()方法可讀取一行
	
	輸入:
	file = open("test.txt", "r")
	print(file.readline())
	print(file.readline())
	print(file.readline())
	file.close()

	輸出:
	applebananacatdog

	123456

	hello world

	使用readlines()方法可讀取多行並建立列表
	
	輸入:
	file = open("test.txt", "r")
	print(file.readlines())
	file.close()
	
	輸出:
	['applebananacatdog\n', '123456\n', 'hello world']
	
* for迴圈
	
	使用for迴圈可分行顯示
	
	輸入:
	file = open("test.txt", "r")
	for i in file:
		print(i)
	file.close()
	
	輸出:
	applebananacatdog

	123456

	hello world
	
# 寫入 writing

* write() 方法

	使用write()方法可以將()的內容寫入文件,內容必須是**字串**
	
	輸入:
	file = open("test.txt", "w")
	file.write("New things")
	file.close()

	file = open("test.txt", "r")
	print(file.read())
	file.close()
	
	輸出:
	New things
	
	此時test.txt的內容是:
		New things
	代表原有內容會完全刪除後再填入新內容
	
	write()方法會回傳寫入字串的字數
	
	file = open("test.txt", "w")
	number = file.write("New things")
	print(number)
	file.close()
	
	10

