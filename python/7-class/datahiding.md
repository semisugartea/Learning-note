# 基本介紹

在python中,透過特殊的處理方式,可以使主程序無法讀取目標物件的內容

# 弱方法

* 透過在物件或屬性名稱前加上**一個**下劃線,可以使物件或屬性無法被import * 引入,但仍可在自身的程序中使用

test.py:

    def public_func():
      print("public")

    def _private_func():
      print("private")

輸入:

    from test import *

    def _not_private_func():
      print("not private")

    try:
      public_func()
    except:
      print('result1 fail')
    else:
      print('result1 succeed')

    try:
      _private_func()
    except:
      print('result2 fail')
    else:
      print('result2 succeed')

    try:
      _not_private_func()
    except:
      print('result3 fail')
    else:
      print('result3 succeed')

輸出:

    public
    result1 succeed
    result2 fail
    not private
    result3 succeed

* 若直接輸入名稱仍可被import

輸入:

    from test import _private_func

    try:
      _private_func()
    except:
      print('result fail')
    else:
      print('result succeed')

輸出:

    private
    result succeed

* 也能用在test.py中使用__all__()方法使其被import * 引入

test.py:

    __all__  = ['public_func', '_private_func']

    def public_func():
      print("public")

    def _private_func():
      print("private")

輸入:

    from test import *

    try:
      _private_func()
    except:
      print('result fail')
    else:
      print('result succeed')

輸出:

    private
    result succeed

# 強方法

* 透過在物件或屬性名稱前加上**一個**下劃線,可以使物件或屬性無法被輕易從類別外讀取，以下為例

輸入：

    class fruit:
        __apple = 'red'
        def show(self):
            print(self.__apple)

        def __hide(self):
            print('hide')

    a = fruit()

    try:
        print(a._fruit__apple)
        print(a.__apple)
    except:
        print('result1 fail')
    else:
        print('result1 succeed')

    try:
        a.show()
    except:
        print('result2 fail')
    else:
        print('result2 succeed')

    try:
        a._fruit__hide()
        a.__hide()
    except:
        print('result3 fail')
    else:
        print('result3 succeed')

輸出：

    red
    result1 fail
    red
    result2 succeed
    hide
    result3 fail

1. 在result1中，透過*物件名._類別名__屬性名* 可以讀取內容，但*物件名.__屬性名*無法讀取內容
2. 在result2中，類別自身的方法可讀取自身的隱藏屬性
3. 在result3中，透過*物件名._類別名__方法名*可以執行方法，但*物件名.__方法名*無法執行方法











