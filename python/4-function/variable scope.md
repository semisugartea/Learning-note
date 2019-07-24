# 變數作用域 variable scope

變數的作用域會決定變數可影響的範圍,在Python一共分為四種,分別是
	
	* Local			局部作用域
	* Enclosing		閉包函數外的函數中
	* Global		全局作用域
	* Built-in		內建作用域

當程序在呼叫變數時,會從內而外找,即:Local找不到就往Enclosing找,再找不到就往Global找,再找不到就往Built-in找

	apple = 1			#全局作用域
	def out():
		banana = 2		#閉包函數外的函數中
		def in():
			cat = 3		#局部作用域

內建作用域是指透過標準模組builtin的內容建立的作用域,可透過dir()查詢

	>>> dir(__builtins__)
	['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'ZeroDivisionError', '_', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']

# global

依作用域的規則,內部的作用域可以呼叫外部作用域的變數,若變數是可變的,則改變外部的變數;若變數是不可變的,則不可重新指派.

可變:

	輸入:
	a = [1]
	def f1():
		a.append(1)
		print(a)

	f1()
	print(a)

	輸出:
	[1, 1]
	[1, 1]

不可變:

	輸入:
	a = 1
	def f1():
		a += 1
		print(a)

	f1()

	輸出:
	Traceback (most recent call last):
	  File "python.py", line 6, in <module>
		f1()
	  File "python.py", line 3, in f1
		a += 1
	UnboundLocalError: local variable 'a' referenced before assignment

	* 使用global宣告全局變數名稱,可重新指派並改變外部變數

	輸入:
	a = 1
	def f1():
		global a
		a += 1
		print(a)

	f1()
	print(a)

	輸出:
	2
	2

# nonlocal

若是要局部作用域使用Enclosing作用域的變數,可使用nonloacal

	輸入:
	def f1():
		a = 1
		def f2():
			nonlocal a
			a = 2
			print(a)
		f2()
		print(a)

	f1()

	輸出:
	2
	2



