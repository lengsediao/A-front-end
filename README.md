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

----------------------

# IE、火狐、谷歌浏览器下兼容统一select样式

<pre>
  select{
*    //谷歌、火狐边框不一样，复写一下；
    border:1px solid #ccc;
*    将默认的select样式清除  
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none;
*    选择图片
    background: url("hshfImg/mark_bot.png") no-repeat scroll 150px center transparent;
*    给小箭头留位置，避免覆盖文字；
    padding-right: 34px;
    color: #8e8e8e;
  }
* 清除ie下拉箭头默认样式，隐藏；
  select::-ms-expand { display: none; }
  </code>

* 给小箭头留位置，避免覆盖文字；



