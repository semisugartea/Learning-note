# try/except

可利用try/except語句處理測試並處理例外,語法形式為:
	
		try:
			statement
		except *exception*:
			statement
		
1. 首先執行try的敘述
2. 若沒有例外發生,try的敘述執行後直接結束,跳過except的敘述
3. 若例外發生,會先跳開try的敘述,執行相應的例外的except的敘述,一個except可利用()指定多個例外
4. 若沒有相應的例外,會執行不指定的except的敘述,此不指定的except必須排最後
5. 若連不指定的except都沒有,則會跳回try的敘述,執行標準的例外回報敘述
	
* else 

	在try/except語句後使用else,若無例外則會執行else的敘述,使用上可有可無,語法形式為:
	
		try:
			statement
		except *exception*:
			statement
		else:
			statement

* finally

	在try/except語句後使用finally,則無論有無例外都會執行finally的敘述,必須放於else之後,使用上可有可無,語法形式為:
	
		try:
			statement
		except *exception*:
			statement
		else:
			statement
		finally:
			statement

