## Swift 
###基本  
 * 常數 :使用Let宣告
 * 變數 :使用Var宣告
  
**命名方式:小駝峰規則**  

### 型別   
 * 宣告int型別  
 ```
var num:int
 ```
 * 轉型別  
 ```
 let nowNum = Int(numberValue)
 //轉成整數
 ```
 
 * nil :沒有值  
 * 任何型別只要加上option type 都可以設為nil   
 ```
var someSource : int?
//加上問號代表可以為nil
 ```

### 運算子  
* 連結字串   
```
var ex: A + B
// ->AB 
var ex += "HA!"
// ->AB HA!
```
---
### 字串  
* 在字串加入其他型別:需加‵```\()```  
```
 let score = 80
 let string = "My score is \(score)."
```
* \(變數、常數、表達式)
 ### 陣列
```
 var arr=[int]
 //宣告空陣列
 var arr=[int]()
 //加一個值
 arr.append(12)
```
### 函式  
用來完成特定任務  
```
 func 函式名稱(參數:參數型別)->返回值型別 {
     內部執行程式
     return 回傳值
 }
 func addOne(num : Int){
     print(num + 1)
 }

  //呼叫函式，傳入12
  addOne(12)
  //印出13
```   

* 多重參數函式  
超過一個參數，將依序將參數帶入，以","隔開  
 ```  
     func hello(name : String,age: Int){
         print("\(name) is \(age) years old.")
      }

     hello("Jack", age: 25)  
 ```

**如果函式有更多參數，除了第一個參數不用之外，第二個以及之後的參數都需要標註其對應的名稱**   

* 內/外部參數名稱  
  - 內部參數名稱:用於函數內部呼叫   
  - 外部參數名稱:用於呼叫函式，標註給函式的參數  
```  
 func hello(name n: String,age a: Int){
     //n.a為內部參數名稱
     print("\(n) is \(a) years old.")
 } 
 // name.age為外部參數名稱
 hello(name:"jack",age:25)
```  
**第一個參數不用寫名稱，其後的參數也不寫可以加"_"**
```  
 func hello(name: String, _ age: Int){
     print("\(name) is \(age) years old.")
 } 
 // 呼叫的時候，第二個參數就不用寫名稱
 hello("jack",25)
```  


---


**參考資料**   
[swift 基本](https://itisjoe.gitbooks.io/swiftgo/content/ch1/ch1.html)  

---
**問題**  

