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
### 实现显示NOte的实现戳，首先时间戳就是根据当前系统时间生成的一组随机数字，作为对数据唯一性的一种判断依据。避免了重复修改数据所带来的错误，先获取，用Timestamp now = new Timestamp(System.currentTimeMillis());//获取系统当前时间，再对时间戳进行返回，这时客户端就需要对时间戳做出处理，将时间戳转换为标准的时间格式，格式在NoteEditor的UpdateNote中进行修改，映射到数据库的PROJECTTION,绑定数据列的dataclolumn，还有绑定的ViewId，然后再listItem.xml文件添加时间戳的TEXTVIEW。

![image](https://github.com/Dabiuliu/notpad/blob/master/app/src/main/res/123/3.png)
