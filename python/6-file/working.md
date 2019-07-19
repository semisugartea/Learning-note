# 例外處理

* try/finally

	為避免檔案讀取失敗發生的例外,可使用try/finally來打開文件
	
	try:
	   file = open("test.txt")
	   print(file.read())
	finally:
	   file.close()

* with ..as

	使用with語句可簡化上例,會自動關閉檔案,語法為 with *文件名* [as *變數名*]
	
	with "test.txt" as file:
		print(file.read())

	也可以讀取多檔案:
	
	with "test1.txt" as file1, "test2.txt" as file2:
		print(file1.read())
		print(file2.read())

