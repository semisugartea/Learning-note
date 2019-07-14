# �r��(dictionary)�򥻤���

* �H��A��{}���, �èϥγr��,�Ϲj����, �C�@�Ӥ��������A��key:value
* ���i�Φ��_�����c

	��(key)���i��,�]���i�H�O�ƭ�,�r��,�u����,����
	��(value)�i�H�O�ƭ�,�r��,�u����,����,�C��	
	=>	���i�Φ��_�����c

	>>> dict1 = {"apple": 24, "banana":61 , "cat": 58}
	>>> dict2 = {1: 2, '2':'b' , (3,3): ('c','c'), True:False , 5.5:['e',5]}

* ��A�����S�����󤸯�����C�٬��Ŧr��(empty dictionary)

* �Q����Ū���۹�������,�䤣�s�b�|��� KeyError

	>>> dict1['apple']
	24

* �r��O�i�ܪ�, �i�Q����W�[�s�������έ��s�����s����

	>>>squares = {1: 1, 2: 4, 3: "error", 4: 16,}
	>>>squares[8] = 64
	>>>squares[3] = 9
	>>>squares
	{1: 1, 2: 4, 3: 9, 4: 16, 8: 64}
	
* �Y�X�{�ۦP����, �h�|�H��̬���

* �r�夣�i�ۥ[�έ��H���

# ����r�B��

* in	�T�{�����O�_�b�䤤
	
	nums = {1: "one", 2: "two", 3: "three"}
	>>> 1 in nums
	True
	>>> "three" in nums
	False

* not in	�T�{�����O�_���b�䤤

	>>> 1 not in nums
	False
	>>> 'three' not in nums
	True

* del *dict[key]*						�����䤤������

# �Q�Ψ�ƧΦ��C��

* dict()	�N��J�������ର�r��

	�Φ������T��:
	dict(**kwarg)					**kwargs:�S��Φ�,�pkey=value
	dict(mapping, **kwarg)			mapping	:�M�g���
	dict(iterable, **kwarg)			iterable:�i�|�N��H

	>>> dict(a='one', b='two',c ='three')
	{'a': 'one', 'b': 'two', 'c': 'three'}
	>>> dict(zip(['one', 'two', 'three'], [1, 2, 3]))   # �M�g���
	{'three': 3, 'two': 2, 'one': 1} 
	>>> dict([('one', 1), ('two', 2), ('three', 3)])    # �|�N�覡
	{'three': 3, 'two': 2, 'one': 1}

# �������

* len(*dict*)		�p��r�夤�������Ӽ�

* max(*dict*)		Ū���r�夤**�̤j��*
	
* min(*dict*)		Ū���r�夤**�̤p��**

* sum(*tuple*)		�X�p�r�夤����

# ������k

* dict.clear()							�����Ҧ�����

* dict.copy()							��h�ƻs�r�夺�e	

* dict.fromkeys(seq[, value])			�Q�ο�J�r�媺��إ߷s�r��,�i�]�w��,����q�{��None

* dict.items()							�N�r�夤���C�@�Ӥ����^�Ǧ�dict_items([(key1, value1), (key2, value2),...])���Φ�

* dict.keys()							�N�r�夤���C�@����^�Ǧ�dict_keys([key1, key2, ...])���Φ�

* dict.values()							�N�r�夤���C�@�ӭȦ^�Ǧ�dict_values([value1, value2, ...])���Φ�

* dict.get(key, default=None)			Ū����J��۹諸��,�S���h�q�{��None,�i�]�w��L�^�ǭ�

* dict.setdefault(key, default=None)	Ū����J��۹諸��,�S���h���J��,����q�{��None,�i�]�w��L��

* dict.update(dict2)					�Ndict2�������[�J�ؼЦr��

* dict.pop(key[,default])				�R����۹諸�����æ^�Ǭ۹諸��,�䤣�s�b�h�^��default��,�Ydefault�Ȥ��]�w�|�ɭP�^�Ǯɵo��KeyError

* dict.popitem()						�H���R���r�夤���䤤�@�Ӥ���,�åH(key, value)���Φ��^�ǸӤ���










