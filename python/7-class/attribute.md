# 屬性(attribute)

在類別中分為類別屬性與實體屬性,以下說明差異

# 屬性的識別字

* 當類別屬性與實體屬性使用相同識別字時,則無法用實體物件存取類別屬性

輸入:

	class fruit:
		x = 0		#類別屬性

		def __init__(self, x):
			self.x = x 	#實體屬性
			fruit.x += 1  	#每當建立一個實體,類別屬性+1

	f1 = fruit(123)
	print(f1.x)
	print(fruit.x)
	f2 = fruit(456)
	print(f2.x)
	print(fruit.x)

輸出:

	123
	1
	456
	2

* 當類別屬性與實體屬性使用不同識別字時,則可用實體物件存取類別屬性

輸入:

	class fruit:
		x = 0 

		def __init__(self, y):
			self.y = y 
			fruit.x += 1

	f1 = fruit(123)
	print(f1.x)
	print(f1.y)
	print(fruit.x)
	f2 = fruit(456)
	print(f2.x)
	print(f2.y)
	print(fruit.x)

輸出:

	1
	123
	1
	2
	456
	2

# 屬性例外(AttributeError)

* 當屬性不存在時,會產生屬性例外

輸入:

	class fruit:
		def __init__(self):
			self.name = 'apple'
			self.color = 'red'

	a = fruit()
	print(a.price)

輸出:

	AttributeError: 'fruit' object has no attribute 'price'