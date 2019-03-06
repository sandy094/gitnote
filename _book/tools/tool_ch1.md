#GIT工具   
git網路託管空間-Github.Bitbucket  
圖形化介面SourceTree   
##下載GIT##
  * 先下載GIT[下載連結](http://msysgit.github.io/)   

##command line 執行git 步驟##    
第一次git     
1. 先建完專案   
2. 加入git，並建立自己的reposity(在要建git的資料夾上)  
 ``` 
  $ git init   
```
3. 將檔案add到staging area   
 ```
  $ git add 檔名.txt  
 ```
4. commit到repository   
  ```
  $ git commit  
  ```
5. 寫commit的訊息  
  ```
  $ git commit -m '訊息內容'   
  ```

---     

##command line##     
**clone**   
將現有的專案clone(複製)下來   
1. 從github網站->按下專案內部的綠色按鈕->把網址複製下來   
2. 回到命令行  

**branch**
1. 建立新 local branch   
```
$git branch  <new name>
```
2. 改名字 (如果有同名會失敗，改用 -M 可以強制覆蓋)
```
$git branch -m <old_name> <new_name> 
```
3. 列出目前有哪些branch
```
$git branch
```
4. 切換branch(要先commit)
```
$git checkout <branch_name> 
```
5. 刪除branch
```
$git branch -d <branch name>
```
6. 砍掉commit重來，修改的程式依然留在working tree
```
$git reset
$git reset HEAD^ //回到前一版 changes留在woring tree
$git reset -hard HEAD^ //刪掉前一次commit
```

---   
##tortiseGIT小烏龜##   
**COMMINT & PUSH**
  1. 在要更新的資料夾按右鍵  
  2. $ git commit -> mastar   
  3. commit 視窗(上面寫commit的訊息,下面勾選要commit的檔案)  
  ![說明](\images\說明.png)  
  4. 成功commit後再push   
     
**Clone**    
  1. 從github網站->按下專案內部的綠色按鈕->把網址複製下來   
  2. 在要放置的位置按右鍵找到"Git Clone"   
  3. 貼上網址(通常都已經複製上)  

**pull**    
  pull 最新的版本   
  1. 在資料夾的位置按右鍵 TourtiseGit->Pull   

**branch**   
  1. 建立新分支   
   TortiseGit -> Create Branch   
  2. 切換分支  
   TortiseGit ->Switch  切換Branch   
   OR   
   Switch -> Create New Branch   
  3. PUSH to Branch   

**Merge**  
 衝突一次顯示出來
  1. 先切為主線(master)   
  2. TortistGit ->merge   
   merge branch
  3. 解決衝突   
  4. 解決完衝突後再一次commit&push   

**Rebase**
  若有衝突，依照每一個commit解。在分主分支上使用

**WorkingTree**
   ```
   $git worktree add <folder name> master  //切到master
   $git worktree prune  //刪除worktree相關資料
   ```


 ##其他語法   
 1. 目前git的狀況  
   ```
    $git status  
   ```     
 2. 將不在Repository的檔案移出StagingArea   
    ```
    $git rm --cached 檔案名稱  
    ```  
 3. 將已經在Repositry的檔案移出StagingArea   
    ```
    $git reset HRAD
    ```
 4. 暫存有修改的部分，保存到一個未完成變更的推疊(stack)中   
    ```
    $git stash
    ```
    查看現有的推疊
    ```
    $git stash list
    ```
    重新套用儲藏(套用最近儲藏的)
    ```
    $git stash apply

    $git stash pop

    $git stash apply stash@{?}  //指定套用哪一個儲藏
    ``` 
    移除儲藏列
    ```
    $git stash drop
    ```


 **GIT檔案有3種不同狀態**  
    

 |狀態             |位置             | 執行的動作|   
 |--------------------------------------------|   
 |已修改(Modified) |working directory| add      |   
 |已暫存(Staged)   |Staging area     | commit   |    
 |已提交(committed)|Repository       | (FINISH) |


**Q&A**   
執行TotoriseGit指令出現的訊息

Q. git did not exit cleanly (exit code 1)

A. 解決方式 : Resposity已經有檔案，要先做Pull

Q.git did not exit cleanly (exit code 128)

A. 解決分式 : Git資料夾進入Setting 將 Network 設定改為 C:\Program Files\TortoiseGit\bin\TortoiseGitPlink.exe   

  ---
  #參考資料#   
  [tortiseGIT]()  
  [git基本語法](https://goo.gl/728vnx)   
  [git文件](https://git-scm.com/docs/git)


**類似工具**   
  [SOURCE TREE](https://zhuanghongkuan1.gitbooks.io/demo0115/content/chapter4/433.html)