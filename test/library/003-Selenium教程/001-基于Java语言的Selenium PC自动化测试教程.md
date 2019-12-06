#基于Java语言的Selenium PC自动化测试教程

### Part.1 Selenium 介绍与环境搭建

- #####1.安装JDK8  官网下载地址：https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

注意windows版本与mac版本，如果已经安装JDK8略过此步。

> Java环境分JDK和JRE ，JDK就是Java Development Kit。简单的说JDK是面向开发人员使用的SDK，它提供了Java的开发环境和运行环境。JRE是Java Runtime Enviroment是指Java的运行环境，是面向 Java 程序的使用者。

- ##### 2.安装IDEA 官网下载地址：https://www.jetbrains.com/idea/  

Idea安装完成之后需要激活码激活（从网址中下载激活http://idea.medeming.com/jetbrains/），如下：

```java
T3ACKYHDVF-eyJsaWNlbnNlSWQiOiJUM0FDS1lIRFZGIiwibGljZW5zZWVOYW1lIjoi5bCP6bifIOeoi+W6j+WRmCIsImFzc2lnbmVlTmFtZSI6IiIsImFzc2lnbmVlRW1haWwiOiIiLCJsaWNlbnNlUmVzdHJpY3Rpb24iOiIiLCJjaGVja0NvbmN1cnJlbnRVc2UiOmZhbHNlLCJwcm9kdWN0cyI6W3siY29kZSI6IklJIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wNi0xMyIsInBhaWRVcFRvIjoiMjAyMC0wNi0xMiJ9LHsiY29kZSI6IkFDIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wNi0xMyIsInBhaWRVcFRvIjoiMjAyMC0wNi0xMiJ9LHsiY29kZSI6IkRQTiIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDYtMTMiLCJwYWlkVXBUbyI6IjIwMjAtMDYtMTIifSx7ImNvZGUiOiJQUyIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDYtMTMiLCJwYWlkVXBUbyI6IjIwMjAtMDYtMTIifSx7ImNvZGUiOiJHTyIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDYtMTMiLCJwYWlkVXBUbyI6IjIwMjAtMDYtMTIifSx7ImNvZGUiOiJETSIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDYtMTMiLCJwYWlkVXBUbyI6IjIwMjAtMDYtMTIifSx7ImNvZGUiOiJDTCIsImZhbGxiYWNrRGF0ZSI6IjIwMTktMDYtMTMiLCJwYWlkVXBUbyI6IjIwMjAtMDYtMTIifSx7ImNvZGUiOiJSUzAiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiUkMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiUkQiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiUEMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiUk0iLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiV1MiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiREIiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiREMiLCJmYWxsYmFja0RhdGUiOiIyMDE5LTA2LTEzIiwicGFpZFVwVG8iOiIyMDIwLTA2LTEyIn0seyJjb2RlIjoiUlNVIiwiZmFsbGJhY2tEYXRlIjoiMjAxOS0wNi0xMyIsInBhaWRVcFRvIjoiMjAyMC0wNi0xMiJ9XSwiaGFzaCI6IjEzMzgwMDA0LzAiLCJncmFjZVBlcmlvZERheXMiOjcsImF1dG9Qcm9sb25nYXRlZCI6ZmFsc2UsImlzQXV0b1Byb2xvbmdhdGVkIjpmYWxzZX0=-nTBuZDiAOuM4IHXNkS7GbCvZVZFo4EcHf9hHzfhaPYsaCGQjuCVJFEboopbPuEHn16yT9Zvf7yRuM5WGlGmpcOJnWLpCmGm65S6wHtZdX0kfSNIqnqdS1MhIHpftsAGxSswuQksrm09tltbO4nATeavGs1BIMafsCJVen+BvDFvYL7+3crkRI7AwdyMb2miLLYJcEVPhiVKZnzJUzT9uA8/4Q02BqsvX5oSJg8cLw3w7Cd0ISrn1i8uENe/1z3T/Ede0STM7eOekFaVEdO9cgzYME3iIFzi2TZXMSqIuBpJqF4NFb6M0039tEGy6EHqcksMyDTdCAASquqcDcHrUUA==-MIIElTCCAn2gAwIBAgIBCTANBgkqhkiG9w0BAQsFADAYMRYwFAYDVQQDDA1KZXRQcm9maWxlIENBMB4XDTE4MTEwMTEyMjk0NloXDTIwMTEwMjEyMjk0NlowaDELMAkGA1UEBhMCQ1oxDjAMBgNVBAgMBU51c2xlMQ8wDQYDVQQHDAZQcmFndWUxGTAXBgNVBAoMEEpldEJyYWlucyBzLnIuby4xHTAbBgNVBAMMFHByb2QzeS1mcm9tLTIwMTgxMTAxMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxcQkq+zdxlR2mmRYBPzGbUNdMN6OaXiXzxIWtMEkrJMO/5oUfQJbLLuMSMK0QHFmaI37WShyxZcfRCidwXjot4zmNBKnlyHodDij/78TmVqFl8nOeD5+07B8VEaIu7c3E1N+e1doC6wht4I4+IEmtsPAdoaj5WCQVQbrI8KeT8M9VcBIWX7fD0fhexfg3ZRt0xqwMcXGNp3DdJHiO0rCdU+Itv7EmtnSVq9jBG1usMSFvMowR25mju2JcPFp1+I4ZI+FqgR8gyG8oiNDyNEoAbsR3lOpI7grUYSvkB/xVy/VoklPCK2h0f0GJxFjnye8NT1PAywoyl7RmiAVRE/EKwIDAQABo4GZMIGWMAkGA1UdEwQCMAAwHQYDVR0OBBYEFGEpG9oZGcfLMGNBkY7SgHiMGgTcMEgGA1UdIwRBMD+AFKOetkhnQhI2Qb1t4Lm0oFKLl/GzoRykGjAYMRYwFAYDVQQDDA1KZXRQcm9maWxlIENBggkA0myxg7KDeeEwEwYDVR0lBAwwCgYIKwYBBQUHAwEwCwYDVR0PBAQDAgWgMA0GCSqGSIb3DQEBCwUAA4ICAQAF8uc+YJOHHwOFcPzmbjcxNDuGoOUIP+2h1R75Lecswb7ru2LWWSUMtXVKQzChLNPn/72W0k+oI056tgiwuG7M49LXp4zQVlQnFmWU1wwGvVhq5R63Rpjx1zjGUhcXgayu7+9zMUW596Lbomsg8qVve6euqsrFicYkIIuUu4zYPndJwfe0YkS5nY72SHnNdbPhEnN8wcB2Kz+OIG0lih3yz5EqFhld03bGp222ZQCIghCTVL6QBNadGsiN/lWLl4JdR3lJkZzlpFdiHijoVRdWeSWqM4y0t23c92HXKrgppoSV18XMxrWVdoSM3nuMHwxGhFyde05OdDtLpCv+jlWf5REAHHA201pAU6bJSZINyHDUTB+Beo28rRXSwSh3OUIvYwKNVeoBY+KwOJ7WnuTCUq1meE6GkKc4D/cXmgpOyW/1SmBz3XjVIi/zprZ0zf3qH5mkphtg6ksjKgKjmx1cXfZAAX6wcDBNaCL+Ortep1Dh8xDUbqbBVNBL4jbiL3i3xsfNiyJgaZ5sX7i8tmStEpLbPwvHcByuf59qJhV/bZOl8KqJBETCDJcY6O2aqhTUy+9x93ThKs1GKrRPePrWPluud7ttlgtRveit/pcBrnQcXOl1rHq7ByB8CFAxNotRUYL9IF5n3wJOgkPojMy6jetQA5Ogc8Sm7RG6vg1yow==

```



