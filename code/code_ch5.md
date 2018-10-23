##bootstrap
需要先import->bootstrap->jquery   
連結本機端該專案也要npm install進package
```
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title>boostrap</title>
   <!-- 掛載CSS樣式 連結本機端-->
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap-grid.min.css"> 
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap-reboot.min.css">
    <link rel="stylesheet" href="./style.css">
    <!-- 掛載JS樣式 -->
    <script src="node_modules/jquery/dist/jquery.js" charset="utf-8"></script>
    <script src="node_modules/jquery/dist/jquery.min.js" charset="utf-8"></script>
    <script src="node_modules/popper.js/dist/umd/popper.js" charset="utf-8"></script>
    <script src="node_modules/bootstrap/dist/js/bootstrap.min.js" charset="utf-8"></script>  
    <script src="./script.js" charset="utf-8"></script>
</head>
<body>
    
        <div class="container-fluid">   
            <div class="row">
                <div class="col-6"><span>1</span></div>
                <div class="col-4"><span>2</span></div>
                <div class="col-2"><span>3</span></div>
            </div>
    </div>
    
</body>
</html>
```

**其他筆記**   
切版->就是把原本設計好的圖檔切成可以使用的HTML/CSS，如何切好的板靠"經驗"   
BOWER->管理相依套件工具，bower更新檢查個套件最新版本及相依   
[參考文件](https://ithelp.ithome.com.tw/articles/10159261)