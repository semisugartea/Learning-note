# �ܼ� variable
	*  Python�̪���� (data)���O���� (object)�A���ܼ�(variable)�۷�󪫥��ѧO�r (identifier)�A�Y�N���󪺦r���`�� (literal) �Ωw�q�Φ��������ܼơA���ܼƫK�㦳���󪺱����v�C
	
	* �R�W�W�h�p�P�ѧO�r (identifier)
	
	* �����W�i�H��@�����Φh������
	>>> x = 7		#�����
	>>> a, b = 1, 2	#�h����
	
	* ���\�P�ɫ���
	>>> a = b = c = 1
	* ��������ܼƦh�l����������,�|�ɭPTypeError
	>>> a, b = 1
	TypeError: 'int' object is not iterable

	* ��������ܼƦh�l����������,�|�Φ�����(tuple)
	>>> a = 1, 2
	>>> a
	(1, 2)

	* ���󪺭ȥi�H�O�i�ܪ� (mutable) �A�άO���i�ܪ� (immutable) �A�q�`�o�O���ƦX��ƫ��A (compound data type) ������ (element) �O�_�i�H����
	
���i��	|Number�BString�BTuple
----	|----
�i��	|List�BDictionary�BSet
	
	* var2=var1�����D
	
		* ��var1���V������O�i�ܪ���,�Yvar1�o�ͧ���,�hvar2�]�|��
		
		* ��var1���V������O���i�ܪ���,�Y������L����var1�ΧQ�Τ�k����var1��,�hvar1����}�|��,var2���|�������ܤ�
	
	* ���P�@�ܼơA�i�H���s��������C���󤣦A�ϥήɡA���ɪ�Ķ���|�۰ʩU������ (garbage collection) �A����O����Ŷ��C

# �����B��l���
	
	* del var �� del(var)		�����ܼ�
	
	>>> foo = "a string"
	>>> foo
	'a string'
	>>> del foo
	>>> foo
	NameError: name 'foo' is not defined

	* id(var)					��o�ؼЪ��󪺰O�Ц�}

	>>> a = 'hello'
	>>> id(a)
	7696578374880

	* var1 is var2				�P�_var1�Mvar2�O�_���V�P�@��}
	
	
	
	
	
	
	
	
	
	
	
	
	