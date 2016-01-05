# Bootstrap
这是bootstrap的学习示例


bootstarpcdn引用方式：
<linkrel="stylesheet"href="//cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css">
bootstarp依赖于jquery
所以在引入bootstarp之前要先引入jquery

第一个bootstrap工程：bootstrap folder01
创建一个web工程，将需要引用的文件复制到文件夹内，使用的是有min的压缩文件，比如bootstrap。min。css。然后创建一个html文件，引用该文件：<link rel="stylesheet" href="bootstrap.min.css">
在html文件的头部添加meta标签，设置页面的宽度。<meta name="viewport" content="width=device-width,initial-scale=1"> width为获取当前设备的宽度，缩放比例为不缩放。
    在body中添加一个导航
<nav class="navbar navbar-default"> //类名为导航，样式为默认 navbarhi导航栏的意思
 
 </nav>
<body>
 <nav class="navbar navbar-inverse navbar-fixed-top" role="navigation"> //类名为导航，样式为inverse ，navbar是导航栏的意思，位置是固定在顶部。
  <div class="container">
   <div class="navbar-header">
    <a href="#" class="navbar-brand">Project Name</a>
   </div>
  </div>
 </nav>
</body>


全局css样式-排版：folder：02
    应用了bootstarp的文件，标签会自动引用bootstarp的样式，显示的效果是跟没有引用的效果是有区别的。对于标题，bootstrap提供一个副标题的标签《small》，使用方法是：<h3>hand<small>欢迎您的到来</small></h3>
    bootstrap将全局的font-size字体大小设置为14px，行高为1.248。这些设置直接赋值body，对于段落这些元素都可以生效。<p>标签还被设置为等高也就是二分之一行高，也就是10px的底部外边距。使用lead类即在标签内定义class=“lead”可以将文本突出显示。
<mark>标签为文本添加背景效果

栅格：folder：03

代码：folder：03 file：condeindex
<!-- code -->
  For example <code>&lt;section&gt;</code> as inline;
  键入<kbd>CMD</kbd>命令
  <!-- 代码框 -->
  <pre>
   Sample text here...;
  </pre>
  <!-- 函数算法 -->
  <var>x</var>=<var>y</var>+<var>z</var>
  <!-- 程序输出 -->
  <samp>hello word!</samp>

表格：folder：03 file：tableindex
<div class="table-responsive">使用该效果把表格包含起来的时候，在显示框缩小时，表格的内容显示不完全，会出现一个滚动条。
<table class="table table-striped table-bordered table-hover table-condensed">
striped 斑马线效果
bordered 边框
hover 鼠标悬停效果
condensed 紧凑
<tr class="active">设置背景颜色为active样式，其他样式有success，info，warning和danger


表单：folder：04 内联表单：index 水平表单：index2 表单支持的控件：index3
  <form role="form">
        <div class="form-group">
            <label>用户名</label>
            <input type="text" class="form-control" placeholder="user">
        </div>
    </form>

placeholder的值是该标签的默认值
使用表单一定要有label这个标签，如果不想该标签显示，可以用.sr-only来隐藏。

下拉列表：
<select  multiple class="form-control">
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
            <option>5</option>
            <option>6</option>
            <option>7</option>
        </select>
multiple 指定所有的选项都在选择框内，也可以不使用该属性
<input class="form-control" type="text" placeholder="hello" disabled>使用disable属性，将输入框设置为不可用
也可以使用readonly来设置标签的只读效果

按钮和图片：folder：04 file：buttonindex
<button type="button" class="btn btn-default">btn-default</button>
可以在class中引用btn-block来使按钮充满父级容器。除了button标签，也可以使用a标签，input标签等应用button的样式
    <img src="G1.jpg" alt="" class="img-circle">  //圆形图片
    <img src="G1.jpg" alt="" class="img-rounded"> //带圆角的正方形
    <img src="G1.jpg" alt="" class="img-thumbnail">//带边框的正方形

下拉菜单：folder：05 index1
使用组件需要引用css、js、jquery3个包。
组件引用需要将基类和子类都引用，并且同一元素只能引用一个组件。引用是需要使用《span》标签承载起来
最后要在body的最后引用js和jq文件，先引用jq再引用js。在使用组件的时候，需要cdn引用css，而不是文件引入：
//cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css
<li role="presentation" class="divider"></li>在下拉菜单中增加一条横线
<li role="presentation" class="dropdown-header">小写1到5</li>在下拉菜单中增加标题
<li class="disabled"><a href="#" role="menuitem">3</a></li>禁止使用该选项

