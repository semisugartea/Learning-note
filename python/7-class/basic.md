# 基本介紹

類別(class)是規劃物件(object)的藍圖，凡是物件的屬性(attribute)及方法 (method) 都要在類別中定義，語法如下:

	class ClassName:
		<statement-1>
		.
		.
		.
		<statement-N>

# 類別的基本概念

直接先以下面為例:
	
輸入:	
	
	class fruit:
	  num = 7
	  def f(self):
	   return 'hello'

	apple = fruit()
	print(type(apple))
	print(apple.num)
	print(apple.f())

輸出:

	<class '__main__.fruit'>
	7
	hello	
	
1. 在例子中,首先利用class定義類別fruit, 再利用fruit類別的建構子(constructor)建立的類別物件指派給變數apple, 所謂建構子是用類別名稱加上小括弧
2. 由type()可看出變數apple是__main__作用域下的fruit型態
3. 類別中的變數可視為類別屬性(class attribute), 可利用obj.name的方式引出屬性內容
4. 類別中的函數被稱為方法(method), 同樣可利用obj.name的方式引出函數, 在建立方法時必須有一個額外的參數名稱, 通常都使用self

# 關於self的使用
	
* 在方法中的第一個參數self代表類別的物件

輸入:	

	class fruit:
		def show(self):
			print(self)
		 
	a = fruit()
	a.show()
	
輸出:		

	<__main__.fruit object at 0x00000237A6F459E8>	
	
* 第一個參數名可以是其他字

輸入:	

	class fruit:
		def show(apple):
			print(apple)
		 
	a = fruit()
	a.show()	
	
輸出:	

	<__main__.fruit object at 0x000001D232EE5E80>	

* 在不同方法中的第一個參數其實都指向同一物件
	
輸入:

	class fruit:
		def show(apple):
			print(apple)
			
		def show2(banana):
			print(banana)

	a = fruit()
	a.show()
	a.show2()	
	
輸出: 	

	<__main__.fruit object at 0x0000029EB8045EF0>
	<__main__.fruit object at 0x0000029EB8045EF0>	


