# 變數 variable
*  Python裡的資料 (data)都是物件 (object)，而變數(variable)相當於物件的識別字 (identifier)，若將物件的字面常數 (literal) 或定義形式指派給變數，該變數便具有物件的控制權。

* 命名規則如同識別字 (identifier)
	
* 指派上可以單一指派或多重指派
		>>> x = 7		#單指派
		>>> a, b = 1, 2	#多指派
	
* 允許同時指派
		>>> a = b = c = 1
* 當指派的變數多餘指派的物件,會導致TypeError
		>>> a, b = 1
		TypeError: 'int' object is not iterable

* 當指派的變數多餘指派的物件,會形成元組(tuple)
		>>> a = 1, 2
		>>> a
		(1, 2)

* 物件的值可以是可變的 (mutable) ，或是不可變的 (immutable) ，通常這是說複合資料型態 (compound data type) 的元素 (element) 是否可以替換
	
不可變	|Number、String、Tuple
----	|----
可變	|List、Dictionary、Set
	
* 對於同一變數，可以重新指派物件。當物件不再使用時，此時直譯器會自動垃圾收集 (garbage collection) ，釋放記憶體空間。

# var2=var1的問題
	
* 當var1指向的物件是可變的時,若var1發生改變,則var2也會變
		
* 當var1指向的物件是不可變的時,若指派其他物件給var1或利用方法改變var1時,則var1的位址會變,var2不會有任何變化
	
# 相關運算子函數
	
* del var 或 del(var)		消除變數
	
		>>> foo = "a string"
		>>> foo
		'a string'
		>>> del foo
		>>> foo
		NameError: name 'foo' is not defined

* id(var)					獲得目標物件的記憶位址

		>>> a = 'hello'
		>>> id(a)
		7696578374880

* var1 is var2				判斷var1和var2是否指向同一位址
	
	
	
	
	
	
	
	
	
	
	
	
	
