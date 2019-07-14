# 輸入

	* 使用input()可以輸入
	>>> input("Enter something please: ")
	Enter something please: This is what\nthe user enters!
	'This is what\\nthe user enters!'

# 輸出

	* 使用print()或直譯器可以顯示物件內容,但有差異
	
	* 直譯器上直接輸入字串會顯示引號,print()內輸入字串不顯示引號
	
	>>> 'apple'
	'apple'
	>>> print('apple')
	apple

	
	* 直譯器上以逗號區隔元素會形成元組, print()以逗號區隔元素會直接顯示內容

	>>> str1='apple'
	>>> 'str1:',str1
	('str1:', 'apple')
	>>> print('str1:',str1)
	str1: apple
	
	* print()會有跳脫序列的效果, 直譯器則否
	
	
|跳脫序列　　 |效果									|
|　\a 　　　　|警示音(Alert bell)					|
|　\b 　　　　|倒退一格(Backspace)					|
|　\n 　　　　|換行(New line)						|
|　\r 　　　　|回歸該行起始點(Carriage return)		|
|　\t 　　　　|水平跳格(Tab，相當於按鍵盤的Tab鍵)	|
|　\v 　　　　|垂直跳格(Vertical tab)				|
|　\\ 　　　　|印出反斜線(Backslash)				|
|　\' 　　　　|印出單引號(Single quote)				|
|　\" 　　　　|印出雙引號(Double quote)				|

	* 若不要產生效果，則須在字串前加r
	>>> print(r'Ru\noob')
	Ru\noob
