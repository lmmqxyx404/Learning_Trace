# 1.import
use src tag to import the resource
```
<script src="/js/jquery-3.4.1.min.js "></script>
```

## validate
You can write down __console__ in your browser.
可以在浏览器 __console__ 中输入
```
$.fn.jquery
```

# 2.pay attention to the __ready__ function
It is neccessary to put the main ___code___ in the <u><strong>ready</strong></u> function since most functions are executed after the DOM tree is rendered.
绝大多数操作需在文档就绪后才执行，因此jquery的代码<u>入口</u>就在这个函数中
```
$(document).ready(function(){ main code }
```