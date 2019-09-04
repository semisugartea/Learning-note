# PEP

 Python Enhancement Proposals (PEP)是由熟練的Python開發者為了改進語言而做的建議。
 PEP 8是對於寫出可讀代碼的格式指南。它包含了許多對於變數名稱的指導方針，如下所示：
 * 模組應有短且全小寫的名稱
 * 類別的名稱應使用CapWords風格，即單詞的首字母為大寫
 * 多數變數及函數應使用lowercase_with_underscores的風格
 * 常數(不改變的變數)應使用CAPS_WITH_UNDERSCORES的風格
 * 與Python關鍵字衝突的名稱應在後面加上下劃線
 PEP 8也建議在運算子與逗號後加上空白鍵以增加可讀性

 PEP 8其他的建議如下：
 * 每一行不應超過80個字元
 * 應避免使用'from module import *'
 * 每一行應只有一個敘述
 
 PEP 8建議使用空白鍵取代Tab鍵，但實際使用依個人習慣而定。若使用空白鍵，則使用4個空白鍵進行縮排。

# 主要的第三方函式庫(3rd-Party Libraries)

 Python的標準函式庫包含廣泛的功能。然而，一些任務需要使用第三方函式庫，一些主要的第三方函式庫如下：
 * Django: 用Python編寫的最頻繁使用的網路框架(web framework)，Django為包含Instagram和Disqus等網站提供助力。它包含許多有用的特點，而它所缺乏的部分則可被擴充包(extension packages)涵蓋。
 * CherryPy和Flask也是熱門的網路框架
 * BeautifulSoup:對於網路爬蟲(scraping data from websites或稱web scraping)相當有用，並能做出比利用標準表達式(regular expression)自製的爬蟲器還要更好的結果。

 有許多模組能使得透過Python進行科學與數學計算更加容易。
 * 模組matplotlib: 在Python中能依據數據製圖
 * 模組NumPy: 允許使用多維的排列(array)並且運行上比起Python的巢狀列表快速許多。它也包含能做數學運算的函式，例如對排列做矩陣轉換(matrix transformation)
 * 函式庫SciPy:包含許多對於NumPy功能的擴充。
 
 Python也可被用於遊戲開發。一般而言，Python對於用其他語言編寫的遊戲以手稿語言的形式使用，但也能利用Python本身進行編寫
 * 函式庫Panda3D:適合3D遊戲
 * 函式庫pygame:適合2D遊戲

# 包裝(Packaging)

 在Python中，packaging一詞代表要將自己編寫的模組放入標準格式中，使其他開發者能安裝並輕易地使用。這需要使用到模組setuptools和distutils。
 包裝的第一步是正確地組織已存在的檔案。將所有想要放入在函式庫的檔案置於同一個父目錄(parent directory)。該目錄需包含__init__.py檔，此檔案可以是空白的但一定要放在目錄中。此目錄被放入另一個目錄中，而這目錄還包含readme和license，以及相當重要的setup.py檔。
 例子如下：

    Fruit/
       LICENSE.txt
       README.txt
       setup.py
       fruit/
          __init__.py
          apple.py
          banana.py

 下一步是編寫setup.py檔。
 此檔包含包裝物的訊息，使得在上傳至PyPI後能用pip (name, version, etc.)的方式安裝。
 setup.py檔的例子如下：

    from distutils.core import setup

    setup(
       name='Fruit', 
       version='0.12',
       packages=['fruit',],
       license='MIT', 
       long_description=open('README.txt').read(),
    )

 在建立setup.py檔後，上傳至PyPI，或是使用command line創造一個binary distribution(可執行的安裝檔)
 為了建立source distribution，使用command line切換至包含setup.py的目錄，並執行python setup.py sdist 。
 執行python setup.py bdist或是在Windows中可執行python setup.py bdist_wininst以建立一個binary distribution。
 使用python setup.py register，在執行python setup.py sdist已上傳封包。
 最後，使用python setup.py install安裝封包

