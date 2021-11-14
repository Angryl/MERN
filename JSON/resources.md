# JSON

- JSON Files<br>
- The file type for JSON files : ".json"<br>
- The MIME type for JSON text : "application/json"<br>


- JSON Stands for **J**ava**S**cript **O**bject **N**otation 
- JSON is a text format for storing and transporting data
- JSON is "Self-describing" and easy to understand
- JSON is used to send data between Computers
- JSON is language INDEPENDENT

``` Json syntax us derived from javascript object notation, but the JSON format is text only.```

>JavaScript has a built in function for converting _JSON strings_ into _JavaScript objects_:
```
JSON.parse()
```

> JavaScript also has a built in function for converting an _object_ into a _JSON string_:

```
JSON.stringify()
```

## Syntex Rules
JSON syntex is derived from javascript from JavaScript object notation syntex:
- Data is in Name/value pairs
- Data is separated by commas
- Curly braces hold objects
- Square brackets holds arrays

> For Example:
```
"name" : "john"
```
JSON name Require Double Quotes
#### JSON
```{"name" : "Jonny"}```
#### Javascript
```{name : "jonny"}```

### DataTypes
In _JSON_ values must be of following types.
- **String**
- **number**
- **object**
- **array**
- **Boolean**
- **null**

Data Type | Example
----------|---------
String | String in json must be written in Double Quotes <br> ```{ "name" : "mark"}```
number | Number in JSON must be an integer or a floaing point <br> ```{"age" : 45}```
Object | values in JSON can be Objects <br> ```{ "employee" : {"name" :"Razak", "age": 28, "city": "baku"} }```
Array   | Values in JSON can be Arrays <br> ```{"employee" : ["john","stark", "hobs"] }```
Boolean | values in JSON can be _true or False_ <br> ```{"sale" : true}```
null    | Values in JSOn can be null <br> ```{"middlename" : null}```


In Javascript, values can be all of the _JSON_ and some other javascript Expressions, including:
- **String**
- **number**
- **object**
- **array**
- **Boolean**
- **null**
- **functon**
- **date **
- **undefined **

**NOTE :** In JSON string must be in Double Quotes. But in Javascript values must be in double and Single quotes.
<HR>

for example: 

In JSON

```{"name" : "Roy"}```

In Javascript

```{name : 'Roy'}```

#### Javascript Objects

Can create a object like thisL
```person = {name:"sam", age:32, city: "Baku"};```

and can have access like:
```person.name; ```

or An alternate Method is:

```person["city"];```

Complete Example:

```<!DOCTYPE html>
<html>
<body>

<h2>Access a JavaScript object</h2>
<p id="demo"></p>
<p id="demo1"></p>
<p id="demo2"></p>

<script>
const myObj = {name:"John", age:30, city:"New York"};
document.getElementById("demo").innerHTML = myObj.name;
document.getElementById("demo1").innerHTML = myObj["age"];
document.getElementById("demo2").innerHTML = myObj["city"];
</script>

</body>
</html>
```
<hr>
  
### Modifying the Data in JSON
  two methods:
1. ```Person.name = "Pearson";```
2. ```person["name"] = "pearson";```
