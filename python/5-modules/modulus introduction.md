# 基本介紹

	模組(modules)是指包含定義變數與函數的文件,其副檔名為.py

# 使用方式

* import

	使用import *模組名*可以將模組引入,其中的變數與函數要在前面加入函數名和點號.才可使用

	import math
	print(math.pi)
	print(math.floor(math.pi))

	* 若引入失敗,會導致發生ImportError的例外
	* 一個模組只會被引入一次
	
* as

	使用import *模組名* as *名稱* 可以改變引入的模組在文件中的名稱,一個模組可以有多個稱呼

	import math as apple
	import math as banana
	print(apple.pi)
	print(banana.pi)

* from

	使用from可以只引入部分模組,語法如下:

	from *模組名* import name1[, name2[, ... nameN]]

	使用此方式引入的變數與函數可以不加前綴

	from math import pi
	print(pi)


	from *模組名* import \* 可以將模組全部引入

	from math import *
	print(pi)
	print(floor(pi))

# 確認模組是否被引入

	如果不要一段程式碼在被引入後執行,可以確認變數__name__是否等於__main__
	若等於,則代表該模組自身在執行中,否則代表被引入中
	
	文件名:test.py
	if __name__ == '__main__':
	   print('main')
	else:
	   print('other')

	終端機輸入:
	$ python test.py
	main

	直譯器輸入:
	>>> import test
	other

# dir函數







