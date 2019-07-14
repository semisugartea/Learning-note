# 元組(tuple)基本介紹

* 以圓括號()表示, 並使用逗號,區隔

* 圓括號中沒有任何元素的串列稱為空元組(empty tuple)

* 與列表相似,元組可使用索引數(index)傳遞其中的元素

* 可形成巢狀結構

* 當指派的變數多餘指派的物件,會形成元組(tuple),稱為tuple packing

	>>> tup1 = "one", "two", "three"
	>>> tup1
	('one', 'two', 'three')

# 與列表對比

* 與列表相似,元組可相加

* 與列表相似,元組可利用乘以整數來重複

* 與列表相似,元組可分割(slice), 同樣是[起始:終點:步數]

* 與列表不同的是,元組是不可變的(immutable), 但運行速度比較快且記憶空間比較小

	>>> tup1 = ('apple', 'banana', 'cat')
	>>> tup1[2] = 'dog'
	TypeError: 'tuple' object does not support item assignment

# 關鍵字運算

* in	確認元素是否在元組中

* not in	確認元素是否不在元組中

# 利用函數形成列表

* tuple(*sequence*) 將輸入的序列(sequence)轉為元組, 序列可以是列表或字串 

* range([start,] stop[[, step]])	

	與tuple()合用可形成元組

**進階**

* 不支持推導式(comprehension)

	與列表不同的是, 在圓括號()使用for迴圈時, 會形成generator, 而非元組

	>>> cubes = (i**3 for i in range(5))
	>>> type(cubes)
	<class 'generator'>
	>>> for j in cubes:
	...  print(j)
	...
	0
	1
	8
	27
	64

# 相關函數

* len(*tuple*)		讀取元組**元素個數**

* max(*tuple*)		讀取元組中**最大值**
	
* min(*tuple*)		讀取元組中**最小值**

* sum(*tuple*)		合計元組中的數字



















