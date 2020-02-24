##Appium    
App測試自動化工具     
**簡單學習筆記**   

###Mobile APP分三種類型:  
1. Native App:原生的APP。  
2. Web App:手機板(WEB)。  
3. Hybird App: 同時具備以上兩點，將Javascript.HTML.CSS執行在embeded webview(WEB直接包版)    
###Appium: 開源跨平台(IOS & Android)的測試架構，目前最多人使用。  
支援多種語言撰寫  

App測試須考量的因素 
![](\images\App說明-1.png) 
系統版本、裝置不同，各裝置解析度、網路及使用者操錯方式不同  



打包測試App  
```xcodebuild -showsdks```
此指令會列出所有安裝的SDK裝置，從這邊記住模擬器SDK   
   

---
參考資料  
[Appium概念](http://blog.autoruby.com/2018/03/mobile-testing-appium.html)  
[操作參考](https://www.appcoda.com.tw/automated-ui-testing-appium/)   
[xcodebuild相關指令](https://chiahsien.github.io/post/how-to-use-appium-to-test-ios-app/)  
[pytest相關指令](https://zwindr.blogspot.com/2019/01/python-pytest.html)