<div class="dropdown pull-right">
            <button class="btn btn-default dropdown-toggle " type="button" data-toggle="dropdown">
                下拉菜单
                <span class="caret"></span>
            </button>
            <ul class="dropdown-menu dropdown-menu-right" role="menu" aria-labelledby="dropdownMenu1">
                <!--<li role="presentation" class="dropdown-header">小写1到5</li>-->
                <li role="presentation" class="divider"></li>
                <li><a href="#" role="menuitem">1</a></li>
                <li><a href="#" role="menuitem">2</a></li>
                <li class="disabled"><a href="#" role="menuitem">3</a></li>
                <li><a href="#" role="menuitem">4</a></li>
                <li><a href="#" role="menuitem">5</a></li>
            </ul>
        </div>


按钮组：folder 05 buttongroup
<div class="btn-group">
            <button type="button" class="btn btn-default"><span class="glyphicon glyphicon-align-left"></span></button>
            <button type="button" class="btn btn-default"><span class="glyphicon glyphicon-align-left"></span></button>
        </div>

需要将按钮组设置为垂直时，将class中的btn-group改为btn-group-vertical即可。如果需要对按钮组的按钮设定大小，可以在class中增加btn-group-*样式。如果要将按钮设置为横向自适应，可以用一个<div class="btn-group btn-group-justified">容器承载起来。

按钮式下拉菜单： folder 05 buttonMenu
<div class="btn-group">
            <button class="btn bg-info dropdown-toggle" data-toggle="dropdown">
                按钮式下拉菜单
                <span class="caret"></span>
            </button>
            <ul class="dropdown-menu" role="menu">
                <li><a href="#">1</a> </li>
            </ul>
        </div>
在按钮处设置btn-*可以设置按钮的大小。在包裹下拉菜单的容器中添加dropup样式的class，可以将下拉菜单变成上拉菜单。

输入框组：folder 05 input
<div class="input-group input-group-lg">
            <span class="input-group-addon">@</span>
            <input type="text" class="form-control" placeholder="username">
        </div>
span可以添加在输入框前面，也可以是后面，或者前后都添加。在承载容器中添加input-group-*可以设置输入框组的高度大小。

导航栏的创建：folder 05 navdemo

<body>
    <div class="container">
        <ul id="mytab" class="nav nav-tabs" role="tablist">
            <li role="presentation" class="active"><a href="#">Home</a> </li>
            <li role="presentation"><a href="#">hello</a> </li>
            <li role="presentation"><a href="#">world</a> </li>
        </ul>
    </div>
<script src="jquery-2.1.4.min.js"></script>
<script src="bootstrap.min.js"></script>
<script>
    $("#mytab a").click(function(e){
        e.preventDefault();
        $(this).tab("show");
    })
</script>
</body>

<script>
    $("#mytab a").click(function(e){
        e.preventDefault();
        $(this).tab("show");
    })
</script>
这条JScript语句可以设置导航栏当前被点击的a标签为活动状态。
也可以在UL中的class添加nav-stacked设置为垂直展示。
nav-justified设置为充满全屏。
在li中添加class="disable"可以设置为无法点击。

导航条的使用：folder 05 nav

媒体对象：folder 05 media
 <div class="media">
                    <a class="media-left media-middle" href="#">
                        <img src="G1.jpg" alt="">
                    </a>
                    <div class="media-body">
                        <h4 class="media-heading">
                            welcome
                        </h4>
                        <p>
                            PPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPP
                            PPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPP
                            PPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPP
                        </p>
                    </div>

<ul class="media-list">
            <li class="media">
                <a class="media-left" href="#">
                    <img src="G1.jpg" alt="">
                </a>
                <div class="media-body">
                    <h4>welcome</h4>
                    <p>welcomewelcomewelcomewelcomewelcomewelcomewelcomewelcomewelcomewelcomewelcomewelcome</p>
                </div>
            </li>
        </ul>

两种创建方法均可以使用。

面板：folder 05 panel

 <div class="panel panel-danger">
           <div class="panel-body">
               hello world!
           </div>
        </div>

        <div class="panel panel-info">
            <div class="panel-heading">
                网站
            </div>
            <div class="panel-body">
                welcome!
            </div>
            <div class="panel-footer panel-warning">
                www.hand.com
            </div>
        </div>


well组件： folder 05 resandwell
<div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" src="https://www.baidu.com">

            </iframe>
        </div>
 <div class="well well-sm">
            look,i am in a well.
        </div>
可以选择16比9和4比3的样式。

分页与标签：folder：05 page


徽章与巨幕：folder：05 badges
巨幕：
<div class="jumbotron">
       <div class="container">
           <h1>hello world!</h1>
           <p></p>
           <p><a class="btn btn-info btn-lg" role="button" href="#">learn more</a> </p>
       </div>
    </div>
徽章：
<div class="container">
        <a href="#">短信消息<span class="badge">30</span></a>
        <button class="btn btn-success" type="button">message<span class="badge">100</span> </button>
    </div>
    <ul class="nav nav-pills" role="rablist">
        <li role="presentation" class="active"><a href="#">Home<span class="badge">10</span> </a> </li>
        <li role="presentation" ><a href="#">lib<span class="badge">101</span> </a> </li>
    </ul>

