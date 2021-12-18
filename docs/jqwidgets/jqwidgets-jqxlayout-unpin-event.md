# jqwidgets jxllayout unpin 事件

> 原文:[https://www . geesforgeks . org/jqwidgets-jqxlayout-unpin-event/](https://www.geeksforgeeks.org/jqwidgets-jqxlayout-unpin-event/)

***jQWidgets*** 是一个 JavaScript 框架，用于为 PC 和移动设备制作基于 web 的应用程序。它是一个非常强大、优化、独立于平台并且得到广泛支持的框架。 ***jqxLayout*** 用于表示 jQuery 小部件，该部件用于创建具有嵌套、调整大小、固定、取消固定和闭合面板的复杂布局。

当一组指定的 jqxLayout 小部件被取消固定时，触发**事件。**

****语法:****

```
$('#jqxLayout').on('unpin', function (event) {
  // Code Section
});
```

****链接文件:**从给定链接下载 https://www.jqwidgets.com/download/。在 HTML 文件中，找到下载文件夹中的脚本文件。**

> <link rel="”stylesheet”" href="”jqwidgets/styles/jqx.base.css”" type="”text/css”"> **<脚本类型=“text/JavaScript”src =“scripts/jquery . js”></脚本>
> <脚本类型=“text/JavaScript”src =“jqwidgets/jqxcore . js”></脚本>
> <脚本类型=“text/JavaScript”src =“jqwidgets/jqxmenu . js”>**

****示例:**下面的示例说明了 jQWidgets jqxLayout***unpin***事件。**

## **超文本标记语言**

```
<!DOCTYPE html>
<html lang="en">

<head>
    <link rel="stylesheet" 
          href="jqwidgets/styles/jqx.base.css" 
          type="text/css"/>
    <script type="text/javascript" 
            src="scripts/jquery.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxcore.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxbuttons.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxribbon.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqxlayout.js">
    </script>
    <script type="text/javascript" 
            src="jqwidgets/jqx-all.js">
    </script>
</head>

<body>
    <center>
        <h1 style="color:green;">
            GeeksforGeeks
        </h1>
        <h3>
            jQWidgets jqxLayout unpin Event
        </h3>
        <div id="jqx_Layout">
            <div data-container="A1">
                <ol>
                    <li>GeeksforGeeks</li>
                    <li>Amazon</li>
                    <li>Capgemini</li>
                </ol>
            </div>
            <div data-container="A2">
                <li>It is a computer science portal.</li>
            </div>
            <div data-container="A3">
                <li>It is a eCommerce platform.</li>
            </div>
            <div data-container="A4">
                <li>It is a service based company.</li>
            </div>
        </div>
        <div id="log"></div>
        <script type="text/javascript">
            $(document).ready(function () {
                var layout = [{
                    items: [{
                        items: [{
                            contentContainer: 'A1',
                            type: 'layoutPanel',
                            title: 'List of Company'
                        }],
                        width: 80,
                        type: 'autoHideGroup',
                        alignment: 'left'
                    }, {
                        items: [{
                            items: [{
                                contentContainer: 'A2',
                                type: 'documentPanel',
                                title: 'GeeksforGeeks',
                            }, {
                                contentContainer: 'A3',
                                type: 'documentPanel',
                                title: 'Amazon',
                            }, {
                                contentContainer: 'A4',
                                type: 'documentPanel',
                                title: 'Capgemini',
                            }],
                            type: 'documentGroup',
                            height: 200,
                        },],
                        width: 370,
                        orientation: 'vertical',
                        type: 'layoutGroup',
                    }],
                    orientation: 'horizontal',
                    type: 'layoutGroup',
                }];
                $('#jqx_Layout').jqxLayout({
                    width: 450,
                    height: 200,
                    layout: layout
                });
                $('#jqx_Layout').on('unpin', function () {
                  $("#log").html('The group has been unpinned.');
                });
            });
        </script>
    </center>
</body>

</html>
```

****输出:****

**![](img/5cdb37dc6a19227ae5c2ac23369cb42e.png)**

****参考:**[https://www . jqwidgets . com/jquery-widgets-documentation/documentation/jqxlayout/jquery-layout-API . htm？搜索=](https://www.jqwidgets.com/jquery-widgets-documentation/documentation/jqxlayout/jquery-layout-api.htm?search=)**