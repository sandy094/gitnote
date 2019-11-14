##Jenkins 
  jenkins:一種CI 的工具    
  自動部屬  在被條件觸發時(定期定時.程式變動)，執行必要的編譯.測試.分析，達到自動化檢查專案狀態目的。   
  >  條件觸發就是 CI 中的 Continuous，不停地進行檢查和測試的行為，而取得程式碼後一連串的建置和測試，則是 CI 中集成的部分。  

  ####安裝流程(window)  
  1.從官網下載檔案  
  2.解壓縮安裝完成後-> install suggested plugins-> 設定完成   

  ----  
  #####建立新工作
  1. 點選"新增作業"  
  2. 輸入專案名稱及選擇專案類型![](\images\jenkins.png)
  3. 工作組態設定  
     3.1  General:輸入專案描述  
      GitHub project:設定github的url  
      忽略舊Builds:保留指定的建置記錄   
      限制專案執行節點:可以特地指定在哪個節點執行   
      ![描述設定](\images\jenkins-1.png)   
     3.2  原始碼管理:選擇程式碼的來源，如果選擇git要從這邊設定    
     3.3  建置觸發程序:  
      * 遠端觸發建置  
      * Build after other projects are built   
      * Github hook trigger for GITScm polling:實踐持續整合。讓Jenkins自動監控控，當有任何Push even發生時進行建置  
      * 定期建置  
         用Cron Format方式來定義時間，共分5個欄位。欄位與欄位之間用空白或Tab做區隔    
         1. 分(minute):0-59分
         2. 時(hour):0-23時  
         3. 日(day of month):1-31日  
         4. 月(month):1-12月  
         5. 星期(day of week):星期0-7(0=7)  
         如果要每隔15分鐘則是```H/15 * * * * ```  
      * 輪詢 SCM  
     3.4 建置環境  
     3.5 建置  
     3.6 建置後動作
---
  ##Jenkins+Robot Framework  
  #####安裝Robot Framework(從本機抓檔案)   
  做以下的設定   
  1. 安裝外掛程式:管理->外掛程式管理->可用性 OR 進階(下載檔案)->上傳外掛程式  
  2. 原始碼管理:無  
  3. 選擇執行Windows批次指令，寫執行的命令路徑  
    ```pybot.bat C:\unit_test\web\test_reports_page.robot```   
  4. 建置後動作:publish Robot Framework test results  
  設定完畢後，按下"馬上建置"   
  左側出現以下圖示表示正在"建置中"   
  ![建置中](\images\建置中.png)   
  出現以下畫面，表示成功  
  ![建置結果](\images\建置結果.png)
----
######名詞解釋   
#####Webhooks  網路鉤手  
透過此連結關聯兩個平台  

----

#####測試報告無法顯示截圖   
**解決辦法**  
```**/selenium-screenshot*.png,**/*.log```  
![](\images\Jenkins+github9.PNG)


 

參考資料 

[自動部屬-架設環境](https://github.com/muyinchen/woker/blob/master/%E9%9B%86%E6%88%90%E6%B5%8B%E8%AF%95%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA/%E6%89%8B%E6%8A%8A%E6%89%8B%E6%95%99%E4%BD%A0%E6%90%AD%E5%BB%BAJenkins%2BGithub%E6%8C%81%E7%BB%AD%E9%9B%86%E6%88%90%E7%8E%AF%E5%A2%83.md)  
[自動部屬-github](http://jenkins.readbook.tw/jenkins/plugin/github_pull_request_builder.html)  
[Jenkins相關設定說明](https://www.itread01.com/content/1546795810.html)

[Jenkin+Slack訊息通知設定](https://dotblogs.com.tw/stanley14/2018/05/28/jenkins_slack)
  


