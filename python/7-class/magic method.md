# 魔術方法(magic method)

Python本身有許多內建方法,在建立類別時使用這些方法可以再發生相應的情況時執行敘述,因此稱為魔術方法,其共通點在於其名稱前後都有兩個下劃線,例如最早接觸的__init__()即是魔術方法之一

# 數值運算類

* 總覽

方法名   |相應運算子   
 ------------ | ------------ 
__add__ |+
__sub__ | -
__mul__ | *
__truediv__ | /
__floordiv__ | //
__mod__ | %
__pow__ | **
__and__ | &
__xor__ | ^
__or__ | \|

* 以__add__()為例

輸入：

  class Vector2D:
    def __init__(self, x, y):
      self.x = x
      self.y = y
    def __add__(self, other):
      return Vector2D(self.x + other.x, self.y + other.y)

  first = Vector2D(5, 7)
  second = Vector2D(3, 9)
  result = first + second
  print(result.x)
  print(result.y)

輸出：

  8
  16

1. 在例子中,由__init__()建立實體,賦予兩個屬性x和y,在主程序中,先建立兩個類別Vector2D的物件first和second,當兩者相加時,執行__add__()方法,回傳結果給result,result因此成為類別Vector2D的物件
2. 方法的敘述內容沒有限定
3. first + second 等價於 first.__add__(second)

* 反運算

對於數值處理類的魔術方法,在名稱前加r可變成反運算


















