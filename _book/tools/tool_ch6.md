##Axure  
設計原型(Prototype)的工具，擬真網站   
**簡單學習筆記**   
1.  Tab Control  
    簡單分為Tab1 Body1 Tab2 Group2  
    1. 點選Body1設定成動態:點選元件按右鍵，選"Convert to Dynamic Panel"，點兩下該元件(dynamic panel)，新增一個state1
    2. 另一個Body2，貼在新增的state2(點兩下新增)，一定要貼在(0.0)
    3. Tab1建立連結:寫onClick的事件，點選"Set Panel State"，選擇執行的動作Select states 選原本設定的states;在點選"Set Selected/Checked"，勾選"This Widget"
    4. Tab2同上的步驟  
    5. 將點選的兩個button設定為selection group:選取兩的Tab，右方列表設定為Selection Group，自己設定Group名稱
2.  Accordion Control   
    1. 將下方多項items選取並點選"Convert to Dynamic Panel"，並取新的名字，並"hide"隱藏此區塊  
    2. 選擇"Header1"，給OnClick事件。點選"Toggle Visibillty"，目標是"body1"(剛剛設定的區塊)，下方選"Push/Pull Widgets"，Direction選"Below"
    3. 當再次點選Header1其他的header內層需要隱藏，點選header1的OnClick事件，新增"Hide"的動作，隱藏其他項(Header)的內層，下方的選擇如同上面  
3. Dynameic Droplists   
    從抓值去判斷要顯示哪段  
    1. 將各種狀況的下拉選單另外設Dynamic Panel States，成為一組(?)在這邊命名為"Job Title"，並重新命名狀態:分別為 Operations.Sales.Development  
    2. 在選怎下拉的選單，新增OnSelectionChange事件，選"Set Panel State"，勾選"Job Title"，"Select state"選擇"value"，點選"fx"，在Local Variables新增如附圖
    ![](\images\axure1.png)
4. Pass Text to Next Page
    傳值到下一頁面
    1. 建立變數
    2. OnClick事件->"Set Variable Value"->選擇變數"FirstNameVar"，下方Set variable to"text on weight"選擇對應的欄位->點選在即將跳轉的下頁->OnPageLoad事件->"Set Text".confirmation message->利用函數將變數串在文字裡
5. Set Dynamic Panel State On Next Page   
    將Radio Button設成一個群組，button要設"OnSelected"事件  
**暫時卡關**   
SCROLL-ACTIVATED STICKY HEADER

---
參考資料  
[官方教學文件](https://www.axure.com/support/training/interactive-button-tutorial)

