# 集合(set)基本介紹

* 以花括號{}表示, 並使用逗號,區隔元素, 是一個無序且不重複元素的序列

	>>> set1 = { 123, "abc", True, 123}
	>>> set1
	{True, 123, 'abc'}

* 空集合以set()表示,並非{ }

	>>> type(set())
	<class 'set'>
	>>> type({})
	<class 'dict'>

* 不可使用索引數(index)傳遞其中的元素

* 不可形成巢狀結構

* 集合不可相加或乘以整數

* 集合是可變的,但需透過方法

# 關鍵字運算

* in		確認元素或集合是否在集合中

* not in	確認元素或集合是否不在集合中

# 利用函數形成列表

* set([iterable])		將輸入的物件轉為集合, 物件可以是可疊代對象

	輸入字串時會形成字元的集合
	
	>>> set('apple')
	{'l', 'e', 'a', 'p'}

	輸入列表或元組或集合時會形成元素的集合

	>>> set([123,'abc',123])
	{'abc', 123}
	>>> set((123,'abc',123))
	{'abc', 123}
	>>> set({123,'abc',123})
	{'abc', 123}

	輸入字典時會形成鍵的集合

* range([start,] stop[[, step]])

	與set()合用可形成集合
	
	>>> set(range(10))
	{0, 1, 2, 3, 4, 5, 6, 7, 8, 9}

**進階**

* 集合推導式 set comprehension

	* for迴圈

	利用for迴圈可在{}內建立集合
	
	>>> cubes = {i**3 for i in range(5)}
	>>> cubes
	{0, 1, 64, 8, 27}


# 運算子

	詳細內容參照[集論](https://zh.wikipedia.org/wiki/%E9%9B%86%E5%90%88%E8%AE%BA)

	set1 = {1, 2, 3, 4, 5, 6}
	set2 = {4, 5, 6, 7, 8, 9}

	>>>print(set1 | set2)	#聯集
	{1, 2, 3, 4, 5, 6, 7, 8, 9}
	>>>print(set1 & set2)	#交集
	{4, 5, 6}
	>>>print(set1 - set2)	#差集
	{1, 2, 3}
	>>>print(set2 - set1)	#差集
	{8, 9, 7}
	>>>print(set1 ^ set2)	#對稱差集
	{1, 2, 3, 7, 8, 9}

# 相關函數

* len(*set*)		讀取集合**元素個數**

* max(*set*)		讀取集合中**最大值**
	
* min(*set*)		讀取集合中**最小值**

* sum(*set*)		合計集合中的數字

* frozenset([iterable])	將目標對象建立成不可變的集合

# 相關方法

* set.add(obj)										將物件加入集合中,物件只可以是單一元素,若不存在則不進行動作

* set.update(obj)									將物件加入集合中,物件可以是單一元素,字串,列表,元組,集合,字典,但不可為巢狀結構,若存在則不進行動作

	輸入其他結構時會將其中的元素抽出

* set.remove(obj)									將物件從集合中移除,物件只可以是單一元素,若不存在則發生KeyError

* set.discard(obj)									將物件從集合中移除,物件可以是單一元素或集合,若不存在則不進行動作

* set.pop()											隨機將一物件從集合中移除

* set.clear()										清空集合

* set.copy()										表層複製集合內容

* set.union(set1[, set2...])						回傳目標集合與其他集合的聯集

* set.intersection(set1[, set2...])					回傳目標集合與其他集合的交集

* set.intersection_update(set1[, set2...])			目標集合變更為與其他集合的交集,不回傳

* set.difference(set1[, set2...])					回傳目標集合與其他集合的差集

* set.difference_update(set1[, set2...])			目標集合變更為與其他集合的差集,不回傳

* set.symmetric_differenceset1[, set2...]()			回傳目標集合與其他集合的對稱差集

* set.symmetric_difference_update(set1[, set2...])	目標集合變更為與其他集合的對稱差集,不回傳

* set.isdisjoint(set1)								判斷目標集合與其他集合set1是否包含相同元素,若沒有則回傳True,否則回傳False

* set.issubset(set1)								判斷其他集合set1是否包含目標集合的所有元素,若有則回傳True,否則回傳False

* set.issuperset()									判斷目標集合是否包含其他集合set1的所有元素,若有則回傳True,否則回傳False




