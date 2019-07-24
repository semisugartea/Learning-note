# 匿名函數

匿名函數(lambda)是種將運算式重複運用的方式,比利用def創建的函數(function)簡單,其語法為:
	
		lambda arg1 [,arg2,.....argn]:expression

1. 敘述上至少要1個引數,而引數的作用範圍只有在表達式中
2. 使用上必須連表達式利用()包住, 並在後頭利用()填入參數
3. 若不填入參數則會回傳函數位址
4. 與function的比較

		function:
		def polynomial(x):
			return x**2 + x + 1
		print(polynomial(2))

		lambda:
		print((lambda x: x**2 + x + 1)(2))

# 指派給變數

	可以將lambda指派給變數

	輸入:
	a = lambda x: x**2 + x + 1
	print(a)
	print(a(1))
	print(a(2))

	輸出:
	<function <lambda> at 0x0000017C3B92C1E0>
	3
	7

# lambda與函數

lambda常與map(),filter(),reduce()等函數一起使用

* map(function, sequence)			將序列元素分別傳入函數,將函數的回傳值作為新的元素,回傳新元素組成的序列,簡稱映射

* filter(function, sequence)		將序列元素分別傳入函數,若函數回傳True則保留元素,否則移除,回傳篩選後的序列			

* reduce(function, sequence[, initializer])		函數須為有兩個參數,先將序列前2個元素傳入,再將回傳值作為第一個參數,與序列的下一個元素一起傳入函數,最後回傳最終值,可將initializer作為初始參數
