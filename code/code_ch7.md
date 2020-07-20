##Robot FrameWork + Selenuim2    

python編寫的自動化測試軟體框架，此Framework用於自動化測試。  
#### 好處  
1. 已經有規範好的keyword，容易使用  
2. 程式經驗少的人也可以好上手  
### Selenuim  
- 是為了讓瀏覽器自動化(Browser Automation)需求所設計的一套工具，驅動瀏覽器  
- 是許多Web Testing工具核心
  
###### 工具(環境建置)     
1. 安裝Python**:確認python版本```python --version```    
當安裝失敗:設定環境變數:將安裝python的資料夾下script檔案位置記下，"加入"PATH的環境變數  
2. robotframework**:下指令 ```pip install robotframework```     
3. selenium2**:下指令```pip install robotframework-selenium2library```    
---

###### 命名規則  
Keyword:透過framework所以提供現有個關鍵字去撰寫測試   
有描述，簡單
---
###### 一、執行命令   
1. 執行整個test檔案 :   
```
robot web/test_dashboard_page.robot
```

2. 執行單一test :   
```
robot -t "Check login" web/test_dashboard_page.robot
```

###### 二、視窗高度大小  
利用JavaScript的語法去調整高度   
* 調整視窗高度  
window.scrollTo (**Height**, document.body.scrollHeight)  
```
Execute JavaScript    window.scrollTo(200, document.body.scrollHeight)
```  
* 到達指定的頁面高度   
window.document.documentElement.scrollTop = **Height**;  
``` 
Execute JavaScript  window.document.documentElement.scrollTop = 0;   
```

###### 三、出錯後繼續執行  
  Run Keyword And Continue On Failure  **Keyword**   

###**常用的keyword**   
#### 1、取值  
判斷是否有正常顯示值，取值再去做驗證  
1. Get Element Count **Element**  :抓有幾個element  
2. Get Text **Element**  :取得值 
3. Remove String  **變數**  **要去除的值**  :將字串做刪修
4. Convert To Integer **變數** :轉換成數值   

#### 2、判斷式   
1. Should Be Equal As Integers  **變數1**  **變數2**   
   :判斷變數1及變數2是否為相等(只能是數值)   

```
    ${A}=    Get Text    //div[@id="data-table"]//tbody/tr[1]/td[3]//span[1]
    ${testA}=    Remove String    ${A}    ,
    Convert To Integer    ${testA}
    Should Be Equal As Integers  ${testA}  ${testA}
```
2. Should Be Equal  **數值**  **數值**   
   :必須是Integer   
3. Should Be True    **判斷式**
4. Should Match  **String**  **pattern**   
比對值 pattern:需符合的條件  
*:任依字母皆符合(不管多少字元)  
?:任依字母皆符合(只限一個字元) 

#### 3、迴圈    
**For In Element**   
指定某些變數   
語法: **For ${target} in @{target_list}**   
Example  

```
    @{elements}    Set Variable    1   2
    :FOR    ${變數}    IN    @{elements}
    \    StartXXX
```    
**For In Range**  
特定某個Range 1到10  
語法: **For ${index} In range ${range}**  
Example  
```
    ${n}    Set Variable    10
    :For   1  in range  ${n}
    \    StarXXX 
```
如果初始值沒給就是從0開始  
由上述例子只會算0-9     
[迴圈參考文件](http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#for-loops)   
[迴圈參考文件2](https://tonylin.idv.tw/dokuwiki/doku.php/rf:rf:for_loop)

---
**其他筆記**   
[Robot命令行指令](https://www.itread01.com/content/1552567083.html)  
**參考資料**   
[Selenium2Library](http://robotframework.org/Selenium2Library/Selenium2Library.html)   
[RobotFrameWork](http://robotframework.org/robotframework/)   
[Builtin](http://robotframework.org/robotframework/latest/libraries/BuiltIn.html)  
[OperatingSystem](http://robotframework.org/robotframework/latest/libraries/OperatingSystem.html)  
[pass execution用法?](https://github.com/robotframework/robotframework/blob/master/atest/testdata/running/pass_execution.robot#L223)  
**額外學習**  
[為何要用RobotFramework](http://blog.castman.net/programming/2016/07/28/robotframework.html)
[How to write good test cases using Robot Framework](https://github.com/robotframework/HowToWriteGoodTestCases/blob/master/HowToWriteGoodTestCases.rst#test-suite-names)
