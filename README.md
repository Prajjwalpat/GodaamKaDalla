# INVENTORYMANAGEMENT
<h3>Run Flask app</h3><br>
1) clone the repo<br>
2)create virtual env fro python<br>
3)install libraries: pip install -r .\requirements.txt<br>
4)Setup mongodb uri and API key in config.py<br>
5)Python app.py<br><hr>

Hostname=https://inventorymanagement.fly.dev
<br><hr><br>

<h3>Endpoints(curl samples):</h3><br>
curl -X GET http://127.0.0.1:8080/summary -H "x-api-key: <yourapikey>"<br>
Get networth and quantity of stocks<br><br><br>

curl -X GET http://127.0.0.1:8080/inventory -H "x-api-key: <yourapikey>"<br> 
list all items<br><br><br>


curl -X POST https://inventorymanagement.fly.dev/inventory -H "x-api-key: <yourapikey>" -H "Content-Type: application/json" -d "{\"item\":\"lychee\",\"quantity\":670,\"price\":20}"<br>
Add a new item<br><br><br>


curl -X DELETE https://inventorymanagement.fly.dev/inventory/apple -H "x-api-key: <yourapikey>" <br>
delete an item<br><br><br>


curl -X PUT https://inventorymanagement.fly.dev/inventory/apple -H "x-api-key: 1234abddcd" -H "Content-Type: application/json" -d "{\"quantity\":80,\"price\":80}"<br>
change price or qty<br><br><br>


curl -X GET http://127.0.0.1:8080/inventory/Mango -H "x-api-key: <yourapikey>" <br>
get details of an item<br><br><br>

<hr><br>
</strong>curl request for API for currency converter: curl "https://data.fixer.io/api/latest?access_key=<fixerioAPIkey>&base=EUR&symbols=INR"<br><hr>
<h3>Database schema:</h3><hr>
{
  "_id": long int,
  "item": str,
  "qty": int,
  "price": float
}
item is unique
