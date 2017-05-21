# NotePad
This is an AndroidStudio rebuild of google SDK sample NotePad
======================
实现了notpad2两个基本功能
--------------------
1.实现Note的搜索功能
--------------------
### 实现搜索功能，首先看下如何配置搜索的XML配置文件。先命名配置文件名称为searchable.xml，保存在res/xml文件夹中。增加一个搜索的Activity，然后需要设置搜索框的文本，并且应该增加一个hint的提示文本信息，在handleIntent方法中，当按下搜索按钮，系统就会自动发送Intent，action是Intent.ACTION_SEARCH，然后通过intent.getStringExtra(SearchManager.QUERY)，重写onQueryTextChange方法来实现搜索。通过匹配对应的title和time完成搜索。

![image](https://github.com/Dabiuliu/notpad/blob/master/app/src/main/res/123/1.png)
![image](https://github.com/Dabiuliu/notpad/blob/master/app/src/main/res/123/2.png)

2.显示Note的时间戳
-------------------
### 实现显示NOte的实现戳，首先时间戳就是根据当前系统时间生成的一组随机数字，为此，要获取，

![image](https://github.com/Dabiuliu/notpad/blob/master/app/src/main/res/123/3.png)
