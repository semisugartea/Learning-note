# �򥻤���

	�Ҳ�(modules)�O���]�t�w�q�ܼƻP��ƪ����,����ɦW��.py

# �ϥΤ覡

* import

	�ϥ�import *�ҲզW*�i�H�N�ҲդޤJ,�䤤���ܼƻP��ƭn�b�e���[�J��ƦW�M�I��.�~�i�ϥ�

	import math
	print(math.pi)
	print(math.floor(math.pi))

	* �Y�ޤJ����,�|�ɭP�o��ImportError���ҥ~
	* �@�ӼҲեu�|�Q�ޤJ�@��
	
* as

	�ϥ�import *�ҲզW* as *�W��* �i�H���ܤޤJ���Ҳզb��󤤪��W��,�@�ӼҲեi�H���h�Ӻ٩I

	import math as apple
	import math as banana
	print(apple.pi)
	print(banana.pi)

* from

	�ϥ�from�i�H�u�ޤJ�����Ҳ�,�y�k�p�U:

	from *�ҲզW* import name1[, name2[, ... nameN]]

	�ϥΦ��覡�ޤJ���ܼƻP��ƥi�H���[�e��

	from math import pi
	print(pi)


	from *�ҲզW* import \* �i�H�N�Ҳե����ޤJ

	from math import *
	print(pi)
	print(floor(pi))

# �T�{�ҲլO�_�Q�ޤJ

	�p�G���n�@�q�{���X�b�Q�ޤJ�����,�i�H�T�{�ܼ�__name__�O�_����__main__
	�Y����,�h�N��ӼҲզۨ��b���椤,�_�h�N��Q�ޤJ��
	
	���W:test.py
	if __name__ == '__main__':
	   print('main')
	else:
	   print('other')

	�׺ݾ���J:
	$ python test.py
	main

	��Ķ����J:
	>>> import test
	other

# dir

	* �bimport�Ҳի�,�i�Q��dir(*�ҲզW*)�d�ݸӼҲժ��Ҧ��ܼ�

	>>> import math
	>>> dir(math)
	['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']

	�Y����J*�ҲզW*,�h�|��ܷ�e�Ҧ��ܼƩM�ҲզW

	>>> dir()
	['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'math']

	�ϥ�del�i�h���Ҳ�

	>>> del math
	>>> dir()
	['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'a']












