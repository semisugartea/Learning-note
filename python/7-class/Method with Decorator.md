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

# 靜態方法(staticmethod)

* 靜態方法與類別方法相似，可透過類別名呼叫該方法，但不接收任何引數，以下為例

輸入：

    class person:
        @staticmethod
        def greet():
            print("Hello!")

    person.greet()
    p1=person()
    p1.greet()

輸出：

    Hello!
    Hello!

# Properties

* @property可使被裝飾的方法成為屬性，或稱能透過被裝飾的方法呼叫屬性，而此屬性只可讀無法變更

輸入：

    class Exam:
        def __init__(self, score):
            self._score = score

        @property
        def myscore(self):
            return self._score

    e = Exam(60)
    print(e.myscore)
    print(e._score)
    e.myscore = 70

輸出：

    60
    60
    AttributeError: can't set attribute

* 利用@*被property裝飾的方法名*.setter可使相應的屬性能被重新設定

輸入：

    class Exam:
        def __init__(self, score):
            self._score = score

        @property
        def myscore(self):
            return self._score

        @myscore.setter
        def newscore(self, val):
            if val < 0:
                self._score = 0
            elif val > 100:
                self._score = 100
            else:
                self._score = val


    e = Exam(60)
    print(e.myscore)
    e.newscore=200
    print(e.myscore)
    e.newscore=-10
    print(e.myscore)


輸出：

    60
    100
    0

在例子中，利用@myscore.setter裝飾newscore()，使得在主程序中，能透過newscore()改變self._score的值，而myscore()再回傳self._score

* 利用@*被property裝飾的方法名*.getter可改變回傳值，但不能修改原屬性

輸入：

    class Exam:
        def __init__(self, score):
            self._score = score

        @property
        def myscore(self):
            return self._score

        @myscore.getter
        def plus_score(self):
            print('Getting...')
            return self._score +10


    e = Exam(60)
    print(e.myscore)
    print(e.plus_score)
    print(e.myscore)
    e.plus_score = 10
    print(e.plus_score)

輸出：

    60
    Getting...
    70
    60
    AttributeError: can't set attribute

* 利用@*被property裝飾的方法名*.deleter可使得在使用del敘述時，被裝飾的方法能呼叫

輸入：

    class Exam:
        def __init__(self, score):
            self._score = score

        @property
        def myscore(self):
            return self._score

        @myscore.deleter
        def del_score(self):
            print('Deleting..')
            del self._score


    e = Exam(60)
    print(e.myscore)
    del e.del_score
    print(e.myscore)

輸出：

    60
    Deleting..
    AttributeError: 'Exam' object has no attribute '_score'











