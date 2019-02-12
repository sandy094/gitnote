##Jenkins+Github  
####Github連結Jenkins  
當做任何commit到branch，透過webhook告訴Jenkins server並開始建置  
#####Step1.設定API TOKEN跟專案TOKEN   
 * API TOKEN:當需要進入jenkins執行動作時須透過帳號及此組Token，一設定的權限進入Jenkins。   
     取得方法:從Jenkins帳戶->設定取得API Token。本身會有一組(或可以自己產生一組)     
   ![](\images\Jenkins2.PNG)  
 * 專案Token:取得要執行的專案的Token給Jenkins(Githib->Jenkins)  
   github(帳戶) setting->Developer settings->Personal access tokens->Click **Generate new token**  
   ![](\images\Jenkins+github6.PNG)  
   setting Token description-> 勾選repo(勾選需要的設定)  
   ![](\images\Jenkins+github7.PNG)  
   將產生的Token複製起來並記下

#####Step2.Jenkins專案設定  
* 原始碼管理:Git Url 貼上git檔案的位址**EX.https://git@github.com/sandy094/ppap_automated_test.git**       
  Credentials輸入github 使用者帳號(**可以不用設定**)  
  ![專案設定](\images\jenkins1.PNG)

* 建置觸發程序  
  選**遠端觸發建置**，填寫驗證Token此處填寫專案的Token(Github)   
  ![建置觸發程序](\images\Jenkins+github10.PNG)   

* 建置     
   下指令**執行Windows批次指令**  
    ```robot web/檔名.robot```  
    ```robot web./```
* 建置後動作  
  選**Publish Robot Framework test results**

#####Step3.Githib設定   
* 新增Webhooks  
  選**Add Webhook**  
  1. Payload URL:填寫  
  **http://<font color=red>userid:APItoken</font>@JenkinsURL/job/<font color=red>jenkinsjobname</font>/build?token=<font color=red>TOKEN_NAME</font>**   
  2. Content type: application/json
  
#####Step4.PUSH 專案   
  成功連線後，試著PUSH到Branch  
  當PUSH成功後，Jenkins同時發起建置的動作，表示觸發成功  
  ![成功畫面](\images\Jenkins+github8.png)

----
#####小工具   
#######ngrok  
[ngrok](https://ngrok.com/)   
利用此小工具將localhost:8080暫時推上網路  
將檔案載下來解壓縮，透過CMD切到下載目錄並執行語法```ngrok.exe http 8080``` (後面打要的port號)    

---
github token:c1a78185cb552b935125475265e67c8362eae16f   
測試區帳號APItoken:  
1118d038c5c6907f28d1c05851e8d3ce99
https://github.com/sandy094/ppap_automated_test.git


----
參考資料  
[jenkins連結github](https://blog.miniasp.com/post/2016/01/05/Jenkins-on-Windows-04-Inegrating-GitHub-Bitbucket-VSTS-build-trigger)


