# ���X(set)�򥻤���

* �H��A��{}���, �èϥγr��,�Ϲj����, �O�@�ӵL�ǥB�����Ƥ������ǦC

	>>> set1 = { 123, "abc", True, 123}
	>>> set1
	{True, 123, 'abc'}

* �Ŷ��X�Hset()���,�ëD{ }

	>>> type(set())
	<class 'set'>
	>>> type({})
	<class 'dict'>

* ���i�ϥί��޼�(index)�ǻ��䤤������

* ���i�Φ��_�����c

* ���X���i�ۥ[�έ��H���

* ���X�O�i�ܪ�,���ݳz�L��k

# ����r�B��

* in		�T�{�����ζ��X�O�_�b���X��

* not in	�T�{�����ζ��X�O�_���b���X��

# �Q�Ψ�ƧΦ��C��

* set([iterable])		�N��J�������ର���X, ����i�H�O�i�|�N��H

	��J�r��ɷ|�Φ��r�������X
	
	>>> set('apple')
	{'l', 'e', 'a', 'p'}

	��J�C��Τ��թζ��X�ɷ|�Φ����������X

	>>> set([123,'abc',123])
	{'abc', 123}
	>>> set((123,'abc',123))
	{'abc', 123}
	>>> set({123,'abc',123})
	{'abc', 123}

	��J�r��ɷ|�Φ��䪺���X

* range([start,] stop[[, step]])

	�Pset()�X�Υi�Φ����X
	
	>>> set(range(10))
	{0, 1, 2, 3, 4, 5, 6, 7, 8, 9}

**�i��**

* ���X���ɦ� set comprehension

	* for�j��

	�Q��for�j��i�b{}���إ߶��X
	
	>>> cubes = {i**3 for i in range(5)}
	>>> cubes
	{0, 1, 64, 8, 27}


# �B��l

	�ԲӤ��e�ѷ�[����](https://zh.wikipedia.org/wiki/%E9%9B%86%E5%90%88%E8%AE%BA)

	set1 = {1, 2, 3, 4, 5, 6}
	set2 = {4, 5, 6, 7, 8, 9}

	>>>print(set1 | set2)	#�p��
	{1, 2, 3, 4, 5, 6, 7, 8, 9}
	>>>print(set1 & set2)	#�涰
	{4, 5, 6}
	>>>print(set1 - set2)	#�t��
	{1, 2, 3}
	>>>print(set2 - set1)	#�t��
	{8, 9, 7}
	>>>print(set1 ^ set2)	#��ٮt��
	{1, 2, 3, 7, 8, 9}

# �������

* len(*set*)		Ū�����X**�����Ӽ�**

* max(*set*)		Ū�����X��**�̤j��**
	
* min(*set*)		Ū�����X��**�̤p��**

* sum(*set*)		�X�p���X�����Ʀr

* frozenset([iterable])	�N�ؼй�H�إߦ����i�ܪ����X

# ������k

* set.add(obj)										�N����[�J���X��,����u�i�H�O��@����,�Y���s�b�h���i��ʧ@

* set.update(obj)									�N����[�J���X��,����i�H�O��@����,�r��,�C��,����,���X,�r��,�����i���_�����c,�Y�s�b�h���i��ʧ@

	��J��L���c�ɷ|�N�䤤��������X

* set.remove(obj)									�N����q���X������,����u�i�H�O��@����,�Y���s�b�h�o��KeyError

* set.discard(obj)									�N����q���X������,����i�H�O��@�����ζ��X,�Y���s�b�h���i��ʧ@

* set.pop()											�H���N�@����q���X������

* set.clear()										�M�Ŷ��X

* set.copy()										��h�ƻs���X���e

* set.union(set1[, set2...])						�^�ǥؼж��X�P��L���X���p��

* set.intersection(set1[, set2...])					�^�ǥؼж��X�P��L���X���涰

* set.intersection_update(set1[, set2...])			�ؼж��X�ܧ󬰻P��L���X���涰,���^��

* set.difference(set1[, set2...])					�^�ǥؼж��X�P��L���X���t��

* set.difference_update(set1[, set2...])			�ؼж��X�ܧ󬰻P��L���X���t��,���^��

* set.symmetric_differenceset1[, set2...]()			�^�ǥؼж��X�P��L���X����ٮt��

* set.symmetric_difference_update(set1[, set2...])	�ؼж��X�ܧ󬰻P��L���X����ٮt��,���^��

* set.isdisjoint(set1)								�P�_�ؼж��X�P��L���Xset1�O�_�]�t�ۦP����,�Y�S���h�^��True,�_�h�^��False

* set.issubset(set1)								�P�_��L���Xset1�O�_�]�t�ؼж��X���Ҧ�����,�Y���h�^��True,�_�h�^��False

* set.issuperset()									�P�_�ؼж��X�O�_�]�t��L���Xset1���Ҧ�����,�Y���h�^��True,�_�h�^��False




