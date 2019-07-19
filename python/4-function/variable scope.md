# 跑计ノ办 variable scope

	跑计ノ办穦∕﹚跑计紇臫絛瞅,Pythonだ贺,だ琌
	
	* Local			Ы场ノ办
	* Enclosing		超ㄧ计ㄧ计い
	* Global		Ыノ办
	* Built-in		ずノ办

	讽祘㊣跑计,穦眖ずτт,:Localтぃ碞┕Enclosingт,тぃ碞┕Globalт,тぃ碞┕Built-inт

	apple = 1			#Ыノ办
	def out():
		banana = 2		#超ㄧ计ㄧ计い
		def in():
			cat = 3		#Ы场ノ办

	ずノ办琌硓筁夹非家舱builtinず甧ミノ办,硓筁dir()琩高

	>>> dir(__builtins__)
	['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'ZeroDivisionError', '_', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']

# global

	* ㄌノ办砏玥,ず场ノ办㊣场ノ办跑计,璝跑计琌跑,玥э跑场跑计;璝跑计琌ぃ跑,玥ぃ穝.

跑:
	块:
	a = [1]
	def f1():
		a.append(1)
		print(a)

	f1()
	print(a)

	块:
	[1, 1]
	[1, 1]

ぃ跑:
	块:
	a = 1
	def f1():
		a += 1
		print(a)

	f1()

	块:
	Traceback (most recent call last):
	  File "python.py", line 6, in <module>
		f1()
	  File "python.py", line 3, in f1
		a += 1
	UnboundLocalError: local variable 'a' referenced before assignment

	* ㄏノglobalЫ跑计嘿,穝э跑场跑计

	块:
	a = 1
	def f1():
		global a
		a += 1
		print(a)

	f1()
	print(a)

	块:
	2
	2

# nonlocal

	璝琌璶Ы场ノ办ㄏノEnclosingノ办跑计,ㄏノnonloacal

	块:
	def f1():
		a = 1
		def f2():
			nonlocal a
			a = 2
			print(a)
		f2()
		print(a)

	f1()

	块:
	2
	2

























