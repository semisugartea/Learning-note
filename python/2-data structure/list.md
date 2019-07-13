# 基本介紹

* 以方括號[]表示, 並使用逗號(,)區隔

	>>> words = ["Hello", "world", "!"]
	>>> list1 = [ 123, "abc", True]			#可同時包含不同型態



* 方括號中沒有任何元素的串列稱為空串列(empty list)

* 與字串相似,列表可使用索引數(index)傳遞其中的元素

	>>> print(words[0])
	Hello
	>>> print(words[0][0])
	H

* 可形成巢狀結構

	>>>number = 3
	>>>things = ["string", 0, [1, 2, number], 4.56]
	>>>print(things[2])
	[1, 2, 3]
	>>>print(things[2][2])
	3




# 與字串差異

* 與字串相似,列表可相加或相乘

	>>> str = words + list1
	>>> str
	['Hello', 'world', '!', 123, 'abc', True]
	
	>>> str2 = words*3
	>>> str2
	['Hello', 'world', '!', 'Hello', 'world', '!', 'Hello', 'world', '!']
	
* 與字串相似,列表可分割(slice), 同樣是[起始:終點:步數]

	>>>squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
	>>>squares[2:6]
	[4, 9, 16, 25]

* 與字串不同的是,列表可變(mutable)

	>>> str = 'apple'
	>>> str[0] = 'b'
	TypeError: 'str' object does not support item assignment
	
	>>> list = ['apple', 'banana', 'cat']
	>>> list[2] = 'dog'
	>>> list
	['apple', 'banana', 'dog']


# 關鍵字運算

* in

	使用in可確認元素是否在列表中

	>>>words = ["spam", "egg", "spam", "sausage"]
	>>>"spam" in words
	True
	>>>"egg" in words
	True
	>>>"tomato" in words
	False

* not

	not可置於判斷元素的前後

	>>>nums = [1, 2, 3]
	>>>not 4 in nums
	True
	>>>4 not in nums
	True
	>>>not 3 in nums
	False
	>>>3 not in nums
	False


# 利用函數形成列表

* list(*sequence*) 將輸入的序列(sequence)轉為列表, 序列可以是元組或字串 

	>>> tup = (123, 'apple', 'banana', 'cat')
	>>> list(tup)
	[123, 'apple', 'banana', 'cat']

	>>> str="Hello World"
	>>> list(str)
	['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
	
* range([start,] stop[[, step]])	建構數字序列,當數到stop時直接停止

	與list()合用可形成列表
	
	>>> list(range(10))				#只有一個數時默認為stop, start默認為0, step默認為1
	[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

	>>> list(range(5,10))			#兩個數時分別默認為start, stop, step默認為1
	[5, 6, 7, 8, 9]

	>>> list(range(5, 20, 2))		#三個數
	[5, 7, 9, 11, 13, 15, 17, 19]

	* 列表若太大會導致MemoryError或OverflowError
	>>>list(range(10**100))
	OverflowError

**進階**

* for迴圈

	利用for迴圈可在[]內建立列表

	>>>cubes = [i**3 for i in range(5)]
	>>>cubes
	[0, 1, 8, 27, 64]

* if陳述

	利用if陳述可篩選元素
	
	>>>evens=[i**2 for i in range(10) if i**2 % 2 == 0]
	>>>evens
	[0, 4, 16, 36, 64]


# 字串與列表互相轉換的方法

	方法(method)是指引用類別class中的函數, 在此是引用<class 'list'>的函數

* *string*.split(*["element"]*)		字串轉列表 ,將字串依輸入元素分割

	>>> str1 = 'hello world app123'
	>>> str1.split()					#若未填入元素,則默認為空格
	['hello', 'world', 'app123']
	>>> str1.split(' ')				
	['hello', 'world', 'app123']

	>>> str2 = 'hello.world.app123'
	>>> str2.split('.')					#填入元素會被消除
	['hello', 'world', 'app123']

* 'element'.join(list)				列表轉字串,以輸入元素分隔列表的元素

	>>> ''.join(['hello','world','app123'])		#若未填入元素,則默認為無
	'helloworldapp123'

	>>> '.'.join(['hello','world','app123'])
	hello.world.app123'

# 相關函數

* del *list*
	
	可使用del消除其中的元素

	>>> words = ["Hello", "world", "!"]
	>>> del words[1]
	>>> words
	['Hello', '!']

* len(*list*)	讀取列表**長度**

* max(*list*)		讀取列表**最大值**
	
* min(*list*)		讀取列表**最小值**

* sorted(iterable, cmp=None, key=None, reverse=False)	回傳列表排序後的值,原列表不受影響

	iterable -- 可疊代對象。
	cmp -- 比較的函數，這個具有兩個參數，參數的值都是從可疊代對象中取出，此函數必須遵守的規則為，大於則返回1，小於則返回-1，等於則返回0。
	key -- 主要是用來進行比較的元素，只有一個參數，具體的函數的參數就是取自於可疊代對象中，指定可疊代對象中的一個元素來進行排序。
	reverse -- 排序規則，reverse = True 降序 ， reverse = False 升序（默認）

# 相關方法

* list.append(obj)	在列表結尾添加新物件

* list.count(obj)	統計某個物件在列表的出現次數

* list.extend(seq)	在列表結尾添加新列表

	與append的不同:append會將新列表視做一個元素加入目標列表,而extend會將新列表中的元素抽出並加入目標列表

* list.index(obj)	找出目標物件的索引數

* list.insert(index, obj)	在索引數的位置插入物件

* list.pop(obj = list[-1])	移除列表中的一個物件(默認為最後一個),並回傳該物件內容

* list.remove(obj)	移除列表中的第一個符合的物件

* list.reverse()	將列表排列反向

* list.sort(cmp=None, key=None, reverse=False)		將原列表排序

	cmp -- 比較的函數，這個具有兩個參數，參數的值都是從可疊代對象中取出，此函數必須遵守的規則為，大於則返回1，小於則返回-1，等於則返回0。
	key -- 主要是用來進行比較的元素，只有一個參數，具體的函數的參數就是取自於可疊代對象中，指定可疊代對象中的一個元素來進行排序。
	reverse -- 排序規則，reverse = True 降序 ， reverse = False 升序（默認）

* list.clear()	清空列表

* list.copy()	複製列表





