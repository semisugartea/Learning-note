# Ū�� reading

* read()��k

	�b����ܼƫ�[�W.read()�i�HŪ����󤺮e

	test.txt���e:
	applebananacatdog
	123456
	hello world
	
	��J:
	file = open("test.txt", "r")
	content = file.read()
	print(content)
	file.close()

	��X:
	applebananacatdog
	123456
	hello world

	�����y�k��read(*size*),*size*�N��Ū�����r��,�U�ҥi�ݥXŪ���u���e���^�Y��

	��J:
	file = open("test.txt", "r")
	print(file.read(5))
	print(file.read(8))
	print(file.read(13))
	print(file.read())
	file.close()

	��X:
	apple
	bananaca
	tdog
	123456
	h
	ello world

	�@�Ӥ��b�@���}�Ҥ��u��Ū���@��

	��J:
	file = open("test.txt", "r")
	file.read()
	print('read again')
	print(file.read())
	print('stop')
	file.close()

	��X:
	read again

	stop

* readline() �M readline()��k
	
	�ϥ�readline()��k�iŪ���@��
	
	��J:
	file = open("test.txt", "r")
	print(file.readline())
	print(file.readline())
	print(file.readline())
	file.close()

	��X:
	applebananacatdog

	123456

	hello world

	�ϥ�readlines()��k�iŪ���h��ëإߦC��
	
	��J:
	file = open("test.txt", "r")
	print(file.readlines())
	file.close()
	
	��X:
	['applebananacatdog\n', '123456\n', 'hello world']
	
* for�j��
	
	�ϥ�for�j��i�������
	
	��J:
	file = open("test.txt", "r")
	for i in file:
		print(i)
	file.close()
	
	��X:
	applebananacatdog

	123456

	hello world
	
# �g�J writing

* write() ��k

	�ϥ�write()��k�i�H�N()�����e�g�J���,���e�����O**�r��**
	
	��J:
	file = open("test.txt", "w")
	file.write("New things")
	file.close()

	file = open("test.txt", "r")
	print(file.read())
	file.close()
	
	��X:
	New things
	
	����test.txt�����e�O:
		New things
	�N��즳���e�|�����R����A��J�s���e
	
	write()��k�|�^�Ǽg�J�r�ꪺ�r��
	
	file = open("test.txt", "w")
	number = file.write("New things")
	print(number)
	file.close()
	
	10

