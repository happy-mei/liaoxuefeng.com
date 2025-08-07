<!-- TRANSLATED by md-translate -->
# Java程序基本结构

# Java program basic structure

我们先剖析一个完整的Java程序，它的基本结构是什么：

We start by dissecting a complete Java program and what its basic structure is:

```java
/**
 * 可以用来自动创建文档的注释
 */
public class Hello {
    public static void main(String[] args) {
        // 向屏幕输出文本:
        System.out.println("Hello, world!");
        /* 多行注释开始
        注释内容
        注释结束 */
    }
} // class定义结束
```

因为Java是面向对象的语言，一个程序的基本单位就是`class`，`class`是关键字，这里定义的`class`名字就是`Hello`：

Because Java is an object-oriented language, the basic unit of a program is a `class`, and `class` is the keyword; the name of the `class` defined here is `Hello`:

```java
public class Hello { // 类名是Hello
    // ...
} // class定义结束
```

类名要求：

Class name requirements:

* 类名必须以英文字母开头，后接字母，数字和下划线的组合
* 习惯以大写字母开头

* Class names must begin with a letter followed by a combination of letters, numbers and underscores
* Customarily begin with a capital letter

要注意遵守命名习惯，好的类命名：

Be careful to follow naming conventions and good class naming:

* Hello
* NoteBook
* VRPlayer

* Hello
* NoteBook
* VRPlayer

不好的类命名：

Bad class naming:

* hello
* Good123
* Note_Book
* _World

* hello
* Good123
* Note_Book
* _World

注意到`public`是访问修饰符，表示该`class`是公开的。

Notice that `public` is an access modifier indicating that the `class` is public.

不写`public`，也能正确编译，但是这个类将无法从命令行执行。

Without `public`, it will compile correctly, but the class will not be executable from the command line.

在`class`内部，可以定义若干方法（method）：

Within `class`, several methods can be defined:

```java
public class Hello {
    public static void main(String[] args) { // 方法名是main
        // 方法代码...
    } // 方法定义结束
}
```

方法定义了一组执行语句，方法内部的代码将会被依次顺序执行。

A method defines a set of execution statements, and the code inside the method will be executed in sequential order.

这里的方法名是`main`，返回值是`void`，表示没有任何返回值。

Here the method name is `main` and the return value is `void`, indicating that there is no return value.

我们注意到`public`除了可以修饰`class`外，也可以修饰方法。而关键字`static`是另一个修饰符，它表示静态方法，后面我们会讲解方法的类型，目前，我们只需要知道，Java入口程序规定的方法必须是静态方法，方法名必须为`main`，括号内的参数必须是String数组。

We notice that `public` can modify methods in addition to `class`. And the keyword `static` is another modifier which denotes a static method, and we will explain the types of methods later, for now, all we need to know is that the methods specified by the Java entry program must be static methods, the method name must be `main`, and the arguments in parentheses must be String arrays.

方法名也有命名规则，命名和`class`一样，但是首字母小写：

There are also naming rules for method names, named like `class`, but with lowercase initial letters:

好的方法命名：

Good way to name it:

* main
* goodMorning
* playVR

* main
* goodMorning
* playVR

不好的方法命名：

Bad way to name it:

* Main
* good123
* good_morning
* _playVR

* Main
* good123
* good_morning
* _playVR

在方法内部，语句才是真正的执行代码。Java的每一行语句必须以分号结束：

Inside the method, the statement is the actual code that is executed.Each line of Java must be terminated with a semicolon:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!"); // 语句
    }
}
```

在Java程序中，注释是一种给人阅读的文本，不是程序的一部分，所以编译器会自动忽略注释。

In a Java program, comments are a kind of text for people to read, not part of the program, so the compiler automatically ignores them.

Java有3种注释，第一种是单行注释，以双斜线开头，直到这一行的结尾结束：

Java has 3 types of comments, the first is a single line comment that starts with a double slash and ends with a double slash until the end of the line:

```java
// 这是注释...
```

而多行注释以`/*`星号开头，以`*/`结束，可以有多行：

Multi-line comments, on the other hand, begin with a `/*` asterisk and end with `*/` and can have multiple lines:

```java
/*
这是注释
blablabla...
这也是注释
*/
```

还有一种特殊的多行注释，以`/**`开头，以`*/`结束，如果有多行，每行通常以星号开头：

There is also a special multi-line comment that starts with `/**` and ends with `*/`, and if there are more than one line, each line usually starts with an asterisk:

```java
/**
 * 可以用来自动创建文档的注释
 * 
 * @auther liaoxuefeng
 */
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

这种特殊的多行注释需要写在类和方法的定义处，可以用于自动创建文档。

This special multi-line comment needs to be written at the definition of classes and methods and can be used to automatically create documentation.

Java程序对格式没有明确的要求，多几个空格或者回车不影响程序的正确性，但是我们要养成良好的编程习惯，注意遵守Java社区约定的编码格式。

Java programs do not have a clear requirement for the format, a few more spaces or carriage returns do not affect the correctness of the program, but we have to develop good programming habits, pay attention to comply with the Java community agreed coding format.

那约定的编码格式有哪些要求呢？其实我们在前面介绍的Eclipse IDE提供了快捷键`Ctrl+Shift+F`（macOS是`⌘+⇧+F`）帮助我们快速格式化代码的功能，Eclipse就是按照约定的编码格式对代码进行格式化的，所以只需要看看格式化后的代码长啥样就行了。具体的代码格式要求可以在Eclipse的设置中`Java`-`Code Style`查看。

What are the requirements of that agreed coding format? In fact, we introduced in the previous Eclipse IDE provides a shortcut `Ctrl + Shift + F ` (macOS is `⌘ + ⇧ + F `) to help us quickly format the code, Eclipse is in accordance with the agreed coding format of the code formatting , so just need to look at the formatted code after the code looks like on the line. Specific code formatting requirements can be in the Eclipse settings ` Java ` - ` Code Style ` view.