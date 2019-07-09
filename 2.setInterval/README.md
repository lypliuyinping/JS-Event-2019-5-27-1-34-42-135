## 要求 
    
- 实现一个基础的计时器应用，点击开始按钮开始计时，点击结束按钮结束计时，并把计时的结果显示在上面的输入框中。

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>定时器示例</title>
  </head>
  <body>
  
  <input type="text" id="result">
  
  <input type="button" value="开始" onclick="start()">
  <input type="button" value="结束"  onclick="stop()">
  
  <script>
      // write your code here
    var c=0;
    var t;
    var timer_is_on=0;
    function timedCount(){
        document.getElementById('result').value=c;
        c=c+1;
        t=setTimeout(function(){timedCount()},1000);
    }
    function start(){
        if (!timer_is_on){
            timer_is_on=1;
            timedCount();
        }
    }
    function stop(){
        clearTimeout(t);
        timer_is_on=0;
    }
  </script>
  </body>
  </html>
```
