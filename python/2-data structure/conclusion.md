# �e��

* ���`�N�r��,�C��,����,���X,�r��@�_�Q��
* �ǦC�O�������Ǫ��������ƾڵ��c,�i�H�O�C��,���ջPrange(),�U�q�W�n�D���������P�@���A

# �S�x���

			|�r��	|�C��	|����	|���X	|�r��
----		|----	|----	|----	|----	|----
�аO�覡	|''		|[,]	|(,)	|{,}	|{:}
��			|''		|[]		|()		|set()	|{}
�i�ܩ�		|�_		|�i		|�_		|�i		|�i
�ϥ�+�ۥ[	|�i		|�i		|�i		|�_		|�_
�ϥ�*���W	|�i		|�i		|�i		|�_		|�_
�_�����c	|�_		|�i		|�i		|�_		|�_
����		|[index]|[index]|[index]|�L		|[key]
����		|�i		|�i		|�i		|�_		|�_
in�B��		|�i		|�i		|�i		|�i		|�i		
���ɦ�		|�_		|�i		|�_		|�i		|�_

# �ϥήɾ�

	�r��:��@�ƾګ��A
	�C��:�g�`�ܧ�B�ݤ������Ʈɨϥ�
	����:���ܧ�B�ݤ������Ʈɨϥ�
	���X:�g�`�ܧ�����n�������Ʈɨϥ�
	�r��:�ݧQ�Ϋ��w���������ɨϥ�
	
# ��]	packing

* ��������ܼƦh�l����������,�|�Φ�����(tuple),�٬�tuple packing

	>>> tup1 = "one", "two", "three"
	>>> tup1
	('one', 'two', 'three')

* ��ǦC�����h���ܼƮ�,�|���O�o���������,�٬���], ��̼ƶq���P�|��ValueError
	
	>>>a, b, c = (1, 2, 3)
	>>>a
	1
	>>>b
	2
	>>>c
	3
	
	* �i�b�䤤�@���ܼƫe�[�P��(*),�h���ܼƷ|�����h�l������,�����i����ӥ[�P�����ܼ�
	
	>>>a, b, *c, d = [1, 2, 3, 4, 5, 6, 7, 8, 9]
	>>>a
	1
	>>>b
	2
	>>>c
	[3, 4, 5, 6, 7, 8]
	>>>d
	9


# �@�P���

* del obj��	del(obj)				�R���ؼЪ���,�C��P�r��i��W�R���䤤������

* all(iterable)						�P�_�O�_�Ҧ������Ҭ�True

* any(iterable)						�P�_�O�_�����󤸯���True

* enumerate(sequence, [start=0])	�C�|�ǦC��������,�H(number,element)���Φ��t��,numeber�qstart��_,start�q�{��0,�^�ǰ_�l�t�諸�����}

* len(iterable)						�^�ǥؼй�H�������Ӽ�

* max(iterable)						�^�ǥؼй�H���̤j����,�����ݦP���A,�r��h����䪺�j�p

* min(iterable)						�^�ǥؼй�H���̤p����,�����ݦP���A,�r��h����䪺�j�p

* sum(sequence)						�^�ǥؼЧǦC���`��

* sorted(iterable, cmp=None, key=None, reverse=False)	�H�C��Φ��^�ǥؼй�H�������Ƨǫ᪺�ˤl,�����ݦP���A,�r��h����䪺�j�p,��ǦC�����v�T

	cmp -- �������ơA�o�Ө㦳��ӰѼơA�Ѽƪ��ȳ��O�q�i�|�N��H�����X�A����ƥ�����u���W�h���A�j��h��^1�A�p��h��^-1�A����h��^0�C
	key -- �D�n�O�ΨӶi�����������A�u���@�ӰѼơA���骺��ƪ��ѼƴN�O���۩�i�|�N��H���A���w�i�|�N��H�����@�Ӥ����Ӷi��ƧǡC
	reverse -- �ƧǳW�h�Areverse = True ���� �A reverse = False �ɧǡ]�q�{�^

# �������

* map(function, sequence)			�N�ǦC�������O�ǤJ���,�N��ƪ��^�ǭȧ@���s������,�^�Ƿs�����զ����ǦC,²�٬M�g

* filter(function, sequence)		�N�ǦC�������O�ǤJ���,�Y��Ʀ^��True�h�O�d����,�_�h����,�^�ǿz��᪺�ǦC			

* reduce(function, sequence[, initializer])		��ƶ�������ӰѼ�,���N�ǦC�e2�Ӥ����ǤJ,�A�N�^�ǭȧ@���Ĥ@�ӰѼ�,�P�ǦC���U�@�Ӥ����@�_�ǤJ���,�̫�^�ǳ̲׭�,�i�Ninitializer�@����l�Ѽ�

* zip(sequence,sequence)			�N��ǦC�����@��@���]�����ժ��Φ�,�^�ǥ]����},���]�ƻP�̵u�ǦC�������ӼƬۦP

* zip(*(zipped sequence))				�N���]�᪺���թ�],�^�Ǩ�դ�������}




