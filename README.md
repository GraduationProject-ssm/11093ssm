# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 11093ssm智能化小区管理系统

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Kp48e9EtU?p=135)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

智能化小区管理系统工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。智能化小区管理系统的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示住户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、住户管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3住户管理实体图

2、活动信息管理实体图如图4-4所示：

![](/md/blog.015.png)

`   `图4-4活动信息管理实体图

3、投诉处理管理系统实体图如图4-5所示：

![](/md/blog.016.png)

`   `图4-5投诉处理管理系统实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 huodongbaoming表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|huodongbiaoti|varchar|50|` `default NULL|
|leixing|varchar|50|` `default NULL|
|huodongshijian|varchar|50|` `default NULL|
|huodongdidian|varchar|50|` `default NULL|
|baomingshijian|varchar|50|` `default NULL|
|zhuhuzhanghao|varchar|50|` `default NULL|
|zhuhuxingming|varchar|50|` `default NULL|


表4-2 huodongxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|huodongbiaoti|varchar|50|default NULL|
|leixing|varchar|50|default NULL|
|fengmiantu|varchar|50|default NULL|
|huodongdidian|varchar|50|default NULL|
|kebaorenshu|varchar|50|default NULL|
|huodongneirong|varchar|50|default NULL|

表4-3：tousuchuli表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|biaotimingcheng|varchar|50|default NULL|
|leixing|varchar|50|default NULL|
|chulifankui|varchar|50|default NULL|
|chulijindu|varchar|50|default NULL|
|gengxinshijian|varchar|50|default NULL|
|zhuhuzhanghao|varchar|50|default NULL|
|zhuhuxingming|varchar|50|default NULL|
|loufanghao|varchar|50|default NULL|


表4-4：tousufankui表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|biaotimingcheng|varchar|50|default NULL|
|leixing|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|tousuneirong|varchar|50|default NULL|
|tousushijian|varchar|50|default NULL|
|cheweibianhao|varchar|50|default NULL|
|zhuhuzhanghao|varchar|50|default NULL|
|zhuhuxingming|varchar|50|default NULL|

# 5统详细设计
## 5.1前台首页功能模块
智能化小区管理系统，在系统首页可以查看首页、活动信息、论坛交流、公告信息、我的、跳转到后台、在线物业等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1前台首页功能界面图



`    `住户注册，在住户注册页面可以填写住户账号、住户姓名、性别、楼房号、联系电话、身份证等信息进行注册，如图5-2所示。

![](/md/blog.018.png)

图5-2 住户注册界面图



`   `登录，在登录页面通过填写账号、密码等信息完成登录，如图5-3所示。

![](/md/blog.019.png)

图5-3 住户登录界面图

个人中心：在个人中心页面通过填写住户账号、住户姓名、性别、头像、楼房号、联系电话、身份证等信息进行操作，如图5-4所示。

![](/md/blog.020.png)

图5-4个人中心界面图

活动信息：在活动信息页面通过填写活动标题、类型、封面图、活动时间、活动地点、可报人数、活动内容、发布日期等信息进行操作，如图5-5所示。


![](/md/blog.021.png)

图5-5活动信息界面图

## 5.2管理员功能模块
管理员登录，通过填写注册时输入的住户名、密码进行登录，如图5-6所示。

![](/md/blog.022.png)

图5-6管理员登录界面图




管理员登录进入智能化小区管理系统可以查看个人中心、住户管理、活动信息管理、活动报名管理、投诉反馈管理、投诉处理管理、物业费管理、论坛交流、系统管理等信息。如图5-7所示。

![](/md/blog.023.png)

图5-7管理员首页界面图





住户管理，管理员通过在住户管理页面中可以查看住户账号、住户姓名、性别、头像、楼房号、联系电话、身份证等内容进行修改、删除和查看等操作，如图5-8所示。

![](/md/blog.024.png)

图5-8住户管理界面图

活动信息管理，管理员通过在活动信息管理页面中可以查看活动标题、类型、封面图、活动时间、活动地点、可报人数、活动内容、发布日期等内容进行修改、删除和查看等操作，如图5-9所示。


![](/md/blog.025.png)

图5-9活动信息管理界面图

轮播图管理管理，在轮播图管理管理页面中可以查看名称、值、操作等信息，并可根据需要对轮播图管理管理进行修改或删除等操作，如图5-10所示。

![](/md/blog.026.png)

图5-10 轮播图管理管理界面图

公告信息，管理员通过在公告信息页面中可以查看标题、简介、图片、内容、操作等信息，并可根据需要对公告信息进行修改或删除等详细操作，如图5-9所示。

![](/md/blog.027.png)

图5-9公告信息界面图

活动报名管理，管理员通过在活动报名管理页面中可以查看活动标题、类型、活动时间、活动地点、报名时间、住户账号、住户姓名、楼房号、联系电话、是否审核、审核回复等内容，并且根据需要对活动报名管理进行详情，修改或删除等详细操作，如图5-10所示。

![](/md/blog.028.png)

图5-10活动报名管理界面图

投诉反馈管理，在投诉反馈管理页面中可以查看标题名称、类型、图片、投诉内容、投诉时间、住户账号、住户姓名、楼房号、联系电话、是否审核、审核回复等内容，并且根据需要对投诉反馈管理进行详情，修改或删除等详细操作，如图5-11所示。

![](/md/blog.029.png)

图5-11投诉反馈管理界面图

## 5.3住户功能模块
住户登录进入智能化小区管理系统可以查看个人中心、活动报名管理、投诉反馈管理、物业费管理、我的收藏管理等内容。

个人中心，在个人中心页面中通过填写原密码、新密码、确认密码等信息，还可以根据需要对个人中心进行修改操作，如图5-12所示。

![](/md/blog.030.png)

图5-12个人中心界面图

活动报名管理，在活动报名管理页面中可以查看活动标题、类型、活动时间、活动地点、报名时间、住户账号、住户姓名、楼房号、联系电话、是否审核、审核回复等信息，并且根据需要对活动报名管理系统进行查看删除等其他详细操作，如图5-13所示。

![](/md/blog.031.png)

图5-13活动报名管理界面图

投诉反馈管理，在投诉反馈管理页面中可以查看标题名称、类型、图片、投诉内容、投诉时间、住户账号、住户姓名、楼房号、联系电话、是否审核、审核回复等信息，并且根据需要对投诉反馈管理进行查看删除等其他详细操作，如图5-14所示。

![](/md/blog.032.png)

图5-14投诉反馈管理界面图














