# ��J

	* �ϥ�input()�i�H��J
	>>> input("Enter something please: ")
	Enter something please: This is what\nthe user enters!
	'This is what\\nthe user enters!'

# ��X-print()�P��Ķ�����t��

�ϥ�print()�Ϊ�Ķ���i�H��ܪ��󤺮e,�����t��
	
	* ��Ķ���W������J�r��|��ܤ޸�,print()����J�r�ꤣ��ܤ޸�
	
	>>> 'apple'
	'apple'
	>>> print('apple')
	apple

	
	* ��Ķ���W�H�r���Ϲj�����|�Φ�����, print()�H�r���Ϲj�����|������ܤ��e

	>>> str1='apple'
	>>> 'str1:',str1
	('str1:', 'apple')
	>>> print('str1:',str1)
	str1: apple
	
	* print()�|������ǦC���ĪG, ��Ķ���h�_
		
|����ǦC�@�@ |�ĪG									|
|----		|----  |
|�@\a �@�@�@�@|ĵ�ܭ�(Alert bell)					|
|�@\b �@�@�@�@|�˰h�@��(Backspace)					|
|�@\n �@�@�@�@|����(New line)						|
|�@\r �@�@�@�@|�^�k�Ӧ�_�l�I(Carriage return)		|
|�@\t �@�@�@�@|��������(Tab�A�۷�����L��Tab��)	|
|�@\v �@�@�@�@|��������(Vertical tab)				|
|�@\\ �@�@�@�@|�L�X�ϱ׽u(Backslash)				|
|�@\' �@�@�@�@|�L�X��޸�(Single quote)				|
|�@\" �@�@�@�@|�L�X���޸�(Double quote)				|

	* �Y���n���ͮĪG�A�h���b�r��e�[r
	>>> print(r'Ru\noob')
	Ru\noob

# print()���i���Ϊk

* print(*objects, sep=' ', end='\n', file=sys.stdout)

	objects	:����,�i�H�ƭ�
	sep		:���󪺤��j��,�q�{�O�Ů�
	end		:����,�q�{�O����r��\n
	file	:�n�g�J����H

* �榡�ƿ�X

	print('string' % (obj1,obj2,...))
	��r��]�t�H�U�Φ���,�|�N�����������૬���X

�r��		|�ĪG									
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


























