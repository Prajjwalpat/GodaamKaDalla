# INVENTORYMANAGEMENT
##Run Flask app
1) clone the repo
2)create virtual env fro python
3)install libraries: pip install -r .\requirements.txt
4)Setup mongodb uri and API key in config.py
5)Python app.py

##Endpoints(curl samples):
curl -X GET http://127.0.0.1:8080/summary -H "x-api-key: <yourapikey>"
Get networth and quantity of stocks

curl -X GET http://127.0.0.1:8080/inventory -H "x-api-key: <yourapikey>" 
list all items


curl -X POST https://inventorymanagement.fly.dev/inventory -H "x-api-key: <yourapikey>" -H "Content-Type: application/json" -d "{\"item\":\"lychee\",\"quantity\":670,\"price\":20}"
Add a new item


curl -X DELETE https://inventorymanagement.fly.dev/inventory/apple -H "x-api-key: <yourapikey>" 
delete an item


curl -X PUT https://inventorymanagement.fly.dev/inventory/apple -H "x-api-key: 1234abddcd" -H "Content-Type: application/json" -d "{\"quantity\":80,\"price\":80}"
change price or qty


curl -X GET http://127.0.0.1:8080/inventory/Mango -H "x-api-key: <yourapikey>" 
get details of an item


###curl request for API for currency converter: curl "https://data.fixer.io/api/latest?access_key=<fixerioAPIkey>&base=EUR&symbols=INR"
