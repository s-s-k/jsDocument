# ECMAScript 函数概述
### 什么是函数
* 函数是一组可以随时运行的语句。  
* 函数通过这样方式声明：关键字function、函数名、参数、以及待执行代码。  
基本语法：  
<pre><code>
function functionName(arg0, arg1,... argN){  
  statuments  
}
</code></pre>

* 函数可以通过函数名加上括号中的参数进行调用，例如：
<pre>
<code>
say("Ravid", "hello")
</code>
</pre>

* 函数返回值： 函数通过return语句来返回值。当没有返回值时，默认返回undefined。当函数执行return语句后函数停止，不再执行之后的代码。

### ECMAScript arguments 对象
* arguments 对象
 在函数代码中使用特殊对象arguments， 可无需明确参数名成，就能访问参数。

 <pre>
 <code>
 function say(){
    if(arguments[0]==='bye'){
      return;
    }
    alert(arguments[0]);
 }
 </code>
 </pre>

* 检测函数参数个数
 可通过查看arguments.length的来查看参数个数。与其他程序设计语言不同，ECMAScript不会验证传递给函数的参数个数是否等于函数定义的参数个数。函数可以接受任意多个参数（最多255个），而不引发错误，遗漏的参数将以undefined传递给函数。

* 模拟函数重载
用arguments对象判断传递给函数的个数即可模拟重载。

<pre>
<code>
function add(){
  if (arguments.length===1)
    return arguments[0];
  if (arguments.length===2)
    return arguments[0]+arguments[1];
}
</code>
</pre>

## ECMAScript Function 对象

### Function对象
* 在ECMAScript 中函数是功能完整的对象。Function类可以表示开发者定义的任何函数。用function直接创建函数语法如下：  
<code>
var functionName = new function(arg1, arg2,arg3, ...argN,function_body )
</code>  
在上面形式中，每一个arg都是一个参数，最后一个参数是函数主体即要执行的代码，这些参数必须是字符串。 
<code>
var functionName = function(arg1, arg2, ...argN){
  function_body;
}
</code>

