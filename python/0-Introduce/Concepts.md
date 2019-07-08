# 註解 comment
	使用#來註解
	可跨行

# Python 的關鍵字與識別字
## 關鍵字 keyword
'''
	False|	class|		finally|	is|			return
	None|	continue|	for|		lambda|		try
	True|	def|		from|		nonlocal|	while
	and|	del|		global|		not|		with
	as|		elif|		if|			or|			yield
	assert|	else|		import|		pass|	
	break|	except|		in|			raise|
'''
	種類	關鍵字
	常數|	False None True
	運算子|	and del in is lambda not or
	簡單陳述|	as assert break continue from global import nonlocal pass raise return yield
	複合陳述|	else elif except finally for if try while with
	定義|	class def

## 識別字 identifier
'''
	_*
	__*__
	__*
'''

# 縮排 indentation
	不可隨意縮排,否則易導致錯誤,如IndentationError

# 運算子 operator
	* 算術運算子 arithmetic operator
	運算子	功能	範例
	+	加	a + b
	-	減	a - b
	*	乘	a * b
	**	指數	a ** b
	/	除	a / b
	//	整數除法	a // b
	%	取餘數	a % b

	* 位移運算子 shifting operator
	<<	向右位移	a << n
	>>	向左位移	a >> n

	* 位元運算子 bitwise operator
	&	位元且	a & b
	|	位元包含或	a | b
	^	位元互斥或	a ^ b
	~	位元相反	~a
	* 關係運算子 comparison operator
	<	小於	a < b
	>	大於	a > b
	<=	小於等於	a <= b
	>=	大於等於	a >= b
	==	相等	a == b
	!=	不相等	a != b
	* 指派運算子 assignment operator
	=	指派	a = b
	+=	相加同時指派	a += b
	-=	相減同時指派	a -= b
	*=	相乘同時指派	a *= b
	**=	取指數同時指派	a **= b
	/=	相除同時指派	a /= b
	/=	整數相除同時指派	a //= b
	%=	取餘數同時指派	a %= b
	&=	位元且同時指派	a &= b
	^=	位元互斥或同時指派	a ^= b
	|=	位元包含或同時指派	a |= b
	<<=	向左位移同時指派	a <<= b
	>>=	向右位移同時指派	a >>= b

# 分隔符號 delimiter
	(	)	[	]	{	}
	,	:	.	;	@	=
	+=	-=	*=	/=	//=	%=
	&=	|=	^=	<<=	>>=	**=

# 字面常數 literal
	* 字串字面常數
	* 字節字面常數
	* 整數字面常數
	* 浮點數字面常數
	* 複數字面常數
	* 串列字面常數
	* 序對字面常數
	* 字典字面常數
	* 集合字面常數