## 字串	string

* 以一對單引號''或一對雙引號""表示字串，每一個字被稱為字元(character)

* 跳脫字元 escape character

	在反斜線\後面加上特定字元可形成跳脫字元，此時二者視作同一字元，利用print()可有特殊效果(於simple I/O講解)，而包含跳脫字元的字串稱為跳脫序列(escape sequence)
	
|跳脫序列　　 |　　效果
| ---------- | :-----------:  
|　\a 　　　　|警示音(Alert bell)
|　\b 　　　　|倒退一格(Backspace)
|　\n 　　　　|換行(New line)
|　\r 　　　　|回歸該行起始點(Carriage return)
|　\t 　　　　|水平跳格(Tab，相當於按鍵盤的Tab鍵)
|　\v 　　　　|垂直跳格(Vertical tab)
|　\\ 　　　　|印出反斜線(Backslash)
|　\' 　　　　|印出單引號(Single quote)
|　\" 　　　　|印出雙引號(Double quote)
* 字串可相加,不可相減或相乘

* 字串可與整數相乘,使字串重複

		>>> 'hello' * 3
		'hellohellohello'
		>>> 'sam'*(-1)	#零或負數會變成空字串
		''
* 字串與數字不能相加

* 字串可用索引數(index)來顯示第幾個字元[*index*],第1個字元以[0]表示

* 可用[::]分割(slice)字串,其中含意為[起始:終點:步數]
			#[:::]不成立
			#'.'為一個字元

* in

	使用in可確認字元是否在字串中
	
		>>> 'he' in 'hello'
		True

* 負數為倒著算

# 字串相關函數或方法

* *string*.format(*object*)			使用'{*index*}'.format(*object*)的形式可將物件填入字串中,index代表format()中*object*的順序,沒有寫則會依默認順序填入
	
		>>>msg = "Numbers: {0} {1} {2}". format(4, 5, 6)
		>>>msg
		'Numbers: 4 5 6'

	index可為指定參數(argument)
	
		>>>a = "{x}, {y}".format(x=5, y=12)
		>>>a
		5, 12

* *string*.replace(str1,str2)		回傳將str1替換成str2後的字串

		>>> "Hello ME".replace("ME", "world"))
		"Hello world"

* *string*.startswith(str)			判斷目標字串是否從str開始,若是則回傳True,否則回傳False

		>>> "This is a sentence.".startswith("This")
		True

* *string*.endswith(str)			判斷目標字串是否以str結尾,若是則回傳True,否則回傳False

		>>> "This is a sentence.".endswith("sentence.")
		True

* *string*.upper()					回傳將目標字串的字皆轉成大寫後的字串

		>>> "This is a sentence.".upper())
		"THIS IS A SENTENCE."

* *string*.lower()					回傳將目標字串的字皆轉成小寫後的字串

		>>> "AN ALL CAPS SENTENCE".lower()
		"an all caps sentence"


**與列表相關的方法**

* *string*.split(*["element"]*)		字串轉列表 ,將字串依輸入元素分割

* 'element'.join(list)			列表轉字串,以輸入元素分隔列表的元素
