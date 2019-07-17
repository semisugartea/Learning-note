# 膀セざ残

	ㄧ计(function)琌贺跋办絏,讽ㄤ砆㊣穦磅︽ず甧,挡穦祘┪肚,膀セΑ:
	
	def *function_name*(*parameter(s)*):
		statement

1. ︽ゲ斗def秨繷,い丁ㄧ计,()ず﹚竡把计,0┪,硆腹跋筳,程玙腹挡Ю
2. Ω︽ゲ斗秨繷罽逼,玥ぃㄧ计い

# 把计(parameter)㎝ま计(argument)

* 把计琌ㄧ计ず┮﹚竡跑计,ㄤ跑计硄盽礚猭ㄧ计跋办ㄏノ

	块:
	def plus(parameter):
	   parameter += 1
	   print(parameter)
	plus(1)
	print(parameter)

	块:
	Traceback (most recent call last):
	  File "python.py", line 5, in <module>
		print(parameter)
	NameError: name 'parameter' is not defined

* ま计琌场肚ㄧ计讽把计,讽砆ま跑计琌跑(mutable),ㄤ穦э跑

ㄒ1:
	块:
	def plus(parameter):
	   parameter += 1
	a = 1
	plus(a)
	print(a)

	块:
	1
ㄒ2:
	块:
	def plus(parameter):
	   parameter.append(1)
	a = []
	plus(a)
	print(a)

	块:
	[1]

# 把计㎝ま计篈

* ゲ惠把计 required parameter

	砞﹚ㄧ计璹把计,㊣ㄧ计,把计ゲ惠Τ莱,玥穦厨岿,嘿ゲ惠把计

	块:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1)

	块:
	Traceback (most recent call last):
	  File "python.py", line 5, in <module>
		printwords(1)
	TypeError: printwords() missing 1 required positional argument: 'b'


* 闽龄ま计 keyword argument

	祘い㊣ㄧ计,璝ノ把计砞﹚ま计,玥嘿闽龄ま计,ま计嘿,τ獶抖

	块:
	def printwords(a, b):
		print("a:", a)
		print("b:", b)

	printwords(1, 2)
	printwords(b=4, a=3)

	块:
	a: 1
	b: 2
	a: 3
	b: 4

* 纐粄把计 default parameter

	砞﹚把计砞﹚纐粄,嘿纐粄把计,讽ㄧ计砆㊣,璝⊿Τま计,玥ㄏノ纐粄把计

	块:	
	def plus(a=2, b=2):
		print("a+b:", a+b)

	plus()
	plus(a=3)
	plus(3,3)

	块:
	a+b: 4
	a+b: 5
	a+b: 6

* ぃ﹚计秖把计

	璝块ま计计秖把计计秖,把计玡琍腹\*,玥ま计穦じ舱よΑま
	璝把计玡ㄢ琍腹,玥ま计穦ㄥよΑま
	
	块:
	def printwords(x, *y, **z):
		print("x:", x)
		print("y:", y)
		print("z:", z)

	printwords(10,20,30,'apple','banana', cat=10, dog='egg')

	块:
	x: 10
	y: (20, 30, 'apple', 'banana')
	z: {'cat': 10, 'dog': 'egg'}

# 肚 return

	ㄧ计いㄏノreturn挡ㄧ计肚,纐粄None,τNone⊿Τヴン

# ㄧ计 pure function

* ㄧ计琌ㄧ计い┮Τ跑计の把计琌跋办┦,磅︽ぃ紇臫跑计

	def pure(x, y):
	  add = x + y
	  return add*x + y

* ぃㄧ计(impure function)琌ㄧ计钡まノ跑计,旧璓磅︽紇臫跑计

	list1 = [1,2]

	def impure(x):
	  some_list.append(x)

* ㄧ计疭翴

	1. 甧瞶秆籔代刚
	2. 磅︽Τ瞯
	3. 籔祘キ︽笲衡

# ㄧ计ンて

	Pythonい,ㄧ计妓砆讽ンㄏノ

1. ㄧ计肚患
	
	盢ㄧ计倒跑计,ㄏㄤ跑Θㄧ计

	块:
	def add(a, b):
	return a+b

	plus = add
	print(plus(1,2))
	
	块:
	3

2. 讽把计

	ㄧ计い盢把计讽ㄧ计,ㄏ眔ㄧ计まㄤㄧ计

	块:	
	def multiply(x, y):
	  return x*y

	def add(func, x, y):
	  return func(x, y) + func(x, y)

	a = 3
	b = 7
	print(add(multiply, a, b))

	块:
	42







