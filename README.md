> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

本系统一共管理员，用户两个角色。

管理员登录进入本系统操作的功能包括对商品信息，订单投诉信息，商品评价信息，商品收藏信息，会员等级信息，商品订单信息等进行管理

用户登录进入本系统操作的功能包括收藏喜欢的商品以及购买商品，查看商品购买信息，管理购物车，管理订单投诉等

# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA;

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS;

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目

6.数据库：MySql5.7/8.0等版本均可；

# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery

# 使用说明

1.使用Navicati或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件；

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目；

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq

源码地址：[http://www.codegym.top](http://www.codegym.top/)



# 运行截图

## 文档截图

![img](https://img-blog.csdnimg.cn/img_convert/7fcdbeda849911aba0930649c2cb7b5e.png)

![img](https://img-blog.csdnimg.cn/img_convert/accfd6d9a0f3e68f4e53c170f5b040d3.png)

## 项目截图

![springboot256基于springbooe的游戏交易系统9](https://img-blog.csdnimg.cn/img_convert/315e363ece57b8c60727f24318d072bd.png)

![springboot256基于springboote的游戏交易系统7](https://img-blog.csdnimg.cn/img_convert/cff1157dc32ecb0fb3b88c2f21b1e35c.png)

![springboot256基于springboote的游戏交易系统8](https://img-blog.csdnimg.cn/img_convert/f0e10fab5626e493d284b6c17d653e62.png)

![springboot256基于springboote的游戏交易系统10](https://img-blog.csdnimg.cn/img_convert/4ec8a44578ab766f01cc0b0a5a0afab2.png)

![springboot256基于springbootvue的游戏交易系统4](https://img-blog.csdnimg.cn/img_convert/0798fc0da4e22d4abc4df4fd66e99d6d.png)

![springboot256基于springbootvue的游戏交易系统5](https://img-blog.csdnimg.cn/img_convert/5fe10de0968e9c62ca75df66054c7a2d.png)

![springboot256基于springbootvue的游戏交易系统6](https://img-blog.csdnimg.cn/img_convert/26faa73656843825b79d375bdb81137b.png)

![db9f52c194ca4417810a1085dfa5c2b7](https://img-blog.csdnimg.cn/img_convert/97e3d0de36c47bc106d33597773ee998.png)

### 代码

```
    public static long getThirtyDaysMillisFromLocalDate() {
        // 获取当前日期
        LocalDate today = LocalDate.now();
        LocalDate thirtyDaysAgo = today.minusDays(30);
        // 将 LocalDate 转换为系统默认时区的 ZonedDateTime（午夜）
        ZonedDateTime zonedDateTime = thirtyDaysAgo.atStartOfDay(ZoneId.systemDefault());
        // 将 ZonedDateTime 转换为 Instant，并获取毫秒数
        Instant instant = zonedDateTime.toInstant();
        return instant.toEpochMilli();
    }

    private static long getMillisOfHour() {
        // 使用系统默认时区
        ZoneId defaultZoneId = ZoneId.systemDefault();

        // 获取当前时间
        LocalDateTime now = LocalDateTime.now();

        // 将当前时间调整为下一个小时的00分00秒
        LocalDateTime nextHourStart = now.withSecond(0).withNano(0);

        // 将LocalDateTime转换为毫秒数
        ZonedDateTime zonedDateTime = nextHourStart.atZone(defaultZoneId);
        return zonedDateTime.toInstant().toEpochMilli();
    }
```
