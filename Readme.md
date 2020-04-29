javac -d C:\projects\example\jaxWsEsxmple\my_target C:\projects\example\jaxWsEsxmple\src\main\java\service\*.java C:\projects\example\jaxWsEsxmple\src\main\java\service\bean\*.java C:\projects\example\jaxWsEsxmple\src\main\java\service\publish\*.java C:\projects\example\jaxWsEsxmple\src\main\java\service\client\*.java

cd my_target

wsgen -cp . service.OrderProcessService -wsdl

Запуск:
java service.publish.OrderWebServicePublisher

Клиент:
wsimport -keep -p service.client http://localhost:8080/OrderProcessWeb/orderprocess?wsdl

java service.client.OrderClient http://localhost:8080/OrderProcessWeb/orderprocess?wsdl


Статья:
https://www.ibm.com/developerworks/ru/edu/ws-jax/index.html