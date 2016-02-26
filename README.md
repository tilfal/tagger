这是一个基于标签的文档管理工具，类似[Tabbles](http://www.appinn.com/tagspaces/)、[TaggedFrog](http://www.appinn.com/taggedfrog/)、[Tabbles](http://tabbles.net/)等

# 依赖
tagger运行在python 2.7 + wxpython 3.0环境中

# 功能介绍
1. 双击start.bat可以运行tagger<br>
（默认Python安装在c:\Python27目录下）
<hr>
1. 将目录拖放到窗口主下角的列表框中，可以将此目录加入管理列表。<br>
加入后有两种模式：一、管理该目录的子目录和子文件；二、管理该目录下递归搜索出来的所有文件<br>
（需要修改tagger.py文件中的ADD_ITEM_RECURSION设置）<br>
加入的子项在右边列表中显示，并被打上[NEW]标签
1. 在左下角单选或多项目录，点击Delete键，可以取消对选中目录的管理<br>
（此时不会删除该目录下的子项）<br>
1. 焦点在左下角列表时，点击F5刷新选中目录下的管理项<br>
如果列表中存在而实际文件不存在，则对列表项打上[DEL]标签；如果实际文件存在而列表中不存在，则加入新列表项，打[NEW]标签<br>
（如左下角列表中未选中目录，则不做操作）
<hr>
1. 单选或多选右边列表项，点击Delete键，可删除列表项
1. 选中右边列表项，点击F2可以设置标签<br>
在对话框中输入字符串，+表示设置标签，-表示取消标签，多个标签间用;分割
1. 选中右边列表项，点击F5可以根据文件名后缀自动设置标签<br>
在_ext.txt文件中可以设置文件名后缀类别，可以将多种后缀重定义，比如.mkv,.rm,.rmvb都是movie
1. 选中右边列表项，点击F11可以设置或取消[NEW]标签
1. 选中右边列表项，点击F12可以设置或取消[DEL]标签
1. 在右边列表中可以直接编辑某些单元格<br>
在_item.txt中第一行定义列头，如果某一列为ro，则不能编辑
<hr>
1. 左上角显示的是所有的标签和包含此标签的列表项<br>
点击某个标签可以按标签进行过滤
1. 工具栏中可以输入逻辑表达式，对当前显示的列表项进行二次过滤<br>
某一列用row[?]表示，从0开始<br>
支持Python语法的任意逻辑表达式
<hr>
1. 单选右边列表中一行，点击F6可以打开对应的目录/文件
<hr>
1. 支持点击列头排序
1. 如需扩展列，可直接修改_item.txt中的第一行，自定义列<br>
（前四列必须依次是name,path,created,tag）
<hr>
1. 以上的操作对应的按键，在tagger窗口的标题中可以看到
