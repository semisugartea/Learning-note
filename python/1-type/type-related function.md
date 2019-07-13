# 前言
	
	* 以*object*代表輸入的物件或變數

# 型態轉變函數
* int(*object [, base]*)	目標物件轉成整數

	* 目標物件可以是"整數型字串", "浮點數", "真假值"

	* base代表進制,當目標物件是字串可使用,默認為十進制

* float(*object*)	目標物件轉成浮點數

* complex(*object [,imag]*)	目標物件轉成複數

* str(*object*)	目標物件轉成字串

* hex(*object*)	目標物件轉成十六進制的字串

* oct(*object*)	目標物件轉成八進制的字串

* chr(*object*)	目標物件(ASCII碼)轉成對應的字元

* ord(*object*) 目標物件(字元)轉成對應的ASCII碼


# 訊息讀取函數

* bool(*object*)	判斷物件的**真假值**

* len(*object*)		讀取目標物件**長度**

* type(*object*)	讀取目標物件**型態**

*  eval(*expression*)	讀取字串型態的表達式的結果

# 字串相關函數

* format method

	使用'{*[index]*}'.format(*object*)的形式可將物件填入字串中,index代表format()中*object*的順序,沒有寫則會依默認順序填入
	
	>>>msg = "Numbers: {0} {1} {2}". format(4, 5, 6)
	>>>msg
	'Numbers: 4 5 6'

	index可為指定參數(argument)
	
	>>>a = "{x}, {y}".format(x=5, y=12)
	>>>a
	5, 12



















