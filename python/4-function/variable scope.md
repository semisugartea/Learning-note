# �ܼƧ@�ΰ� variable scope

	�ܼƪ��@�ΰ�|�M�w�ܼƥi�v�T���d��,�bPython�@�@�����|��,���O�O
	
	* Local			�����@�ΰ�
	* Enclosing		���]��ƥ~����Ƥ�
	* Global		�����@�ΰ�
	* Built-in		���ا@�ΰ�

	��{�Ǧb�I�s�ܼƮ�,�|�q���ӥ~��,�Y:Local�䤣��N��Enclosing��,�A�䤣��N��Global��,�A�䤣��N��Built-in��

	apple = 1			#�����@�ΰ�
	def out():
		banana = 2		#���]��ƥ~����Ƥ�
		def in():
			cat = 3		#�����@�ΰ�

	���ا@�ΰ�O���z�L�зǼҲ�builtin�����e�إߪ��@�ΰ�,�i�z�Ldir()�d��

	>>> dir(__builtins__)
	['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'ZeroDivisionError', '_', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']

# global

	* �̧@�ΰ쪺�W�h,�������@�ΰ�i�H�I�s�~���@�ΰ쪺�ܼ�,�Y�ܼƬO�i�ܪ�,�h���ܥ~�����ܼ�;�Y�ܼƬO���i�ܪ�,�h���i���s����.

�i��:
	��J:
	a = [1]
	def f1():
		a.append(1)
		print(a)

	f1()
	print(a)

	��X:
	[1, 1]
	[1, 1]

���i��:
	��J:
	a = 1
	def f1():
		a += 1
		print(a)

	f1()

	��X:
	Traceback (most recent call last):
	  File "python.py", line 6, in <module>
		f1()
	  File "python.py", line 3, in f1
		a += 1
	UnboundLocalError: local variable 'a' referenced before assignment

	* �ϥ�global�ŧi�����ܼƦW��,�i���s�����ç��ܥ~���ܼ�

	��J:
	a = 1
	def f1():
		global a
		a += 1
		print(a)

	f1()
	print(a)

	��X:
	2
	2

# nonlocal

	�Y�O�n�����@�ΰ�ϥ�Enclosing�@�ΰ쪺�ܼ�,�i�ϥ�nonloacal

	��J:
	def f1():
		a = 1
		def f2():
			nonlocal a
			a = 2
			print(a)
		f2()
		print(a)

	f1()

	��X:
	2
	2

