页头与缩略图： folder05 pageheader

页头：
  <div class="page-header">
       <H1>hand<small> Hello</small></H1>
    </div>
缩略图：
 <div class="row">
        <div class="col-xs-6 col-md-3">
            <a href="#" class="thumbnail">
                <img src="img/1.jpg">
            </a>
        </div>
    </div>

警告框：folder05 Alert
不可以关闭的警告框：
 <div class="alert alert-warning" role="alert">
            Hello大家好！
        </div>
可以关闭的警告框（要引用jq和js文件）：
<div class="alert alert-warning" role="alert">
            <button type="button" class="close" data-dismiss="alert">
                <span aria-disabled="true">&times;</span>
            </button>
            <strong>welcome</strong>
        </div>

带连接的警告框：
 <div class="alert alert-info" role="alert">
            如有问题，请自行
            <a href="https://www.baidu.con" class="alert-link">
                百度
            </a>
        </div>

进度条：folder 05 progres
<div class="progress">
            <div class="progress-bar progress-bar-striped active" role="progressbar" aria-valuemin="0" aria-valuemax="100" style="width: 40%">
                40%
            </div>
        </div>

列表组：folder 05 List
    <div class="container">
        <ul class="list-group">
            <li class="list-group-item"><span class="badge">10</span> 1 </li>
            <li class="list-group-item">2 </li>
            <li class="list-group-item">3 </li>
            <li class="list-group-item">4 </li>
            <li class="list-group-item">5 </li>
        </ul>

        <div class="list-group">
            <a href="#" class="list-group-item">abc</a>
            <a href="#" class="list-group-item">abc</a>
            <a href="#" class="list-group-item">abc</a>
        </div>

    </div>



模态框：folder06 modal
在创建好模态框之后，需要引用jq和js文件，然后再使用
<script>
    $("#mymodal").modal("show");
</script>
调用。
也可以使用
<button type="button" class="btn btn-primary btn-lg" data-toggle="modal" data-target="#myModal">
        启动模态框
    </button>
按钮进行调用，但是data-target的值必须是模态框的父级容器的ID带上#号。
在class中添加fade可以为模态框添加一个效果
可以在模态框的一级和二级承载中添加bs-example-moal-*来设置模态框的大小。

下拉菜单：folder06 dropdown

弹出当前的bootstarp版本，在script中添加一下代码：alert($.fn.tooltip.Constructor.VERSION);

过渡效果：folder06 transitionend


滚动监听：folder06 scrollspy
需要给body添加属性：data-spy="scroll" data-target=".navbar" data-offset="70  导航栏的href要对应标题的ID

标签页：folder06  tabs
可以使用script来指定默认显示的标签页为最后一个：$("#myTab a:last").tab("show");
或者在内容的div中的class中添加active设置默认显示的内容。
$('#myTabs a[href="#profile"]').tab('show')// Select tab by name$('#myTabs a:first').tab('show')// Select first tab$('#myTabs a:last').tab('show')// Select last tab$('#myTabs li:eq(2) a').tab('show')// Select third tab (0-indexed)
也可以在内容的div中的class中添加fade设置过渡效果。

工具提示：folder06 tooltips
该功能是设置鼠标略过之后显示提示。
data-toggle="tooltip"设置触发器
data-placement="bottom"显示位置为底部
 $("#mytooltip").tooltip("show")可以使用script将其设置为自动显示
data-original-title="内容"设置展示的内容，只有title="title"没有内容的时候才会展示data-original-title

需要使用 $('[data-toggle="tooltip"]').tooltip();将提示工具初始化
可以使用data-animation=“false”来取消淡入淡出的效果。

弹出框：folder06 popover
依赖于工具提示插件，也需要初始化。与提示工具不同的是，提示工具是鼠标略过弹出提示，而弹出框是鼠标点击弹出提示。使用弹出框的时候，尽量使用a标签。
data-toggle="popover"设置触发器为弹出框
 title="title"设置标题
 data-content="这里是内容区域" 设置内容
data-trigger="focus"设置点击空白处，弹出框消失
可以使用data-animation=“false”来取消淡入淡出的效果。
data-placement="left"可以设置上下左右弹出方向
初始化：$(".js-popover").popover();

警告框：folder06 alert
当使用 .close 按钮时，它必须是 .alert-dismissible 的第一个子元素，并且在它之前不能有任何文本内容。
只有在按钮中添加了data-dismiss="alert"属性，才会实现警告框的关闭。

