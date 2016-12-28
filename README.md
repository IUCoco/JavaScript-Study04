# JavaScript-Study04
### AJAX 教程   

********声明该资料来源于w3school以及网络博客整理，仅供学习交流谢谢！*******  

AJAX = Asynchronous JavaScript and XML（异步的 JavaScript 和 XML）。  
AJAX 不是新的编程语言，而是一种使用现有标准的新方法。  
AJAX 是与服务器交换数据并更新部分网页的艺术，在不重新加载整个页面的情况下。  

#### XMLHttpRequest 对象  
所有现代浏览器均支持 XMLHttpRequest 对象（IE5 和 IE6 使用 ActiveXObject）。  
- XMLHttpRequest 用于在后台与服务器交换数据。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新。  
为了应对所有的现代浏览器，包括 IE5 和 IE6，请检查浏览器是否支持 XMLHttpRequest 对象。如果支持，则创建 XMLHttpRequest 对象。如果不支持，则创建 ActiveXObject ：  
```
var xmlhttp;
if (window.XMLHttpRequest)
  {// code for IE7+, Firefox, Chrome, Opera, Safari
  xmlhttp=new XMLHttpRequest();
  }
else
  {// code for IE6, IE5
  xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
  }
  ```
  
#### 向服务器发送请求  
如需将请求发送到服务器，我们使用 XMLHttpRequest 对象的 `open()` 和 `send()` 方法：  
```
xmlhttp.open("GET","test1.txt",true);
xmlhttp.send();
```
方法	描述  
`open(method,url,async)`
规定请求的类型、URL 以及是否异步处理请求。  
method：请求的类型；GET 或 POST  
url：文件在服务器上的位置  
async：true（异步）或 false（同步）  
send(string)  
将请求发送到服务器。  
string：仅用于 POST 请求
