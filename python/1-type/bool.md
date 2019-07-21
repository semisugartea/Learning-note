## 真假值 bool

* 分為True和False
	
* 布林運算:and or not

* 優先序:not>and>or
	
		>>> not True and False		#not>and
		False
		>>> not (True and False)
		True

		>>> True or False and False		#and>or
		True
		>>> (True or False) and False
		False

* 除了字面常數 True 及 False 外，數字 0 、 0.0 、空字串及空的資料結構也表示邏輯上的 False，
	
* 反之非 0 、非 0.0 、至少一個元素的字串 (string) 及串列 (list) 都表示邏輯上的 True
	
* 真假值可與數字計算,True默認為1,False默認為0
