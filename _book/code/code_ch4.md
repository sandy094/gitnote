##HTML/CSS      

1. HTML tags are not case senteive(沒有帶小寫之分)   
2.   
   <b> - Bold text粗體 </b>    
   <strong> - Important text粗體-[text important]  </strong>   
   <i> - Italic text斜體 </i>   
   <em> - Emphasized text斜體-[text important] </em>   
   <mark> - Marked text </mark>   
   <small> - Small text </small>   
   <del> - Deleted text </del>  
   <ins> - Inserted 底線 </ins>   
   <sup> - Superscript text上標 </sup>  
   <sub> - Subscript text下標 </sub><br>
   文字順序對換-><bdo dir="rtl">what a wonderful day</bdo>      

3. HTML supports [140 standard color name](https://www.w3schools.com/colors/colors_names.asp)   

   HTML color can use RGB[rgb(255,99,71)],HEX[#ff6347],HSL[hsl(9,100%,64%)],RGBA [rgba(255,99,71,0.5)],HSLA[hsla(9,100%64%,0.5)]   

**CSS在HTML執行有3種方式**   
1. inline   
```
 <p style="color:blue">this</p>
```
2. internal-used to denfine a style for single HTMLpage嵌入套用      
```
<html>
<head>
<style>
body {background-color:powderblue;}
h1   {color:bluel}
p    {color:red;}
</style>
</body>
</html>
```
3. external CSS外部連結   
   連結CSS檔連結 
   ```
   <head>
    <link rel="stylesheet" href="style.css">
   </head>
   ```
  使用ID做CSS連結  

  ```
  <html>
    <head>
      <style>
       #p01 {
         color: blue;
        }
      </style>
    </head>
    <body>

       <p id="p01">I am different.</p>

    </body>
</html>
  ```
  
** The id of an element should be unique within a page, so the id selector is used to select one unique element!**  
連結外部CSS資源(匯入套用)
```
<link rel="stylesheet" href="https://www.w3schools.com/html/styles.css">
```
**標籤**   
* table標籤   
```
<table> 
 <tr>
  <th>1</th>
  <th>2</th>
 </tr>
 <tr>
   <td>11</td>
   <td>22</td>
  </tr>
 </table>
```
* list標籤  
 1. An unordered List(圖形標籤ul)   
<font color="cornflowerblue">
list-style-type:desc //標籤的樣式(預設)   
list-style-type:circle   
list-style-type:square   
list-style-type:none
</font>   
```
<ul style="list-style-type:circle">
  <li>A</li>
  <li>B</li>
  <li>C</li>
</ul>
```
 2. An Ordered List(文字標籤ol)   
```
<ol type="1">
 <li>AAA</li>   
 <li>BBB</li>
 <li>CCC</li>
</ol>
```

* placeholder(input 預設文字)   
 1. example   
<input type="text" name="fname" placeholder="first name">   
```
<input type="text" name="fname" placeholder="first name">  
```

**[CSS]class/id區別**   
class 可以在頁面裡重複使用,盡量用class   
id 只能出現一次,可以用來區分不同模組  
class名稱跟ID名稱有大小寫之分    
class:
```   
<style type="text/css">
.footer{background:LightCyan ;}
</style>
<div class="footer">fotter</div>
```
id
```   
<style type="text/css">
#footer{background:LightCyan ;}
</style>
<div id="footer">fotter</div>
```

**CSS盒子模式**   


1. 邊界Margin   
   語法:   
   margin[上邊界值][右邊界值][下面邊界值][左邊界值]   
2. 邊框border   
3. 留白padding   
   語法:   
   padding[上留白值][右邊留白值][下面留白值][左留白值]
   
*CSS文字*
1. text-align-文字如何對齊  
``` 
   p{text-align:justify;} //左右對齊
```
2. word-spacing-字與字之間的距離
```
  p{word-spacing:5px;}
```

**QA**   
 
Q. Which HTML element defines navigation links? A.```<nav>```   
Q. Choose the correct HTML element for the largest heading A.```<h1>```   
Q. The HTML ```<canvas>``` element is used to draw graphics on a web page. A.True  
Q. Which input type defines a slider control?  A. range   
Q. Which HTML element is used to display a scalar measurement within a range? A.```<meter>```   
Q. Which HTML element is used to specify a header for a document or section?A. ```<header>```
 


---
參考資料   

