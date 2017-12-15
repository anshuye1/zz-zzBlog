# zz-zzBlog
zz@zz的博客
<br>
<h1>1.如何理解和熟练运用js中的call及apply？</h1>
本身不难理解，看下MDN就知道了，但是不常用，遇到了，还要脑回路回转下。或者时间长了，还是要确定下去看下文档，<br>
为了方便记忆：<br>
  猫吃鱼，狗吃肉，奥特曼打小怪兽。<br>
  有天狗想吃鱼了<br>
  猫.吃鱼.call(狗，鱼)<br>
  狗就吃到鱼了<br>
  猫成精了，想打怪兽<br>
  奥特曼.打小怪兽.call(猫，小怪兽)<br>
  就这样记住了。<br>
作者：寇云
链接：https://www.zhihu.com/question/20289071/answer/258643285
来源：知乎

<div>

  function Animal(){
    this.name = "Animal";
    this.showName = function(){
        alert(this.name);
    }
  } 

  function Cat(){
      this.name = "Cat";    
  }
  
  var animal = new Animal();
  
  var cat = new Cat();
 

  //通过call或apply方法，将原本属于Animal对象的showName()方法交给对象cat来使用了。
  
  //输入结果为"Cat" 
  
  animal.showName.call(cat,",");
  
  //animal.showName.apply(cat,[]); 
  
</div>
call和apply，这两个方法基本上是一个意思，区别在于 call 的第二个参数可以是任意类型，而apply的第二个参数必须是数组，也可以是arguments

<h1></h1>
