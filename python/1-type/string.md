## �r��	string

* �H�@���޸�''�Τ@�����޸�""��ܦr��A�C�@�Ӧr�Q�٬��r��(character)

* ����r�� escape character

	�b�ϱ׽u\�᭱�[�W�S�w�r���i�Φ�����r���A���ɤG�̵��@�P�@�r���A�Q��print()�i���S��ĪG(��1.3����)�A�ӥ]�t����r�����r��٬�����ǦC(escape sequence)
	
|����ǦC�@�@ |�@�@�ĪG
| ---------- | :-----------:  
|�@\a �@�@�@�@|ĵ�ܭ�(Alert bell)
|�@\b �@�@�@�@|�˰h�@��(Backspace)
|�@\n �@�@�@�@|����(New line)
|�@\r �@�@�@�@|�^�k�Ӧ�_�l�I(Carriage return)
|�@\t �@�@�@�@|��������(Tab�A�۷�����L��Tab��)
|�@\v �@�@�@�@|��������(Vertical tab)
|�@\\ �@�@�@�@|�L�X�ϱ׽u(Backslash)
|�@\' �@�@�@�@|�L�X��޸�(Single quote)
|�@\" �@�@�@�@|�L�X���޸�(Double quote)
* �r��i�ۥ[,���i�۴�άۭ�

* �r��i�P��Ƭۭ�,�Ϧr�꭫��

	>>> 'hello' * 3
	'hellohellohello'
	>>> 'sam'*(-1)	#�s�έt�Ʒ|�ܦ��Ŧr��
	''
* �r��P�Ʀr����ۥ[

* �r��i�ί��޼�(index)����ܲĴX�Ӧr��[*index*],��1�Ӧr���H[0]���

* �i��[::]����(slice)�r��,�䤤�t�N��[�_�l:���I:�B��]
			#[:::]������
			#'.'���@�Ӧr��

* in
	�ϥ�in�i�T�{�r���O�_�b�r�ꤤ
	>>> 'he' in 'hello'
	True

* �t�Ƭ��˵ۺ�

# �r�������ƩΤ�k

* *string*.format(*object*)			�ϥ�'{*index*}'.format(*object*)���Φ��i�N�����J�r�ꤤ,index�N��format()��*object*������,�S���g�h�|���q�{���Ƕ�J
	
	>>>msg = "Numbers: {0} {1} {2}". format(4, 5, 6)
	>>>msg
	'Numbers: 4 5 6'

	index�i�����w�Ѽ�(argument)
	
	>>>a = "{x}, {y}".format(x=5, y=12)
	>>>a
	5, 12

* *string*.replace(str1,str2)		�^�ǱNstr1������str2�᪺�r��

	>>> "Hello ME".replace("ME", "world"))
	"Hello world"

* *string*.startswith(str)			�P�_�ؼЦr��O�_�qstr�}�l,�Y�O�h�^��True,�_�h�^��False

	>>> "This is a sentence.".startswith("This")
	True

* *string*.endswith(str)			�P�_�ؼЦr��O�_�Hstr����,�Y�O�h�^��True,�_�h�^��False

	>>> "This is a sentence.".endswith("sentence.")
	True

* *string*.upper()					�^�ǱN�ؼЦr�ꪺ�r���ন�j�g�᪺�r��

	>>> "This is a sentence.".upper())
	"THIS IS A SENTENCE."

* *string*.lower()					�^�ǱN�ؼЦr�ꪺ�r���ন�p�g�᪺�r��

	>>> "AN ALL CAPS SENTENCE".lower()
	"an all caps sentence"


**�P�C���������k**

* *string*.split(*["element"]*)		�r����C�� ,�N�r��̿�J��������

* 'element'.join(list)				�C����r��,�H��J�������j�C������