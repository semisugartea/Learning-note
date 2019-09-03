# 基本介紹

在類別中，有三個內建方法可用裝飾子，分別為classmethod、staticmethod和property

# 類別方法(classmethod)

* @classmethod可使被裝飾的方法成為類別方法，可透過類別名呼叫該方法，以下為例

輸入：

    class person:
      totalObjects=0
      def __init__(self):
        person.totalObjects += 1

      @classmethod
      def showcount(cls):
        print("Total objects: ",cls.totalObjects)

    p1=person()
    p2=person()
    person.showcount()
    p1.showcount()

輸出：

    Total objects:  2
    Total objects:  2

1. @classmethod裝飾在showcount()方法上，其中的參數cls是參照整個類別person
2. 參數cls實質作用與參數self相似，可用其他名稱代替
3. 類別方法可透過類別名呼叫，也可被實體化的物件呼叫

* 當類別方法使用return時，可利用參數cls回傳值，而此值可被__init__方法接收，以建立實體屬性

輸入：

    class Rectangle:
      def __init__(self, width, height):
        self.width = width
        self.height = height

      def calculate_area(self):
        return self.width * self.height

      @classmethod
      def new_square(cls, side_length):
        return cls(side_length, side_length)

    square = Rectangle.new_square(5)
    print(square.calculate_area())

輸出：

    25



Static Methods{
Static methods are similar to class methods, except they don't receive any additional arguments; they are identical to normal functions that belong to a class. 
They are marked with the staticmethod decorator.
Static methods behave like plain functions, except for the fact that you can call them from an instance of the class.
ex{
class Pizza:
  def __init__(self, toppings):
    self.toppings = toppings

  @staticmethod
  def validate_topping(topping):
    if topping == "pineapple":
      raise ValueError("No pineapples!")
    else:
      return True

ingredients = ["cheese", "onions", "spam"]
if all(Pizza.validate_topping(i) for i in ingredients):
  pizza = Pizza(ingredients) 
}



}

Properties{
Properties provide a way of customizing access to instance attributes. 
They are created by putting the property decorator above a method, which means when the instance attribute with the same name as the method is accessed, the method will be called instead. 
One common use of a property is to make an attribute read-only
ex{
class Pizza:
  def __init__(self, toppings):
    self.toppings = toppings
    
  @property
  def pineapple_allowed(self):
    return False

pizza = Pizza(["cheese", "tomato"])
print(pizza.pineapple_allowed)
pizza.pineapple_allowed = True
>>>
False

AttributeError: can't set attribute
>>>
}

Properties can also be set by defining setter/getter functions.
The setter function sets the corresponding property's value.
The getter gets the value.
To define a setter, you need to use a decorator of the same name as the property, followed by a dot and the setter keyword.
The same applies to defining getter functions.
ex{
class Pizza:
  def __init__(self, toppings):
    self.toppings = toppings
    self._pineapple_allowed = False

  @property
  def pineapple_allowed(self):
    return self._pineapple_allowed

  @pineapple_allowed.setter
  def pineapple_allowed(self, value):
    if value:
      password = input("Enter the password: ")
      if password == "Sw0rdf1sh!":
        self._pineapple_allowed = value
      else:
        raise ValueError("Alert! Intruder!")

pizza = Pizza(["cheese", "tomato"])
print(pizza.pineapple_allowed)
pizza.pineapple_allowed = True
print(pizza.pineapple_allowed)
>>>
False
Enter the password: Sw0rdf1sh!
True
>>>
}

