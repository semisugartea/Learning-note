# �C��(list)�򥻤��� 

* �H��A��[]���, �èϥγr��,�Ϲj

	>>> words = ["Hello", "world", "!"]
	>>> list1 = [ 123, "abc", True]			#�i�P�ɥ]�t���P���A

* ��A�����S�����󤸯�����C�٬��ŦC��(empty list)

* �P�r��ۦ�,�C��i�ϥί��޼�(index)�ǻ��䤤������

	>>> print(words[0])
	Hello
	>>> print(words[0][0])
	H

* �i�Φ��_�����c

	>>>number = 3
	>>>things = ["string", 0, [1, 2, number], 4.56]
	>>>print(things[2])
	[1, 2, 3]
	>>>print(things[2][2])
	3

# �P�r����

* �P�r��ۦ�,�C��i�ۥ[

	>>> str = words + list1
	>>> str
	['Hello', 'world', '!', 123, 'abc', True]

* �P�r��ۦ�,�C��i�Q�έ��H��ƨӭ���

	>>> str2 = words*3
	>>> str2
	['Hello', 'world', '!', 'Hello', 'world', '!', 'Hello', 'world', '!']
	
* �P�r��ۦ�,�C��i����(slice), �P�ˬO[�_�l:���I:�B��]

	>>>squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
	>>>squares[2:6]
	[4, 9, 16, 25]

* �P�r�ꤣ�P���O,�C��O�i�ܪ�(mutable)

	>>> str = 'apple'
	>>> str[0] = 'b'
	TypeError: 'str' object does not support item assignment
	
	>>> list = ['apple', 'banana', 'cat']
	>>> list[2] = 'dog'
	>>> list
	['apple', 'banana', 'dog']


# ����r�B��

* in	�T�{�����O�_�b�C��

	>>>words = ["spam", "egg", "spam", "sausage"]
	>>>"spam" in words
	True
	>>>"egg" in words
	True
	>>>"tomato" in words
	False

* not in	�T�{�����O�_���b�C��

	>>>nums = [1, 2, 3]
	>>>4 not in nums
	True
	>>>3 not in nums
	False

* del list[[�_�l:]���I[:�B��]]		�����䤤������,�Pslice�B���h

	>>> words = ["Hello", "world", "!"]
	>>> del words[1]
	>>> words
	['Hello', '!']

# �Q�Ψ�ƧΦ��C��

* list(*sequence*) �N��J���ǦC(sequence)�ର�C��, �ǦC�i�H�O���թΦr�� 

	>>> tup = (123, 'apple', 'banana', 'cat')
	>>> list(tup)
	[123, 'apple', 'banana', 'cat']

	>>> str="Hello World"
	>>> list(str)
	['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
	
* range([start,] stop[[, step]])	�غc�Ʀr�ǦC,��ƨ�stop�ɪ�������

	�Plist()�X�Υi�Φ��C��
	
	>>> list(range(10))				#�u���@�ӼƮ��q�{��stop, start�q�{��0, step�q�{��1
	[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

	>>> list(range(5,10))			#��ӼƮɤ��O�q�{��start, stop, step�q�{��1
	[5, 6, 7, 8, 9]

	>>> list(range(5, 20, 2))		#�T�Ӽ�
	[5, 7, 9, 11, 13, 15, 17, 19]

	* �C��Y�Ӥj�|�ɭPMemoryError��OverflowError
	>>>list(range(10**100))
	OverflowError

**�i��**

* �C����ɦ� list comprehension

	* for�j��

	�Q��for�j��i�b[]���إߦC��

	>>>cubes = [i**3 for i in range(5)]
	>>>cubes
	[0, 1, 8, 27, 64]

	* if���z

	�Q��if���z�i�z�露��
	
	>>>evens=[i**2 for i in range(10) if i**2 % 2 == 0]
	>>>evens
	[0, 4, 16, 36, 64]


# �r��P�C�����ഫ����k

	��k(method)�O���ޥ����Oclass�������, �b���O�ޥ�<class 'list'>�����

* *string*.split(*["element"]*)		�r����C�� ,�N�r��̿�J��������

	>>> str1 = 'hello world app123'
	>>> str1.split()					#�Y����J����,�h�q�{���Ů�
	['hello', 'world', 'app123']
	>>> str1.split(' ')				
	['hello', 'world', 'app123']

	>>> str2 = 'hello.world.app123'
	>>> str2.split('.')					#��J�����|�Q����
	['hello', 'world', 'app123']

* 'element'.join(list)				�C����r��,�H��J�������j�C������

	>>> ''.join(['hello','world','app123'])		#�Y����J����,�h�q�{���L
	'helloworldapp123'

	>>> '.'.join(['hello','world','app123'])
	hello.world.app123'

# �������

* len(*list*)		Ū���C��**�����Ӽ�**

* max(*list*)		Ū���C��**�̤j��**
	
* min(*list*)		Ū���C��**�̤p��**

* sum(*list*)		�X�p�C�����Ʀr

* sorted(iterable, cmp=None, key=None, reverse=False)	�H�C��Φ��^�ǧǦC�Ƨǫ᪺��,��ǦC�����v�T

	iterable -- �i�|�N��H�C
	cmp -- �������ơA�o�Ө㦳��ӰѼơA�Ѽƪ��ȳ��O�q�i�|�N��H�����X�A����ƥ�����u���W�h���A�j��h��^1�A�p��h��^-1�A����h��^0�C
	key -- �D�n�O�ΨӶi�����������A�u���@�ӰѼơA���骺��ƪ��ѼƴN�O���۩�i�|�N��H���A���w�i�|�N��H�����@�Ӥ����Ӷi��ƧǡC
	reverse -- �ƧǳW�h�Areverse = True ���� �A reverse = False �ɧǡ]�q�{�^

# ������k

* list.append(obj)	�b�C�����K�[�s����

* list.count(obj)	�έp�Y�Ӫ���b�C���X�{����

* list.extend(seq)	�b�C�����K�[�s�C��

	�Pappend�����P:append�|�N�s�C������@�Ӥ����[�J�ؼЦC��,��extend�|�N�s�C����������X�å[�J�ؼЦC��

* list.index(obj)	��X�ؼЪ��󪺯��޼�

* list.insert(index, obj)	�b���޼ƪ���m���J����

* list.pop(obj = list[-1])	�����C�����@�Ӫ���(�q�{���̫�@��),�æ^�ǸӪ��󤺮e

* list.remove(obj)	�����C�����Ĥ@�ӲŦX������

* list.reverse()	�N�C��ƦC�ϦV

* list.sort(cmp=None, key=None, reverse=False)		�N��C��Ƨ�

	cmp -- �������ơA�o�Ө㦳��ӰѼơA�Ѽƪ��ȳ��O�q�i�|�N��H�����X�A����ƥ�����u���W�h���A�j��h��^1�A�p��h��^-1�A����h��^0�C
	key -- �D�n�O�ΨӶi�����������A�u���@�ӰѼơA���骺��ƪ��ѼƴN�O���۩�i�|�N��H���A���w�i�|�N��H�����@�Ӥ����Ӷi��ƧǡC
	reverse -- �ƧǳW�h�Areverse = True ���� �A reverse = False �ɧǡ]�q�{�^

* list.clear()	�M�ŦC��

* list.copy()	�ƻs�C��





