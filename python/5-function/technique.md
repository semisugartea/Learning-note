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
	
# 裝飾器 decorator

	裝飾器是定義函數或方法的一種簡化語法，主要是讓新定義的函數，可以有效減少繁複的用函數當參數，或是函數回傳函數的寫法。

以下為例,主程序上用rose代稱f1(f2),而函數f1的作用是傳入函數f2再傳出函數flower,f2變成f1的參數

	def f1(func):
		def flower(color2):
			print('flower')
			return 'color:'+func(color2)				#3	參數func是由f1傳入的f2,參數color2則是引數arg
		return flower								#2	f1(func))(arg)變成flower(arg), 但實際上flower需要傳入函數

	def f2(color1):
		return color1

	rose = f1(f2)
	print(rose('red'))							#1	等價於print((f1(f2))('red'))
	
若在f2前加上裝飾器,即@函數名,則f2的功能就會跟rose一樣,由此省略將f2設為f1的參數的步驟
	
	def f1(func):
	def flower(color2):
		print('flower')
		return 'color:'+func(color2)
	return flower

	@f1
	def f2(color1):
		return color1

	print(f2('red'))
	
# 產生器 generator


# 遞迴 recursion




