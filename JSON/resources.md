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

# Syntex Rules
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

## DataTypes
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

## Javascript Objects

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
  dwf
  
## Modifying the Data in JSON
  There are two methods:
1. ```Person.name = "Pearson";```
2. ```person["name"] = "pearson";```
  
 ## JSON.parse()
 
> Use of JSON is to ecxchange the data to/from a web Server.
> When receving data from a web server, the data is always a string.
> Parse the data with **JSON.parse()**, and the data become a Javascript object.
  
Example - Parsing JSON <br>
Imagine we received this text data from a web server:
  ``` '{"name" :"peter","age": 23,"city": "razak"}' ```
 <br>
  use Javascript function ```JSON.Parse()``` to convert text into a javascript object:
 ```const obj = JSON.parse( '{"name" :"peter","age": 23,"city": "razak"}' ); ```
  <br>
  **NOTE:** Make sure the text in JSON format, or else you will get an error.
  
  Using java object in webpage:
  
 Example:
  
  ```<p id="test"></p>
  
  <script>
    document.getElementById("test").innerHTML = obj.name;
  </script>
  ```
  
Example #2:

  ```<!DOCTYPE html>
<html>
<body>

<h2>Creating an Object from a JSON String</h2>

<p id="demo"></p>

<script>
const txt = '{"name":"John", "age":30, "city":"New York"}'
const obj = JSON.parse(txt);
document.getElementById("demo").innerHTML = obj.name + ", " + obj.age;
</script>

</body>
</html>
```
  
  ### Array As JSON
  applying ```JSON.parse()``` on a JSON derived from an array, the method will return a javascript array, instead of javascript Object.
  
  Example:
  
  ```
  const text = '["Ford", "BMW", "Audi", "Fiat"]';
  const myArr = JSON.parse(text);
  ```
  
  ```
  <!DOCTYPE html>
<html>
<body>

<h2>Parsing a JSON Array.</h2>
<p>Data written as an JSON array will be parsed into a JavaScript array.</p>
<p id="demo"></p>

<script>
const text = '[ "Ford", "BMW", "Audi", "Fiat" ]';
const myArr = JSON.parse(text);
document.getElementById("demo").innerHTML = myArr[0];
</script>

</body>
</html>
```
## Exceptions
 #### Parsing Dates
 Date objects are not allowed in JSON.

If you need to include a date, write it as a string.

You can convert it back into a date object later:
  
 **Example:**
  
converting a string into a date:
  ``` 
  <!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a date object.</h2>
<p id="demo"></p>

<script>
const text = '{"name":"John", "birth":"1986-12-14", "city":"New York"}';
const obj = JSON.parse(text);
obj.birth = new Date(obj.birth);
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth; 
</script>

</body>
</html>
```
 
we can also use the _second parameter_, of the ```JSON.parse()``` function, called _reviver_.

The reviver parameter is a function that checks each property, before returning the value.
  
 Example:
  
  Convert a string into a date, using the reviver function:
  
  ```
  <!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a date object.</h2>

<p id="demo"></p>

<script>
const text = '{"name":"John", "birth":"1986-12-14", "city":"New York"}';
const obj = JSON.parse(text, function (key, value) {
  if (key == "birth") {
    return new Date(value);
  } else {
    return value;
  }
});
document.getElementById("demo").innerHTML = obj.name + ", " + obj.birth; 
</script>

</body>
</html>
```
  
  ### Parsing Functions
  Functions are not allowed in JSON.

If you need to include a function, write it as a string.

You can convert it back into a function later:
 
  **Example**
  
  Convert a string into a function:
  
  ```
  <!DOCTYPE html>
<html>
<body>

<h2>Convert a string into a function.</h2>
<p id="demo"></p>

<script>
const text = '{"name":"John", "age":"function() {return 30;}", "city":"New York"}';
const obj = JSON.parse(text);
obj.age = eval("(" + obj.age + ")");
document.getElementById("demo").innerHTML = obj.name + ", " + obj.age(); 
</script>

</body>
</html>
```
  **NOTE:** we should avoid using functions in JSON, the functions will lose their scope, and we would have to use eval() to convert them back into functions.
  
  
