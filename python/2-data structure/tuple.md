# ����(tuple)�򥻤���

* �H��A��()���, �èϥγr��,�Ϲj

* ��A�����S�����󤸯�����C�٬��Ť���(empty tuple)

* �P�C��ۦ�,���եi�ϥί��޼�(index)�ǻ��䤤������

* �i�Φ��_�����c

* ��������ܼƦh�l����������,�|�Φ�����(tuple),�٬�tuple packing

	>>> tup1 = "one", "two", "three"
	>>> tup1
	('one', 'two', 'three')

# �P�C����

* �P�C��ۦ�,���եi�ۥ[

* �P�C��ۦ�,���եi�Q�έ��H��ƨӭ���

* �P�C��ۦ�,���եi����(slice), �P�ˬO[�_�l:���I:�B��]

* �P�C���P���O,���լO���i�ܪ�(immutable), ���B��t�פ���֥B�O�ЪŶ�����p

	>>> tup1 = ('apple', 'banana', 'cat')
	>>> tup1[2] = 'dog'
	TypeError: 'tuple' object does not support item assignment

# ����r�B��

* in	�T�{�����O�_�b���դ�

* not in	�T�{�����O�_���b���դ�

# �Q�Ψ�ƧΦ��C��

* tuple(*sequence*) �N��J���ǦC(sequence)�ର����, �ǦC�i�H�O�C��Φr�� 

* range([start,] stop[[, step]])	

	�Ptuple()�X�Υi�Φ�����

**�i��**

* ��������ɦ�(comprehension)

	�P�C���P���O, �b��A��()�ϥ�for�j���, �|�Φ�generator, �ӫD����

	>>> cubes = (i**3 for i in range(5))
	>>> type(cubes)
	<class 'generator'>
	>>> for j in cubes:
	...  print(j)
	...
	0
	1
	8
	27
	64

# �������

* len(*tuple*)		Ū������**�����Ӽ�**

* max(*tuple*)		Ū�����դ�**�̤j��**
	
* min(*tuple*)		Ū�����դ�**�̤p��**

* sum(*tuple*)		�X�p���դ����Ʀr



















