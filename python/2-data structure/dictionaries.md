# 字典(dictionary)基本介紹

* 以花括號{}表示, 並使用逗號,區隔元素, 每一個元素的型態為key:value
* 不可形成巢狀結構

	鍵(key)不可變,因此可以是數值,字串,真假值,元組
	值(value)可以是數值,字串,真假值,元組,列表	
	=>	不可形成巢狀結構

	>>> dict1 = {"apple": 24, "banana":61 , "cat": 58}
	>>> dict2 = {1: 2, '2':'b' , (3,3): ('c','c'), True:False , 5.5:['e',5]}

* 花括號中沒有任何元素的串列稱為空字典(empty dictionary)

* 利用鍵讀取相對應的值,鍵不存在會顯示 KeyError

	>>> dict1['apple']
	24

* 字典是可變的, 可利用鍵增加新的元素或重新指派新的值

	>>>squares = {1: 1, 2: 4, 3: "error", 4: 16,}
	>>>squares[8] = 64
	>>>squares[3] = 9
	>>>squares
	{1: 1, 2: 4, 3: 9, 4: 16, 8: 64}
	
* 若出現相同的鍵, 則會以後者為準

* 字典不可相加或乘以整數

# 關鍵字運算

* in	確認元素是否在鍵中
	
	nums = {1: "one", 2: "two", 3: "three"}
	>>> 1 in nums
	True
	>>> "three" in nums
	False

* not in	確認元素是否不在鍵中

	>>> 1 not in nums
	False
	>>> 'three' not in nums
	True

* del *dict[key]*						消除其中的元素

# 利用函數形成列表

* dict()	將輸入的物件轉為字典

	形式分為三種:
	dict(**kwarg)					**kwargs:特殊形式,如key=value
	dict(mapping, **kwarg)			mapping	:映射函數
	dict(iterable, **kwarg)			iterable:可疊代對象

	>>> dict(a='one', b='two',c ='three')
	{'a': 'one', 'b': 'two', 'c': 'three'}
	>>> dict(zip(['one', 'two', 'three'], [1, 2, 3]))   # 映射函數
	{'three': 3, 'two': 2, 'one': 1} 
	>>> dict([('one', 1), ('two', 2), ('three', 3)])    # 疊代方式
	{'three': 3, 'two': 2, 'one': 1}

# 相關函數

* len(*dict*)		計算字典中的元素個數

* max(*dict*)		讀取字典中**最大鍵*
	
* min(*dict*)		讀取字典中**最小鍵**

* sum(*tuple*)		合計字典中的鍵

# 相關方法

* dict.clear()							消除所有元素

* dict.copy()							表層複製字典內容	

* dict.fromkeys(seq[, value])			利用輸入字典的鍵建立新字典,可設定值,其值默認為None

* dict.items()							將字典中的每一個元素回傳成dict_items([(key1, value1), (key2, value2),...])的形式

* dict.keys()							將字典中的每一個鍵回傳成dict_keys([key1, key2, ...])的形式

* dict.values()							將字典中的每一個值回傳成dict_values([value1, value2, ...])的形式

* dict.get(key, default=None)			讀取輸入鍵相對的值,沒有則默認為None,可設定其他回傳值

* dict.setdefault(key, default=None)	讀取輸入鍵相對的值,沒有則插入鍵,其值默認為None,可設定其他值

* dict.update(dict2)					將dict2的元素加入目標字典

* dict.pop(key[,default])				刪除鍵相對的元素並回傳相對的值,鍵不存在則回傳default值,若default值不設定會導致回傳時發生KeyError

* dict.popitem()						隨機刪除字典中的其中一個元素,並以(key, value)的形式回傳該元素










