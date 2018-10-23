##Angular   
專案內容     
![專案內容](\images\angular.PNG)  
#####環境架設  
* node.js  
* angular cli  
```npm install -g @angular/cli```   

確認版本   
```
node -v  //確認node.js版本為8.9以上  
npm -v   //確認版本為5.5.1以上
ng -v    //確認cli版本為6.0.0以上
```
----
建立專案   
```ng new project-name```  
啟動   
```
cd project-name  //指到檔案位置
npm start 或  npm serve  //啟用  
```
切component  
``` 
ng g c component-name  //新增component  
```  

將原本html部分搬到component.html  
在app.component.html加入標籤  

----  
#####資料綁定Data Binding   
1.內嵌繫結(Interpolation):變數改變HTML跟著改變 ex.```<h1>{{value}}</h1>```   
2.屬性繫結(Property Binding):變數改變HTML跟著改變 ex.```<h1 [preperty]="value"> </h1>```  
3.事件繫結(Event Binding):發送HTML事件到script裡面  ex.```(event)="function()"```  
4.雙向繫結(Two-way Data Binding):變數改變HTML跟著改變，且發送HTML事件到script裡面 ex.```[(ngModal)]  ```  
5.屬性指令(Attribute Directive):修改元素的外觀或者是行為，常用的是ngClass、ngStyle ex.```<p [ngStyle]="{'font-size.px': fontSize}"></p>``` 並在component.ts 加function    
6.結構指令(Structural Directive):```<span *ngIf="keyword === ''"> </span>```  
######ngclass   
動態更新element的CSS   

######NgModal   
使用於Input.Select,雙向綁定component數據   
######ngOnInit   
執行比較複雜的初始化(constructor是設定簡單的初始化資料)    
設定完@Input屬性之後，設定Component   
######ngOnChange   
偵測到元件的@Input屬性有變動時，呼叫ngOnChange    

######*ngFor   
*ngFor="let item of items"   
items為陣列

---   
#####元件傳遞資料   
* @Input():傳遞資料給子元件 ex.將資料移到app.component.ts 在app.component.html加```<app-main [list]="list"></app-main>``` 在main.component.ts加```@Input() list: any[]```    
* @Output():接受子元件輸出的資料 ex.在nav component.ts 加```@Output() keywordChanges = new EventEmitter<string>();```  

---
#####服務(Service)   
* 自訂服務元件  
  ```ng g s serviceName```  
* HttpClient服務  
  1. 在app.component.ts import HttpClientModule，也在service.ts import，並加一個FN，ex.  
  ```
  getData(){
      return this.httpClient.get('assets/data/car.jason')
  }  
  ```  
  2. 在app.component.ts呼叫服務元件，import service並呼叫  
  ```
   import {**Service name**Service}

   list:any
   listOriginal:any

   Service.getData().subscribe(resp => {
       this.listOriginal = this.list = resp
   })
  ```



**SMART-TABLE**   
[參考資料](https://akveo.github.io/ng2-smart-table/#/documentation)   
table屬性   
type:   
1.text:單純文字   
2.html:   
3.custom(renderComponent)使用套件   

valuePrepareFunction:在載入表格內容之前，你可以定義該欄位要如何顯示   

######Toaster Module   
[參考資料](https://github.com/PointInside/ng2-toastr)   

**其他筆記**   
[Angular](https://gist.github.com/doggy8088/91e5b6773715c15e5df50792678cac2a)  
[Angular-開發環境](https://gist.github.com/wellwind/5190fd34bf67c3fb9736a70c0af57ebd)  
[屬性指令Attribute Directive](https://dotblogs.com.tw/h20/2018/05/08/182057)  
[Angular 資源](https://angular.io/resources/)