按钮：folder06 button
<button type="button" data-loading-text="loading for 3 seconds" class="btn btn-default js-loading-btn">
            Loading state
        </button>
    $(".js-loading-btn").on("click",function(e){
        var btn = $(this).button("loading");
        setTimeout(function(e){
            btn.button("reset")
        },3000)
    })

data-loading-text="loading for 3 seconds"设置按钮按下之后显示的内容。

setTimeout(function(e){
            btn.button("reset")
        },3000)
设置3秒后按钮重置。
autocomplete="off" 可以设置按钮固定在按下的状态，再次点击就弹出

多选按钮组（复选）：
 <div class="btn-group" data-toggle="buttons">
            <label class="btn btn-primary active">
                <input type="checkbox" autocomplete="off" checked>选择1
            </label>
            <label class="btn btn-primary ">
                <input type="checkbox" autocomplete="off" checked>选择2
            </label>
            <label class="btn btn-primary ">
                <input type="checkbox" autocomplete="off" checked>选择3
            </label>
        </div>
注意，这里是用一个div包裹起来按钮组，按钮的实现是用label标签作为按钮的样式，并且使用input作为按钮实体。

单选：<div class="btn-group" data-toggle="buttons">
            <label class="btn btn-primary active">
                <input type="radio" name="options" autocomplete="off" checked>选择1
            </label>
            <label class="btn btn-primary ">
                <input type="radio" name="options" autocomplete="off" >选择2
            </label>
            <label class="btn btn-primary ">
                <input type="radio" name="options" autocomplete="off" >选择3
            </label>
        </div>

注意这里的按钮的name必须是一样的

点击之后按钮名称改变：
        <button type="button" data-complete-text="finish" class="btn btn-primary mybtn" autocomplete="off">
            hello
        </button>
  $(".mybtn").on("click",function(e){
        $(this).button("complete");
    })
data-complete-text="finish"设置改变之后的按钮名称，

collapse（点击之后显示内容框）：folder06 collapse

 <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample">点击查看</a>
        <div class="collapse" id="collapseExample">
           <div class="well">
                Hello
            </div>
        </div>

注意：a标签中的链接要指向文本的div的ID，用well组件包裹起来，会比较好看，当然不需要也可以

<div class="panel-group" id="accordion" role="tablist">
            <div class="panel panel-default">
                <div class="panel-heading" role="tab" id="heading1">
                    <h4 class="panel-title">
                        <a data-toggle="collapse" data-parent="#accordion" href="#collapse1">item1</a>
                    </h4>
                </div>
                <div id="collapse1" class="panel-collapse collapse in" role="tabpanel">
                    <div class="panel-body">
                        Hello1 welcome!
                    </div>
                </div>
            </div>
            <div class="panel panel-default">
                <div class="panel-heading" role="tab" id="heading2">
                    <h4 class="panel-title">
                        <a data-toggle="collapse" data-parent="#accordion" href="#collapse2">item2</a>
                    </h4>
                </div>
                <div id="collapse2" class="panel-collapse collapse" role="tabpanel">
                    <div class="panel-body">
                        Hello2 welcome!
                    </div>
                </div>
            </div>
            <div class="panel panel-default">
                <div class="panel-heading" role="tab" id="heading3">
                    <h4 class="panel-title">
                        <a data-toggle="collapse" data-parent="#accordion" href="#collapse3">item3</a>
                    </h4>
                </div>
                <div id="collapse3" class="panel-collapse collapse" role="tabpanel">
                    <div class="panel-body">
                        Hello3 welcome!
                    </div>
                </div>
            </div>
        </div>


用in将标签在网页打开时就设置为打开

轮播板：folder06 carousel

    <div class="container" id="myCarsoursel">
        <div id="carousel-example-generic" class="carousel slide" data-ride="carousel" data-interval="2000">
            <ol class="carousel-indicators">
                <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
                <li data-target="#carousel-example-generic" data-slide-to="1" class=""></li>
                <li data-target="#carousel-example-generic" data-slide-to="2" class=""></li>
            </ol>
            <div class="carousel-inner" role="listbox">
                <div class="item active">
                    <img src="img/1.jpg">
                    <div class="carousel-caption">
                        <h3>title</h3>
                        <p>描述</p>
                    </div>
                </div>
                <div class="item ">
                    <img src="img/2.jpg">
                </div>
                <div class="item ">
                    <img src="img/3.jpg">
                </div>
            </div>
            <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
                <span class="glyphicon glyphicon-chevron-left"></span>
            </a>
            <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
                <span class="glyphicon glyphicon-chevron-right"></span>
            </a>
        </div>
    </div>

data-interval="2000"设置轮播版图片转换的时间，不设置是默认5秒。但是以该方式实现的自动切换，在刷新页面之后就会不动，需要手动点击才能再次移动。所以建议使用script的方式实现自动播放：
 $(".carousel").carousel({
        interval:2000
    })

附加导航：folder06 affix
































