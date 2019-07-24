# 文檔字符串 DocStrings

在函數中可使用一對三個引號'''作註解,可使用print(*function_name*.__doc__)顯示內容

	輸入:
	def hello():
		'''hello world
		'''
		print('apple')
	 
	print(hello.__doc__)

	輸出:
	hello world

# 遞迴 recursion

*   遞迴是指函數呼叫自己的函數名,此時呼叫者暫停並等待回傳值,執行被呼叫者,回傳有效的值後再執行呼叫者,以下利用階乘函數為例

		輸入:
		def fac(n):
			print(n)
			if n == 1:
				return 1
			else: 
				a = n * fac(n-1)
				print(n)
				return a

		print(fac(3))

		輸出:
		3
		2
		1
		2
		3
		6

*   若不設定終點值,會導致RuntimeError的例外

		輸入:
		def fac(n):
			return n * fac(n-1)

		輸出:
		RuntimeError: maximum recursion depth exceeded

* 遞迴可以是間接的,即函數呼叫別的函數名,而該函數呼叫自己的函數名



