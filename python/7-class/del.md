# 物件生命週期 Object Lifecycle

物件的生命週期是由創造，操作，消滅所組成

在第一階段，物件被定義所屬的類別中。
在下一階段，物件被實例化，即是呼叫__init__方法，並將記憶體分配給實例儲存。在這情形發生前，會呼叫__new__方法。在特殊的案例中經常被覆寫(overridden)。
在這階段後，物件開始可被使用。

當物件被摧毀時，被分配的記憶體會被釋放並可用做其他用途。物件摧毀發生在它的引用計數(reference count)歸零時。
引用計數是用來參照物件的變數及其他元素的數字。若物件沒有參照點(即指引用計數為零)，則沒有其他物件能與之互動，便可安全地刪除。

在部分情況下，兩個或以上的物件只會互相參照，此時依然能刪除。
del敘述能逐一減少物件的引用計數，這時常導致物件刪除。
del敘述的魔術方法是__del__。
當物件不再被需要而被刪除的過程稱為垃圾回收(garbage collection)。
總結上，當物件被指派新的名稱或被放入容器(list,tuple,dictionary)中時，物件的引用計數會增加；當物件被del敘述刪除時，物件的引用計數會減少
，而他的參照會被重新指派，或是參照會離開作用域(scope)。當物件的引用計數歸零時，Python會自動刪除它。

例子：

    a = 42  # Create object <42>
    b = a  # Increase ref. count  of <42> 
    c = [a]  # Increase ref. count  of <42> 

    del a  # Decrease ref. count  of <42>
    b = 100  # Decrease ref. count  of <42> 
    c[0] = -1  # Decrease ref. count  of <42>


