##JavaScript      
  **QA**
  1. detect the client's brower's name   
  2. Javascript is case-sensitive(有區分大小寫)

Array Sort   
1. the sort() method sorts an array alphabetically   
  ```
  var A = ["Banana","Orage","Apple","Mango"];   
  fruits.sort();
  
  Apple,Banana,Mango,Orange
  ```   
2. the compare function  
  ```
  function(a,b){return a-b}  //由小排到大 
  fubction(a,b){return b-a}  //由大排到小
  ``` 
3. Booleans  
  ```
  var x = false;  //string
  var y = new boolean(false);  //object

  //(x===y) is false because x and y have different types
  ```
  * "==="不會把兩邊的type強制轉型,"=="會強制轉型"   
  * "=="簡易轉型      
  * object cannont be compared   
4. Switch   

**JSON**   
JavaScriptObjectNotation        
JSON is a format for storing and transporting data.   
JAON is often used when data is sent from a server to a web page.

**Objects**
1. definitions   
   objects也是一個變數(variables),但是objects可以包含很多個值   
   ```
   var person ={first:"John",age:50,color:"blue"};  
   ```
2. 宣告方式(Object Literal)  
有兩種，通常都用第一種  
 ```
 var person = {
   first="name",
   last="name",
   age=50,
   color="na"
 };   

 var person = new Object();
 person.frist="name";
 person.last="name";
 person.age=50;
 person.color="na";

 var person = new Object();
 person["first"]="name";
 person["last"]="name";
 person["age"]=50;
 person[color]="na";
```
  
prototype(原型)[類似繼承的概念]   
  1. object和object之間可以互相成為各自的prototype,被繼承的object將會繼承父object的prototype所有屬性     
  3. JavaScript 在尋找特性名稱時，會在該物件找特性,如果找不到再往prototype(原型)裡找特性並使用。   
  4. **只有在查找特性，而物件上不具該特性時才會使用原型，如果你對物件設定某個特性，是直接在物件上設定了特性，而不是對原型設定了特性。**   
ex   

```
function person(name,age){
  this.name=name;   
  this.age=age;
}

person.prototype.toString=function(){
  return'['+ this.name+','+this.age+']'
};
ver p1=new person('AAA',33);

console.log(p1.tostring()); //[AAA,33]
```

* 宣告變數   

```
 var d;
  console.log(d);   //d=undefind

  console.log(a);  //a=Regerenceerror  

```   

* 如果給予的值是[0,undenfind,null]在boolean是視為FALSE   


```
 var a;
   a+2;  //NaN

var n = null;   
  console.log(n*32);  //n=0

```
* 在運算中undefind會轉成非數值(NaN)，null轉成0

* 立即函式
 架構   
  (function(){

  })();

<html>
<script>
int num=10;
for(int i = 0;i<100; i++){
  int num=20;
}
printf("%d",num);
</script>
  </html>

---
參考資料   
[JavaScript](https://goo.gl/Un1FfB)   
[JavaScript陣列方法](https://goo.gl/A5otbG)