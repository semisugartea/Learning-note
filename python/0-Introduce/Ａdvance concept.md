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



Packaging{
In Python, the term packaging refers to putting modules you have written in a standard format, so that other programmers can install and use them with ease. 
This involves use of the modules setuptools and distutils. 
The first step in packaging is to organize existing files correctly. Place all of the files you want to put in a library in the same parent directory. This directory should also contain a file called __init__.py, which can be blank but must be present in the directory.
This directory goes into another directory containing the readme and license, as well as an important file called setup.py. 

After creating the setup.py file, upload it to PyPI, or use the command line to create a binary distribution (an executable installer).
To build a source distribution, use the command line to navigate to the directory containing setup.py, and run the command python setup.py sdist.
Run python setup.py bdist or, for Windows, python setup.py bdist_wininst to build a binary distribution. 
Use python setup.py register, followed by python setup.py sdist upload to upload a package.

The previous lesson covered packaging modules for use by other Python programmers. However, many computer users who are not programmers do not have Python installed. Therefore, it is useful to package scripts as executable files for the relevant platform, such as the Windows or Mac operating systems. This is not necessary for Linux, as most Linux users do have Python installed, and are able to run scripts as they are. 

For Windows, many tools are available for converting scripts to executables. For example, py2exe, can be used to package a Python script, along with the libraries it requires, into a single executable.
PyInstaller and cx_Freeze serve the same purpose.

For Macs, use py2app, PyInstaller or cx_Freeze.

Standard Library{
Many third-party Python modules are stored on the Python Package Index (PyPI)
The best way to install these is using a program called pip
pip install library_name

}
