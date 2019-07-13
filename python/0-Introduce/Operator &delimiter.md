# 運算符 operator
* 算術運算子 arithmetic operator

	|運算子	|功能	|範例|
	| ---------- | :-----------:  | :-----------: |
	|+	|加	|a + b|
	|-	|減	|a - b|
	|*	|乘	|a * b|
	|**	|指數	|a ** b|
	|/	|除	|a / b|
	|//	|整數除法	|a // b|
	|%	|取餘數	|a % b|

* 位移運算子 shifting operator

	|運算子	|功能	|範例|
	| ---------- | :-----------:  | :-----------: |
	|<<	|向右位移	|a << n|
	|>>	|向左位移	|a >> n|

* 位元運算子 bitwise operator

	|運算子	|功能	|範例|
	| ---------- | :-----------:  | :-----------: |
	|&	|位元且	|a & b|
	|\|	|位元包含或	|a \| b|
	|^	|位元互斥或	|a ^ b|
	|~	|位元相反	|~a|
	
* 關係運算子 comparison operator

	|運算子	|功能	|範例|
	| ---------- | :-----------:  | :-----------: |
	|<	|小於	|a < b|
	|>	|大於	|a > b|
	|<=	|小於等於	|a <= b|
	|>=	|大於等於	|a >= b|
	|==	|相等	|a == b|
	|!=	|不相等	|a != b|
	
* 指派運算子 assignment operator

	|運算子	|功能	|範例|
	| ---------- | :-----------:  | :-----------: |
	|=	|指派	|a = b|
	|+=	|相加同時指派	|a += b|
	|-=	|相減同時指派	|a -= b|
	|*=	|相乘同時指派	|a *= b|
	|**=	|取指數同時指派	|a **= b|
	|/=	|相除同時指派	|a /= b|
	|/=	|整數相除同時指派	|a //= b|
	|%=	|取餘數同時指派	|a %= b|
	|&=	|位元且同時指派	|a &= b|
	|^=	|位元互斥或同時指派	|a ^= b|
	|\|=	|位元包含或同時指派	|a \|= b|
	|<<=	|向左位移同時指派	|a <<= b|
	|>>=	|向右位移同時指派	|a >>= b|
	
# 分隔符號 delimiter

|分隔符號	|功能	|
| ---------- | :-----------:  |
|( )	|小括弧圍住的運算式會優先計算，函數 (function) 也用小括弧圍住參數列 (parameter list)	|
|[ ]	|序列型態 (sequence type) 的索引符號，或用作定義串列 (list)	|
|{ }	|用作定義字典 (dictionary)	|
|,	|同一行中分隔多個運算式	|
|:	|控制陳述條件 (condition) 後的分隔符號	|
|.	|用為存取物件的方法 (method) 或屬性 (attribute)	|
|;	|可作為單行程式結束的符號，也可不用	|
|@	|用作函數或類別 (class) 定義的特殊標記	|

# 運算符優先序 Operator Precedence
* 部分運算符要到後面才講

|Operators		|Description|
|-----------------------------------------------		|---------------------------------|
|{ }			|Parentheses (grouping)|
|-----------------------------------------------		|---------------------------------|
|f(args…)		|Function call|
|-----------------------------------------------		|---------------------------------|
|(expressions…)		|Binding or tuple display|
|[expressions…]		|list display|
|{key: value…}		|dictionary display|
|{expressions…}		|set display|
|-----------------------------------------------		|---------------------------------|
|x[index:index]		|Slicing|
|x[index]		|Subscription|
|x.attribute		|Attribute reference|
|-----------------------------------------------		|---------------------------------|
|await x		|Await expression|
|-----------------------------------------------		|---------------------------------|
|**			|Exponent|
|-----------------------------------------------		|---------------------------------|
|~x			|Bitwise not|
|+x, -x			|Positive, negative|
|-----------------------------------------------		|---------------------------------|
|*, /, %		|Product, division, remainder|
|-----------------------------------------------		|---------------------------------|
|+, –			|Addition, subtraction|
|-----------------------------------------------		|---------------------------------|
|<<, >>			|Shifts left/right|
|-----------------------------------------------		|---------------------------------|
|&			|Bitwise AND|
|-----------------------------------------------		|---------------------------------|
|^			|Bitwise XOR|
|-----------------------------------------------		|---------------------------------|
|\|			|Bitwise OR|
|-----------------------------------------------		|---------------------------------|
|in, not in, is,is not, <, <=, >, >=, <>, !=, ==		|Comparisons, membership, identity|
|-----------------------------------------------		|---------------------------------|
|not x			|Boolean NOT|
|-----------------------------------------------		|---------------------------------|
|and			|Boolean AND|
|-----------------------------------------------		|---------------------------------|
|or			|Boolean OR|
|------------------------------------------------		|---------------------------------|
|if- else		|Conditional expression|
|-----------------------------------------------		|---------------------------------|
|lambda			|Lambda expression|