# ǰ��
	
	* ��*object*����ݔ��������׃��

# �͑B�D׃����
* int(*object [, base]*)	Ŀ������D������

	* Ŀ�����������"�������ִ�", "���c��", "���ֵ"

	* base�����M��,��Ŀ��������ִ���ʹ��,Ĭ�J��ʮ�M��

* float(*object*)	Ŀ������D�ɸ��c��

* complex(*object [,imag]*)	Ŀ������D���}��

* str(*object*)	Ŀ������D���ִ�

* hex(*object*)	Ŀ������D��ʮ���M�Ƶ��ִ�

* oct(*object*)	Ŀ������D�ɰ��M�Ƶ��ִ�

* chr(*object*)	Ŀ�����(ASCII�a)�D�Ɍ�������Ԫ

* ord(*object*) Ŀ�����(��Ԫ)�D�Ɍ�����ASCII�a


# ӍϢ�xȡ����

* bool(*object*)	�Д������**���ֵ**

* len(*object*)		�xȡĿ�����**�L��**

* type(*object*)	�xȡĿ�����**�͑B**

*  eval(*expression*)	�xȡ�ִ��͑B�ı��_ʽ�ĽY��

# �ִ����P����

* format method

	ʹ��'{*[index]*}'.format(*object*)����ʽ�Ɍ���������ִ���,index����format()��*object*�����,�]�Ќ��t����Ĭ�J�������
	
	>>>msg = "Numbers: {0} {1} {2}". format(4, 5, 6)
	>>>msg
	'Numbers: 4 5 6'

	index�ɞ�ָ������(argument)
	
	>>>a = "{x}, {y}".format(x=5, y=12)
	>>>a
	5, 12



















