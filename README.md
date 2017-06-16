# A-front-end
### 前端杂记

---------------
# form表单提交serlize（）
<pre>
<form id="seachForm" action=" url " method="post">
  <input id="one" name="eaml" value="eaml_c" type="checkbox">
  <input type="text" id="mealText" name="content"/>
  </form>
<a id="query"> 提交</a>

<script>
$("#query").click(function(){
    //$("#mealText").val();
   $("#seachForm").submit();
})

</script>
### 或者
 <form id="seachForm">
  First name: <input type="text" name="FirstName" value="Bill" /><br />
  Last name: <input type="text" name="LastName" value="Gates" /><br />
 </form>
 <button id="query"> 提交</button>

<script>
$("#query").click(function(){
    $.ajax({
      type:post,
      url:url,
      data:$("#seachForm").serialize(), //FirstName=Bill&&LastName=Gates
      success:function(data){
        console.log(data);
      }
    })
})
</script>

</code>

* 把序列化的值传给ajax()作为url的参数，轻松使用ajax()提交form表单了，而不需要一个一个获取表单中的值然后传给ajax()
------------------------

-------------------
# @page打印
###### 使用@page规则可以对打印进行更多的设置，比如指定页面的尺寸。页边 距,页眉页脚等，
* @page{size:5.5in 8.5in;}
* 设置纸张大小,5.5英寸宽,8.5英寸高。
* @page{size:A4 landscape;}
* 可以控制打印方向，portrait： 纵向打印地,  landscape: 横向

* 样式将只应用于打印 
<pre>
 @media print {
  /*code*/
 }
</code>
---------------------









