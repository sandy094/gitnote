## IOS
* UIView:是一個底層的原件，絕大部分的UI元件都是吃這個底層的元件
* UIKit:大部分的原件來源
* 練習使用工具:xcode:playground
### tableView

在框架裡塞一個view使用init   
uiview.init(frame:)
<!-- 詳細code在引用的時候 -->
<!-- 新的框架的概念 -->
在view塞一個框架
addsubview

let label= UILabel.init(frame:CGRect.init())


### viewcontroller 生命週期  
- viewcontroller有一個生命週期，週期跑完才會執行其他程序
一個生命週期有好幾個方法，主要常使用的是下列3個
1. loadView
2. viewDidLoad
3. viewWillAppear:當個view再次出現，需再次重Load就會執行

func
super.

```
var tableView:UITableView!

<!-- 1. 載入元件 -->
override func loadView(){
    <!-- 繼承 -->
    super.loadView()
    self.title="Title"
}

<!-- 2.載入完成 -->
override func viewDidLoad(){
    super.viewDidLoad()
    setupTableView()
}

<!-- 列表 -->

func setupTable(){
    tableView = UITableView.init(frame: view.bounds)
    view.addSubview(tableview) 
    tableView.delegate = self
    tableView.dataSource = self
}

```
layout...view
元件重載所觸發的view

### 導頁
- 導頁有兩種方式:
1. present:由下往上開啟
2. Push
- 關閉這兩種導頁方式各不一樣  
1. present-> dimiss  
2. push->pop  
** Present必須在載入的時候將此func加入執行序，這時候必須要用**dispathque**讓此func在生命週期跑完之後作執行
```
<!-- 此範例為Present方法 -->
Dispathque.main.async{[week self] in
  self?.present(page2ViewController, animated: true, completion: {

  })}

```

2. Push
```

self.navigationController?.pushViewController(page2ViewController, animated: true)

```

----
### navigate
- navigate:UINavigationController

self.title
embin 
self.navigate

- closeBtn.addTrget(self action: #selector(closeBtnTrapped),for: .touchUpInside)
<!-- closeBtnTrapped是一個點擊的方法需另外定義 -->
<!-- 點擊方法 -->
- 需要加上@objc func 方法
```
@objc func closeBtnTrapped(){
    closeThisPage()
}

func closeThisPage(){
    self.dimiss(animted:true, completion: nil)
}

```
### tableview
- 有這兩個方式
  - view.bounds-->先用這個
  - view.frame

- tableView.delegate
- tableView.datsource  
**冒號是繼承逗號是擴充**

protocol

section都從tableview

exten:繼承
共用cell


---

**參考資料**   


---
**問題**  
super 是繼承的概念嗎?  
@objc func跟func差別在?
