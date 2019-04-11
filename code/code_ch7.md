##Robot FrameWork + Selenuim    

Robot FrameWork: python編寫的自動化測試軟體框架
######工具(環境建置)     
**1. 安裝Python**:確認python版本```python --version```      
**2. robotframework**:下指令 ```pip install robotframework```   
**3. selenium2**:下指令 ```pip install robotframework-selenium2library```

Keyword:透過framework所以提供現有個關鍵字去撰寫測試   
主要網頁(?)->寫TestCase   

######執行命令   
1. 執行整個test檔案 :
robot ${robot_file_url}
```
example:
robot web/test_dashboard_page.robot
```

2. 執行單一test :
robot -t ${test_name} ${robot_file_url}
```
example:
robot -t "Check login" web/test_dashboard_page.robot
```

######視窗高度大小  
調整視窗高度  
Execute JavaScript    window.scrollTo (**Height**, document.body.scrollHeight)  
EX.
```
Execute JavaScript    window.scrollTo(200, document.body.scrollHeight)
```

#####傳值  
判斷是否有正常顯示值，取值再去做驗證  
1. Get Text **Element**  :取得值 
2. Remove String  **變數**  **要去除的值**  :將字串做刪修
3. Convert To Integer **變數** :轉換成數值  
#####判斷式   
1. Should Be Equal As Integers  **變數1**  **變數2**   
   :判斷變數1及變數2是否為相等
EX.
```
    ${A}=    Get Text    //div[@id="data-table"]//tbody/tr[1]/td[3]//span[1]
    ${testA}=    Remove String    ${A}    ,
    Convert To Integer    ${testA}
    Should Be Equal As Integers  ${testA}  ${testA}
```
2. Should Be True    **判斷式**
3. Should Match  **String**  **pattern**  
比對值 pattern:需符合的條件  
*:任依字母皆符合(不管多少字元)  
?:任依字母皆符合(只限一個字元) 

#####出錯後繼續執行  
  Run Keyword And Cintinue On Failure  **Keyword** 
######迴圈  
Example
```
    @{elements}    Set Variable    1   2
    :FOR    ${變數}    IN    @{elements}
    \    StartXXX
```   
[迴圈參考文件](http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#for-loops) 
[迴圈參考文件2](https://tonylin.idv.tw/dokuwiki/doku.php/rf:rf:for_loop)

---
**其他筆記**   
**參考資料**   
[Selenium2Library](http://robotframework.org/Selenium2Library/Selenium2Library.html)   
[RobotFrameWork](http://robotframework.org/robotframework/)   
[Builtin](http://robotframework.org/robotframework/latest/libraries/BuiltIn.html)  
[OperatingSystem](http://robotframework.org/robotframework/latest/libraries/OperatingSystem.html)