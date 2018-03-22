##Selenium IDE  

1. browsers test   
2. 只能用firefox開啟(seleuim的版本要跟firefox版本相符)   
3. 也可以在chrome上執行,必須透過webdriver(chromedriver)   
   * 先下載chromedriver(?)jar檔   
   * CMD執行命令   
   ```
      java -Dwebdriver.chrome.driver=chromedriver.exe -jar selenium-server-standalone-2.53.1.jar 
   ```
   * 在IDE工具裡options -> options ->webdriver ->  勾選Enable WebDriver Playback  ->改成 chrome   
   * 重開chrome跑IDE 

###指令
|command |Target    |Value| 描述  |   
|---------------------------------|   
|open    |/         |     |開新網頁|
|typeKeys|id=input |123456|輸入文字|   
|keyPress|id=imput |\13   |Enter  |   
|Click   |(//input[@name='XX'])[2]| |radio button輸入|   
|Click   |//select[@name='XX']|'value'|select選單|  
|assertText|//div[@id='Username']|test|驗證文字(ID)|   
|verifyLocation<br/>assertLocation|*/XX(url)| |驗證網址|  
|xpath |//table[@id='table1']//tr[4]/td[2]<br/>//a[contains(text(),'站台列表')]| |定位HTML元素|   
|selectWindow|title=xxx <br/>tab=1| |跳至另外的分頁|
|click   |link=tabName |  |跳至另外的分頁|


**在http網頁下type的指令要改成typekeys**


  
  

---
參考資料  