- ##### 3.安装maven，此文件为独立压缩文件，找王岩要。

  > maven可以对项目依赖的jar包进行管理，可以让项目保持基本的依赖，排除冗余jar包，并且非常轻松的对依赖的jar包进行版本升级。这些仅仅是Maven最基本的功能，它可以在这基础上对项目进行清理、编译、测试、打包、发布等等构建项目的工作。 

![](assets/003/maven安装.png)

- ##### 4.使用Maven构建Selenium

打开IDEA -> File -> Project ->

![maven](assets/003/maven.jpg)

点击Next

![坐标](assets/003/project.jpg)

点击Next

![项目名称](assets/003/project2.jpg)

点击Finish 完成创建项目



- ##### 4.修改pom.xml文件 加入Seleunim依赖

> 目前Java项目 比较流行的构建方式有2中，一种使用Maven，另一种为Gradle。
>
> Selenium测试直接运行在浏览器中，就像真正的用户在操作一样。其实就是模拟浏览器操作。



加入如下依赖：

```java
    <dependencies>
        <!--> selenium 依赖<-->
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>3.4.0</version>
        </dependency>
    </dependencies>
      
```



- #####5.浏览器驱动

当selenium升级到3.0之后，对不同的浏览器驱动进行了规范。如果想使用selenium驱动不同的浏览器，必须单独下载并设置不同的浏览器驱动。Chrome浏览器版本对驱动的版本也有要求一般大版本号对应即可。
各浏览器下载地址：
Firefox浏览器驱动：[geckodriver](https://github.com/mozilla/geckodriver/releases)
Chrome浏览器驱动：[chromedriver](https://sites.google.com/a/chromium.org/chromedriver/home)      [taobao备用地址](https://npm.taobao.org/mirrors/chromedriver)
IE浏览器驱动：[IEDriverServer](http://selenium-release.storage.googleapis.com/index.html)
Edge浏览器驱动：[MicrosoftWebDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
Opera浏览器驱动：[operadriver](https://github.com/operasoftware/operachromiumdriver/releases)
PhantomJS浏览器驱动：[phantomjs](http://phantomjs.org/)
注：部分浏览器驱动地址需要科学上网。

完成上述操作之后基本的selenium环境配置完成。后续针对移动端自动化套路是一样的。



- ##### 6.浏览器、WebDriver及简单示例

我们完成一个简单的DEMO，通过控制WebDriver，打开Chrome，之后打开www.baidu.com网址，输入搜索内容“腾讯”并点击搜索，搜索内容弹出后点击分页中的第2页并显示第2页内容。

示例代码如下：

```java
package cc.tframe.part1;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

import java.util.List;

/**
 * <br>@see
 * <br>@author chenghao
 * <br>@version v1.0 2019-11-18 5:32 下午
 **/
public class main1 {
    public static void main(String[] args) throws InterruptedException {
        //加载相应的驱动，第二个参数是驱动路径（使用你自己的路径）
        System.setProperty("webdriver.chrome.driver", "/Users/chenghao/cmproject/java/ch-frame/cc-tframe/src/main/resources/chromedriver");

        //创建ChromeDriver对象
        WebDriver driver = new ChromeDriver();

        //全屏放大窗口
        driver.manage().window().maximize();

        //访问www.baidu.com
        driver.get("https://www.baidu.com");

        //让线程休眠2秒
        Thread.sleep(3000);

        //使用xpath方式查找元素，并输入"腾讯"
        driver.findElement(By.xpath("//*[@id='kw']")).sendKeys("腾讯");

        //让线程休眠2秒
        Thread.sleep(3000);

        // 点击"搜索"按钮
        driver.findElement(By.id("su")).click();
        //让线程休眠3秒
        Thread.sleep(3000);

        //获取分页元素，因为分页元素会查找出很多相似的内容所以我们需要用数组来接收数据
        List<WebElement> list = driver.findElements(By.xpath("//*[@id=\"page\"]/a[1]"));
        //确认第一个元素就是第2页，然后点击
        if (list.get(0).findElement(By.className("pc")).getText().equals("2")) {
            list.get(0).click();
        }
        //让线程休眠5秒
        Thread.sleep(5000);

        // 关闭浏览器窗口
        driver.close();

    }
}

```

> ##### 作业：将环境安装完成，并开发完成简单示例程序



-----------------------

### Part.2 Java语言基础

> 在使用Selenuim过程中，我将基于https://www.runoob.com/java/java-basic-syntax.html的教程讲解相关Java基础。

- #####基础

主方法入口：所有的 Java 程序由 **public static void main(String []args)** 方法开始执行。

对象：对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有（也可叫属性或字段）：颜色、名字、品种；行为有：摇尾巴、叫、吃等。

类：类是一个模板，它描述一类对象的行为和状态，也就是说没有类就没有对象。

方法：方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。



- ##### 对象

  声明：声明一个对象，包括对象名称和对象类型。

  实例化：使用关键字new来创建一个对象。

  初始化：使用new创建对象时，会调用构造方法初始化对象。

  ```java
  String str = new String();
  ```

  

- #####基本数据类型

| byte                   | 0       |
| ---------------------- | ------- |
| short                  | 0       |
| int                    | 0       |
| long                   | 0L      |
| float                  | 0.0f    |
| double                 | 0.0d    |
| char                   | 'u0000' |
| String (or any object) | null    |
| boolean                | false   |

- ##### 修饰符

  Java中可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。

  default (即默认）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。

  private : 在同一类内可见。使用对象：变量、方法。 

  **public : 对所有类可见。使用对象：类、接口、变量、方法。我们先学public，其余的先不用管**

  protected : 对同一包内的类和所有子类可见。使用对象：变量、方法。 

- ##### 包

  把功能相似或相关的类或接口组织在同一个包中，方便类的查找和使用。(也可理解为文件夹目录)
  
  ```java
  package cc.framework.common.util;
  ```
  
  
  
- 循环与条件控制

  for(初始化; 布尔表达式; 更新) {    //代码语句 }

  ```java
  public class Test {
     public static void main(String args[]) {
   
        for(int i = 0; i < 20; i++) {
           System.out.print("value of i : " + String.valueOf(i));
           System.out.print("\n");
           break;//跳出整个语句块
           continue;//终止到当前,立刻跳转到下一次循环的迭代
           int b = 2;
        }
           int a = 1;
     }
  }
  ```

  if(布尔表达式){   //如果布尔表达式的值为true }else{   //如果布尔表达式的值为false }

  ```java
  public class Test {
   
     public static void main(String args[]){
        int x = 30;
   
        if( x < 20 ){
           System.out.print("这是 if 语句");
        }else{
           System.out.print("这是 else 语句");
        }
     }
  }
  ```

  - 占位符

  | 转 换 符 | 说  明                                      | 示  例       |
  | -------- | ------------------------------------------- | ------------ |
  | %s       | 字符串类型                                  | "mingrisoft" |
  | %c       | 字符类型                                    | 'm'          |
  | %b       | 布尔类型                                    | true         |
  | %d       | 整数类型（十进制）                          | 99           |
  | %x       | 整数类型（十六进制）                        | FF           |
  | %o       | 整数类型（八进制）                          | 77           |
  | %f       | 浮点类型                                    | 99.99        |
  | %a       | 十六进制浮点类型                            | FF.35AE      |
  | %e       | 指数类型                                    | 9.38e+5      |
  | %g       | 通用浮点类型（f和e类型中较短的）            |              |
  | %h       | 散列码                                      |              |
  | %%       | 百分比类型                                  | ％           |
  | %n       | 换行符                                      |              |
  | %tx      | 日期与时间类型（x代表不同的日期与时间转换符 |              |

### Part.3 Java语言基础2

- 面向对象特性

  #####封装

  封装，就是把客观事物封装成抽象的类，并且类可以把自己的数据和方法只让可信的类或者对象操作，对不可信的进行信息隐藏。一个类就是一个封装了数据以及操作这些数据的代码的逻辑实体。在一个对象内部，某些代码或某些数据可以是私有的，不能被外界访问。通过这种方式，对象对内部数据提供了不同级别的保护，以防止程序中无关的部分意外的改变或错误的使用了对象的私有部分。

  #####继承

  继承，指可以让某个类型的对象获得另一个类型的对象的属性的方法。它支持按级分类的概念。继承是指这样一种能力：它可以使用现有类的所有功能，并在无需重新编写原来的类的情况下对这些功能进行扩展。 通过继承创建的新类称为“子类”或“派生类”，被继承的类称为“基类”、“父类”或“超类”。继承的过程，就是从一般到特殊的过程。要实现继承，可以通过 “继承”（Inheritance）和“组合”（Composition）来实现。继承概念的实现方式有二类：实现继承与接口继承。实现继承是指直接使用 基类的属性和方法而无需额外编码的能力；接口继承是指仅使用属性和方法的名称、但是子类必须提供实现的能力。

  #####多态

  多态，是指一个类实例的相同方法在不同情形有不同表现形式。多态机制使具有不同内部结构的对象可以共享相同的外部接口。这意味着，虽然针对不同对象的具体操作不同，但通过一个公共的类，它们（那些操作）可以通过相同的方式予以调用。

- 异常处理

  在Java中，凡是可能抛出异常的语句，都可以用`try ... catch`捕获。把可能发生异常的语句放在`try { ... }`中，然后使用`catch`捕获对应的`Exception`及其子类。

- 接口

  接口可以理解为一种特殊的类，里面全部是由***\*全局常量\****和**公共的抽象方法**所组成。接口是解决***\*Java无法使用多继承\****的一种手段，但是接口在实际中更多的作用是***\*制定标准\****的。

- 集合

  集合是在Java中最常见的数据结构，现实世界都是有由单个个体组合而成的，又因Java中一切皆对象，要把这些对象组合起来管理和使用，集合类就出现了。

  集合关系图

   

  ![img](https://img2018.cnblogs.com/blog/1175569/201908/1175569-20190813185822827-390071136.png)

   

  发现一个特点，上述所有的集合类，除了map系列的集合，即左边的集合都实现了Iterator接口。

  　　Iterator是一个用来遍历集合中元素的接口，主要有hashNext()，next()，remove()三种方法。

  　　它的子接口ListIterator在它的基础上又添加了三种方法，分别是add()，previous()，hasPrevious()。

  从图中我们可以看到：

  　　1.集合主要分为Collection和Map两个接口。

  　　2.Collection又分别被List和Set继承。

  　　3.List被AbstractList实现，然后分为3个子类，ArrayList，LinkList和VectorList。

  　　4.Set被AbstractSet实现，又分为2个子类，HashSet和TreeSet。

  　　5.Map被AbstractMap实现，又分为2个子类，HashMap和TreeMap。

  　　6.Map被Hashtable实现。

### Part.4 HTML基础 元素



### Part.5 HTML基础 Cookie 及本地存储



### Part.6 WebElement Api 元素定位

> 在做自动化功能时，最常用的就是定位元素，赋值，取值，比较，逻辑运算，所以第一步必须先认识并找到我们的元素才可以后续操作。必须熟练掌握Part4和Part5

- 通过id定位：

  ```java
  <input id="kw" class="wd" name="tj_trnews"></input>
  ```

  ```java
  driver.findElement(By.id("kw"))
  ```

- 通过name定位：

  ```java
  <input id="kw" class="cls" name="wd"></input>
  ```

  ```java
  driver.findElement(By.name("wd"))
  ```

- 通过class name定位：

  ```java
  <input id="kw" class="cls" name="wd"></input>
  ```

  ```java
  driver.findElement(By.className("s_ipt"))
  ```

- 通过tag name定位：

  ```java
  <input id="kw" class="cls" name="wd"></input>
  ```

  ```java
  driver.findElement(By.tagName("input"))
  ```

- 通过xpath定位，xpath定位有N种写法，这里列几个常用写法：xpath路径使用chrome工具获取，最简单也最好用

  ```java
  driver.findElement(By.xpath("//*[@id='kw']"))
  driver.findElement(By.xpath("//*[@name='wd']"))
  driver.findElement(By.xpath("//input[@class='s_ipt']"))
  driver.findElement(By.xpath("/html/body/form/span/input"))
  driver.findElement(By.xpath("//span[@class='soutu-btn']/input"))
  driver.findElement(By.xpath("//form[@id='form']/span/input"))
  driver.findElement(By.xpath("//input[@id='kw' and @name='wd']"))
  ```

- 通过css定位，css定位有N种写法，这里列几个常用写法：(一般用于批量定位)

  ```java
  driver.findElement(By.cssSelector("#kw")
  driver.findElement(By.cssSelector("[name=wd]")
  driver.findElement(By.cssSelector(".s_ipt")
  driver.findElement(By.cssSelector("html > body > form > span > input")
  driver.findElement(By.cssSelector("span.soutu-btn> input#kw")
  driver.findElement(By.cssSelector("form#form > span > input")
  ```

- 通过link text定位：

  页面上有一组文本链接。

  ```java
  <a class="mnav" href="http://news.baidu.com" name="tj_trnews">新闻</a>
  <a class="mnav" href="http://www.hao123.com" name="tj_trhao123">hao123</a>
  ```

  ```java
  driver.findElement(By.linkText("新闻")
  driver.findElement(By.linkText("hao123")
  ```

- 通过partialLink text定位：parial link定位是对link定位的一个补充，有些文本链接会比较长，这个时候我们可以取文本链接的一部分定位，只要这一部分信息可以唯一地标识这个链接。

  ```java
  driver.findElement(By.partialLinkText("新")
  driver.findElement(By.partialLinkText("hao")
  driver.findElement(By.partialLinkText("123")
  ```



###Part.7 控制浏览器及 WebElement常用操作

- 控制浏览器

```java
//设置浏览器最大化
driver.manage().window().maximize();
//设置浏览器窗口宽高
driver.manage().window().setSize(new Dimension(600, 800));
//让浏览器后退操作
driver.navigate().back();
//让浏览器前进操作
driver.navigate().forward();
//让浏览器刷新操作
driver.navigate().refresh();

```



- 常用操作API

```java
//获取一个元素
WebElement input = driver.findElement(By.id("h"));
//模拟键盘向输入框里输入内容
input.sendKeys("hello");
//清除文本输入框中的内容
input.clear();
//单机input元素，作用于button的话就是提交操作
input.click();
//提交表单
input.submit();
//返回元素的尺寸
input.getSize();
//获取元素的文本
input.getText();
//获得元素的属性值
intput.getAttribute("class");
//设置该元素是否用户可见
input.isDisplayed();

```



###Part.7 模拟鼠标与键盘操作



### Part.9 JavaScriptExecutor

> 某些页面中需要执行网页原生JS脚本或模拟操作不起租用时候可以植入脚本使用JavaScriptExecutor执行



### Part.10 截图操作



###Part.11 大作业淘宝自动下单





### Part.11 接口自动化

> 在前后端分离项目中，接口自动化核心就是模拟前端发送请求



### Part.12 接口自动化

