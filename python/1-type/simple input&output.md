# 輸入

* 使用input()可以輸入

		>>> input("Enter something please: ")
		Enter something please: This is what\nthe user enters!
		'This is what\\nthe user enters!'

# 輸出-print()與直譯器的差異

使用print()或直譯器可以顯示物件內容,但有差異
	
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
|----		|----  |
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

# print()的進階用法

* print(*objects, sep=' ', end='\n', file=sys.stdout)

	objects	:物件,可以數個
	sep		:物件的分隔物,默認是空格
	end		:結尾,默認是換行字元\n
	file	:要寫入的對象

* 格式化輸出

	print('string' % (obj1,obj2,...))
	
	當字串包含特殊字元時,會將對應的物件轉型後輸出

字元		|效果									
----		|----  
%d			|Signed integer decimal.
%i			|Signed integer decimal.
%o			|Unsigned octal.
%u			|Obsolete and equivalent to 'd', i.e. signed integer decimal.
%x			|Unsigned hexadecimal (lowercase).
%X			|Unsigned hexadecimal (uppercase).
%e			|Floating point exponential format (lowercase).
%E			|Floating point exponential format (uppercase).
%f			|Floating point decimal format.
%F			|Floating point decimal format.
%g			|Same as "e" if exponent is greater than -4 or less than precision, "f" otherwise.
%G			|Same as "E" if exponent is greater than -4 or less than precision, "F" otherwise.
%c			|Single character (accepts integer or single character string).
%r			|String (converts any python object using repr()).
%s			|String (converts any python object using str()).
%%			|No argument is converted, results in a "%" character in the result.
