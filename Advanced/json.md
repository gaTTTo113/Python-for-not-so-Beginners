
# Python  JSON

Python has a built-in package called  `json`, which can be used to work with JSON data.

Import the `json` module:
```
import json
```

If you have a JSON string, you can parse it by using the  `json.loads()`  method.
The result will be a Python [dictionary](https://docs.python.org/3.4/c-api/dict.html):
```
import  json  

some_json = '{ "city":"Berlin", "count":790}'  
answer = json.loads(some_json)  
print(answer["count"])
```
> 790

If you have a Python object, you can convert it into a JSON string by using the  `json.dumps()`  method:
```
import  json  

data = {  
"city":  "Berlin",  
"count":  790  
}  
json_answer = json.dumps(data)  
```
You can convert Python objects of the following types, into JSON strings:
```
import  json  

json.dumps({"city":  "Berlin",  "count":  790})  
json.dumps(["train",  "bus"])
json.dumps(("John",  "Ben"))  
json.dumps("John")  
json.dumps(790)
json.dumps(113.54)  
json.dumps(True)  
json.dumps(None)
```
To make `json` strings more readable use the `separators` and the `indent` parameters:
```
json.dumps(data, indent=3, separators=(", ".  " - "))  
```
Use the  `sort_keys`  parameter to specify if the result should be sorted or not:
```
json.dumps(x, indent=3, sort_keys=True)
```
Read more about `json` library [here](https://docs.python.org/3/library/json.html)
