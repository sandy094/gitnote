## Python
### 列表

新增
```
names:["A,B,C,D"]
<!-- 新增在後面 -->
names.append("E")
<!-- 新增在特定一個位置 -->
names.insert(1,"F")

print(names)
<!-- 執行結果 -->
["A,B,C,D,E"]
["A,B,C,D,E"]
["A,F,C,D,E"]

```

刪除
```
names:["A,B,C,D"]
<!-- 沒特別說明就是刪除最後一個 -->
names.pop()


```  
--- 
### Pytest  
是python測試工具，支援平行化測試  

需遵循的規則  
1. 檔名必須含有test是 ```test_*.py``` 或 ```*_test.py```   
2. 類別名稱必須是 ```test```開頭  
3. 函數與類別內方法必須要以 ```test``` 最為前綴  


**參考資料**   
[Python](https://ithelp.ithome.com.tw/users/20069378/ironman/1113)   
