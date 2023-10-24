<a name="Requirement"></a>
## Requirement

<a name="f562b435"></a>
##### **Functional requirements**

• Describe _what_ the system should do

```latex
inputs，outputs，data stored，computations，timing and synchronization
```

<a name="35bdf658"></a>
##### **Quality requirements**

• C_onstraints_ on the design to meet specified levels of quality

```latex
Response time，Throughput，Resource usage，Reliability，Availability，Recovery from failure，Allowances for maintainability and enhancement，Allowances for reusability
```

<a name="a924d6e0"></a>
##### **Platform requirements**

•C_onstraints_ on the environment and technology of the system

<a name="22988946"></a>
##### **Process requirements**

•C_onstraints_ on the project plan and development methods

职能要求-说明该系统应该做什么

质量要求 -对设计的限制，以达到规定的质量水平。

平台要求 -对系统环境和技术的限制；

流程要求 -对项目计划和开发方法的限制因素；

Define the system under discussion - verb with identifier - defines a positive end result - quality criteria

```
The [Online Banking System] [shall/will/must-may/should] allow the Internet user to [access her current account balance] [in less than 5 seconds].
```

<a name="4de8388d"></a>
## Use Case

<a name="55496762"></a>
##### **A use case should**

—Describe the user’s interaction with the system

**—Not the computations the system performs.**

—Be as _independent_ as possible from any particular user interface design.

—Only include actions in which the actor interacts with the computer.

**—Not actions a user does manually**

<a name="Procedure"></a>
##### Procedure

**A. Name**: Short and descriptive.

**B. Actors**: Types of users that will do this

**C. Goals**: What are the actors trying to achieve.

**D. Preconditions**: State of the system before the use case.

**E. Summary**: Short informal description.

**F. Related use cases.**

**G. Steps**: Describe each step using a 2-column format.

**H. Postconditions**: State of the system after completion.

<a name="6acc26ab"></a>
##### Use Case in text

1. **Use case**: **Open file**

**Related use cases:**

Generalization of:

• Open file by typing name

• Open file by browsing

**Steps**:

| **Actor  actions** | **System  responses** |
| --- | --- |
| 1. Choose ‘Open…’ command | 2. File open dialog  appears |
| 3. Specify filename | <br /> |
| 4. Confirm selection | 5. Dialog disappears |


2. **Use case**: **Open file by typing name**

**Related use cases:**

Specialization of: Open file

**Steps**:

| **Actor  actions** | **System  responses** |
| --- | --- |
| 1. Choose ‘Open…’ command | 2. File open dialog  appears |
| 3a. Select text field | <br /> |
| 3b. Type file name | <br /> |
| 4. Click ‘Open’ | 5. Dialog disappears |


![](https://i.loli.net/2021/03/05/hAdOkRmNYqBM9Hi.png#id=RCHRE&originHeight=844&originWidth=1149&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

Extension: optional

Inclusion: commonality

![](https://i.loli.net/2021/03/05/RwC3HjzDX56hPOF.png#id=JeK7I&originHeight=1411&originWidth=1882&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="b9a30e64"></a>
## Sequence Diagrams: Fragments

**Allow** **multiple sequences to be represented in compact form (may involve all participants or just a subset).**

•alt, for alternatives with conditions       •opt, for optional behavior

•loop(lower bound, upper bound), for loops       •par, for con-current behavior

![](https://i.loli.net/2021/03/05/GYrqgvyXjPowEHb.png#id=bLXWf&originHeight=1618&originWidth=2153&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="2b4dc72a"></a>
## Activity Diagrams: Representing concurrency

•Concurrency is shown using forks, joins and rendezvous.

—A _fork_ has one incoming transition and multiple outgoing transitions.

-The execution splits into two concurrent threads.

—A _rendezvous_ has multiple incoming and multiple outgoing transitions.

-Once all the incoming transitions occur all the outgoing transitions may occur.

—A join has multiple incoming transitions and one outgoing transition.<br />The outgoing transition will be taken when all incoming transitions have occurred.<br />The incoming transitions must be triggered in separate threads.<br />If one incoming transition occurs, a wait condition occurs at the join until the other transitions occur.

并发用分叉、加入和会合来显示。

一个fork分叉有一个进入的过渡和多个离开的过渡。执行分裂成两个并发线程。

一个rendezvous会合有多个传入转折和多个传出转折。一旦所有的传入转义发生，所有的传出转义都可能发生。并发用分叉、接合和会合来显示。

一个join有多个传入转换和一个传出转换。<br />当所有传入的转折发生后，将进行传出转折。<br />入站转换必须在不同的线程中触发。<br />如果一个传入转场发生，在连接处会发生一个等待条件，直到其他转场发生。

<a name="da2302a0"></a>
### 泳道 Swimlanes

Activity diagrams are most often associated with several classes.<br />The partition of activities among the existing classes can be explicitly shown using swimlanes.活动图最常见的是与几个类相关联。<br />活动在现有类之间的分割可以用泳道明确地显示出来。

![](https://i.loli.net/2021/03/05/Opu8Mxde9yPFb42.png#id=D4KzS&originHeight=1607&originWidth=2148&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="40801c24"></a>
## State Machine

<a name="State"></a>
### State

•At any given point in time, the system is in one state.

•It will remain in this state until an event occurs that causes it to change state.

•A state is represented by a rounded rectangle containing the name of the state.

•Special states:

—A black circle represents the _start state_

—A circle with a ring around it represents an _end state_

<a name="Transitions"></a>
### Transitions

•A transition represents a change of state in response to an event.

—It is considered to occur instantaneously.

•The label on each transition is the event that causes the change of state.

<a name="Activities"></a>
### Activities

•An _activity_ is something that takes place while the system is _in_ a state.

—It takes a period of time.

—The system may take a transition out of the state in response to completion of the activity,

—Some other outgoing transition may result in:

-The interruption of the activity, and

-An early exit from the state.

![](https://i.loli.net/2021/03/05/6cMYPOFy9BX4kS3.png#id=D1p9U&originHeight=1038&originWidth=1558&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/05/A9QzUaH4GL2WfvP.png#id=dpYtC&originHeight=1116&originWidth=1200&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="0bb074dd"></a>
## Class Diagram

<a name="7beb8ad4"></a>
##### •An association should exist if a class

-_possesses_/controls/_is connected to_/is related to_/is a part of_/has as parts/is a member of_/_has as members*

<a name="9385cecf"></a>
##### •There are two ways to identify generalizations:

—bottom-up-Group together similar classes creating a new superclass

—top-down-Look for more general classes first, specialize them if needed

<a name="39dff6c7"></a>
##### •Create an _interface_, instead of a superclass if

—The classes are very dissimilar except for having a few operations in common

—One or more of the classes already have their own superclasses

—Different implementations of the same class might be available

![](https://i.loli.net/2021/03/05/4fdB8JMWpiaNcgb.png#id=thqeF&originHeight=875&originWidth=1139&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/05/4fdB8JMWpiaNcgb.png#id=n0Rsz&originHeight=875&originWidth=1139&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/05/emRogDNyu5zdSOb.png#id=qFjX6&originHeight=854&originWidth=1162&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="Patterns"></a>
##### Patterns

![](https://i.loli.net/2021/03/05/NoDydUlpvjzbSCW.png#id=v7M94&originHeight=1384&originWidth=1857&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/AxhTP3o695nbRVS.png#id=VILF4&originHeight=825&originWidth=1399&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/q4jacHTfvF9Px2W.png#id=uN1sS&originHeight=1394&originWidth=1857&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/mIhsOEjLWCPrzlG.png#id=yyhUB&originHeight=1012&originWidth=1074&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/Z5OX89mEWeBkowa.png#id=Sl3tL&originHeight=1388&originWidth=1849&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/ctX5ruCW87ynbd1.png#id=KyUbU&originHeight=994&originWidth=1374&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/oyKki65VDp4Twuz.png#id=CD5Au&originHeight=1392&originWidth=1849&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/dYAR6gz2lnVeXHo.png#id=uSyXy&originHeight=1386&originWidth=1868&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/AqeOvg315atsFCi.png#id=NP6u5&originHeight=1391&originWidth=1854&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/BAQ8E1ozmnNT4cY.png#id=tdZxx&originHeight=1408&originWidth=1859&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/8NDJHTzh96CWtBI.png#id=llpPr&originHeight=1388&originWidth=1851&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/tuSjQWIZaMV1DXr.png#id=RbXOV&originHeight=1007&originWidth=1364&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/XrTZf5cGNeFHPlA.png#id=cmbcH&originHeight=741&originWidth=1365&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/h2LgaMyPzKpA8fS.png#id=mA5CI&originHeight=1621&originWidth=2142&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

![](https://i.loli.net/2021/03/06/T6d2nk1RWujvzQg.png#id=mzi18&originHeight=1395&originWidth=1856&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

<a name="c1b8eee1"></a>
## Software Design

<a name="25a3dea4"></a>
### Divide and conquer

**Trying to deal with something big all at once is normally much harder than dealing with a series of smaller things**

<a name="1e1a70f1"></a>
### Increasing Cohesion 增加内聚

A subsystem or module has high cohesion if it keeps together things that are related to each other, and keeps out other things<br />This makes the system as a whole easier to understand and change<br />Type of cohesion:<br />Functional, Layer, Communicational, Sequential, Procedural, Temporal, Utility

如果一个子系统或模块把彼此相关的东西放在一起，而把其他东西挡在外面，那么这个子系统或模块就有很高的凝聚力。<br />这使得整个系统更容易理解和改变。<br />凝聚力的类型。<br />职能性、层级性、交流性、顺序性、程序性、时间性、实用性。

<a name="d50990bb"></a>
##### Function Cohesion 功能凝聚力

This is achieved when all the code that computes a particular result is kept together - and everything else is kept out<br />i.e. when a module only performs a single computation, and returns a result, without having side-effects.<br />Benefits to the system:<br />Easier to understand<br />More reusable<br />Easier to replace<br />Modules that update a database, create a new file or interact with the user are not functionally cohesive

当所有计算某个特定结果的代码都被保存在一起时，就可以实现这一点--而其他所有的代码都被排除在外。<br />即当一个模块只进行一次计算，并返回一个结果，而不产生副作用。<br />对系统的好处。<br />更容易理解<br />更多的可重复使用<br />更容易更换<br />更新数据库、创建新文件或与用户交互的模块在功能上不一致。

<a name="b58aef8a"></a>
##### 层内聚力Layer cohesion

All the facilities for providing or accessing a set of related services are kept together, and everything else is kept out<br />The layers should form a hierarchy<br />Higher layers can access services of lower layers,<br />Lower layers do not access higher layers<br />The set of procedures through which a layer provides its services is the application programming interface (API)<br />You can replace a layer without having any impact on the other layers<br />You just replicate the API

所有提供或获取一套相关服务的设施都放在一起，其他一切都不在其中。<br />各层应形成一个层次结构<br />上层可以访问下层的服务。<br />低层不能访问高层。<br />层提供服务的一组程序就是应用程序接口（API）。<br />你可以在不影响其他图层的情况下替换一个图层。<br />您只需复制API   。

<a name="3193bc39"></a>
##### 沟通的凝聚力Communicational Cohesion

All the modules that access or manipulate certain data are kept together (e.g. in the same class) - and everything else is kept out<br />A class would have good communicational cohesion<br />if all the system’s facilities for storing and manipulating its data are contained in this class.<br />if the class does not do anything other than manage its data.<br />Main advantage:  When you need to make changes to the data, you  find all the code in one place

所有访问或操作特定数据的模块都被保存在一起（例如在同一个类中）--而其他所有模块都被排除在外。<br />一个班级会有良好的沟通凝聚力。<br />如果系统存储和操作其数据的所有设施都包含在这个类中。<br />如果该类除了管理其数据外，不做任何其他事情。<br />主要优点。 当你需要对数据进行修改时， 你可以在一个地方找到所有的代码。

<a name="15f8efc7"></a>
##### 顺序内聚Sequential cohesion

Procedures, in which one procedure provides input to the next, are kept together – and everything else is kept out<br />You should achieve sequential cohesion, only once you have already achieved the preceding types of cohesion.

在程序中，一个程序为下一个程序提供输入，并保持在一起--而其他一切都被排除在外。<br />你应该实现顺序凝聚，只有当你已经实现了前面的凝聚类型时，你才应该实现顺序凝聚。

**顺序内聚指一个模块中各个处理元素都密切相关于同一功能且必须顺序执行,前一功能元素的输出就是下一功能元素的输入。**

`**In the context of software design, sequential cohesion refers to the grouping of procedures that are called one after another where the output of a procedure: • Corresponds to the input to the next procedure in the sequence.**`

```java
a = x();
b = y(a);
c = z(b);
```

<a name="bdf444b8"></a>
##### 程序上的凝聚力Procedural cohesion

Procedures that are used one after another are kept together<br />Even if one does not necessarily provide input to the next.<br />Weaker than sequential cohesion

接连使用的程序被保存在一起。<br />即使一个不一定为下一个提供投入。<br />弱于顺序的凝聚力。

<a name="f6347373"></a>
##### 时序内聚Temporal Cohesion

Operations that are performed during the same phase of the execution of the program are kept together, and everything else is kept out<br />For example, placing together the code used during system start-up or initialization.<br />Weaker than procedural cohesion.

在程序执行的同一阶段所进行的操作会被保留在一起，其他的操作都被保留在外面。<br />例如，将系统启动或初始化时使用的代码放在一起。<br />弱于程序凝聚力。

<a name="17a8209b"></a>
##### 实用性内聚Utility cohesion

Related utilities are kept together when there is no way to group them using a stronger form of cohesion<br />A utility is a procedure or class that has wide applicability to many different subsystems and is designed to be reusable.<br />For example, the java.lang.Math class.

当没有办法使用更强的凝聚力形式将其分组时，相关的实用程序就会保持在一起。<br />实用程序是一个过程或类，它对许多不同的子系统具有广泛的适用性，并且被设计为可重用。<br />例如，java.lang.Math类。

`**如果你仅仅因为一组方法具有相似的实现就把它们放在一个对象里，那么你将犯“创建逻辑内聚对象（logically cohesive object）”的错误。**`

<a name="ea826b25"></a>
### Reduce Coupling 减少耦合

`**tight coupling vs loosely coupling**`

Coupling occurs when there are interdependencies between one module and another<br />When interdependencies exist, changes in one place will require changes somewhere else.<br />A network of interdependencies makes it hard to see at a glance how some component works.<br />Type of coupling:<br />Content, Common, Control, Stamp, Data, Routine Call, Type use, Inclusion/Import, External

当一个模块和另一个模块之间存在相互依赖关系时，就会发生耦合。<br />当存在相互依赖关系时，一个地方的变化将需要其他地方的变化。<br />一个相互依赖的网络，让人很难一眼看出某个组件的工作原理。<br />耦合的类型。<br />内容、通用、控制、印记、数据、例程调用、类型使用、包含/导入、外部。

<a name="8f1bf3f8"></a>
#### 内容耦合Content Coupling

Occurs when one component surreptitiously modifies data that is internal to another component<br />To reduce content coupling you should therefore encapsulate all instance variables, and declare them private and provide get and set methods

当一个模块直接修改或操作另一个模块的数据,或者直接转入另一个模块时，就发生了内容耦合。此时，被修改的模块完全依赖于修改它的模块。

因此，为了减少内容耦合，你应该封装所有的实例变量，并声明它们是私有的，并提供get和set方法。

```java
public class Line
{
 private Point start, end;
 ...
 public Point getStart() { return start; }
 public Point getEnd() { return end; }
}
public class Arch
{
 private Line baseline;
 ...
 void slant(int newY)
 {
  Point theEnd = baseline.getEnd();
  theEnd.setLocation(theEnd.getX(),newY);
 }
}
```

<a name="33a90f73"></a>
##### 公共耦合Common Coupling

Occurs whenever you use a global variable<br />All the components using the global variable become coupled to each other<br />A weaker form of common coupling is when a variable can be accessed by a subset of the system’s classes<br />e.g. a Java package<br />Can be acceptable for creating global variables that represent system-wide default values<br />The Singleton pattern provides encapsulated global access to an object

两个以上的模块共同引用一个全局数据项就称为公共耦合。大量的公共耦合结构中，会让你很难确定是哪个模块给全局变量赋了一个特定的值.<br />一种较弱的共同耦合形式是当一个变量可以被系统中的一个类的子集访问时<br />如：一个Java包<br />可以接受创建代表全系统默认值的全局变量。<br />Singleton模式提供了对对象的封装全局访问。

<a name="e80cc57b"></a>
##### 外部耦合External coupling

When a module has a dependency on such things as the operating system, shared libraries or the hardware<br />It is best to reduce the number of places in the code where such dependencies exist.<br />The Façade design pattern can reduce external coupling

当一个模块对操作系统、共享库或硬件等有依赖性的时候<br />最好是减少代码中存在这种依赖关系的地方。<br />Façade设计模式可以减少外部耦合性

**一组模块都访问同一全局简单变量，而且不通过参数表传递该全局变量的信息，则称之为外部耦合 从定义和图中也可以看出，公共耦合和外部耦合的区别就在于前者是全局数据结构，后者是全局简单变量**

<a name="e7e38f98"></a>
##### **控制耦合Control Coupling**

Occurs when one procedure calls another using a ‘flag’ or ‘command’ that explicitly controls what the second procedure does<br />To make a change you have to change both the calling and called method<br />The use of polymorphic operations is normally the best way to avoid control coupling<br />One way to reduce the control coupling could be to have a look-up table<br />commands are then mapped to a method that should be called when that command is issued<br />当一个存储过程使用 "标志 "或 "命令 "调用另一个存储过程时发生，这些标志或命令明确控制了第二个存储过程的操作。<br />要做一个改变，你必须同时改变调用和被调用的方法。<br />使用多态操作通常是避免控制耦合的最佳方式。<br />减少控制耦合的一个方法是可以有一个查找表。<br />然后，命令被映射到一个方法，当该命令被发出时，该方法应该被调用。

```java
public routineX(String command)
{
   if (command.equals("drawCircle")
   {
      drawCircle();
   }
   else
   {
      drawRectangle();
   }
}
```

<a name="a5b0f296"></a>
##### 印记耦合Stamp Coupling

Occurs whenever one of your application classes is declared as the type of a method argument<br />Since one class now uses the other, changing the system becomes harder<br />Reusing one class requires reusing the other

Two ways to reduce stamp coupling,<br />using an interface as the argument type<br />passing simple variables

每当你的应用程序类被声明为方法参数的类型时发生。<br />由于现在一个类使用另一个类，所以改变系统变得更难了<br />重用一个类需要重用另一个类

减少印章耦合的两种方法。<br />使用接口作为参数类型<br />传递简单变量

**如果一组模块通过参数表传递记录信息，就是标记耦合。事实上，这组模块共享了这个记录，它是某一数据结构的子结构，而不是简单变量。这要求这些模块都必须清楚该记录的结构，并按结构要求对此记录进行操作。**

```java
public class Emailer
{
  public void sendEmail(Employee e, String text)
  {...}
  ...
}
```

```java
public displayName(Person p)
{
 ui.display(p.getName());
}
```

**Using simple data types to avoid it:**

```java
public class Emailer
{
  public void sendEmail(String name, String email, String text) 
  {...}
  ...
}
```

**Using an interface to avoid it:**

```java
public interface Addressee
{
  public abstract String getName();
  public abstract String getEmail();
}
 
public class Employee implements Addressee {…}
 
public class Emailer
{
  public void sendEmail(Addressee e, String text)
  {...}
  ...
}
```

<a name="79bd5395"></a>
##### 数据耦合Data coupling

**Occurs whenever the types of method arguments are either primitive or else simple library classes** (e.g. String)

•The more arguments a method has, the higher the coupling

—All methods that use the method must pass all the arguments

•You should reduce coupling by not giving methods unnecessary arguments

•There is a trade-off between data coupling and stamp coupling

—Increasing one often decreases the other

-一个方法的参数越多，耦合度越高。

-所有使用该方法的方法必须传递所有的参数。

-你应该通过不给方法提供不必要的参数来减少耦合性。

-数据耦合和印章耦合之间有一个权衡。

-增加一个往往会减少另一个。

**模块之间通过参数来传递数据，那么被称为数据耦合。数据耦合是最低的一种耦合形 式，系统中一般都存在这种类型的耦合，因为为了完成一些有意义的功能，往往需要将某些模块的输出数据作为另 一些模块的输入数据**

<a name="2ee0dc91"></a>
##### Routine call coupling

Occurs when one routine (or method in an object oriented system) calls another<br />The routines are coupled because they depend on each other’s behaviour<br />Routine call coupling is always present in any system.

If you repetitively use a sequence of two or more methods to compute something<br />then you can reduce routine call coupling by writing a single routine that encapsulates the sequence.

常规呼叫耦合

当一个例程（或一个面向对象系统中的方法）调用另一个例程时发生<br />例程是耦合的，因为它们相互依赖对方的行为。<br />常规调用耦合总是存在于任何系统中。

如果你重复地使用两个或多个方法的序列来计算某件事情<br />那么你可以通过编写一个封装序列的单例程来减少例程调用的耦合。

<a name="eec8e1c6"></a>
##### Type use coupling

Occurs when a module uses a data type defined in another module<br />It occurs any time a class declares an instance variable or a local variable as having another class for its type.<br />The consequence of type use coupling is that if the type definition changes, then the users of the type may have to change<br />Always declare the type of a variable to be the most general possible class or interface that contains the required operations

类型使用联轴器<br />当一个模块使用另一个模块中定义的数据类型时发生。<br />它发生在任何时候，当一个类声明一个实例变量或局部变量的类型有另一个类的时候。<br />类型使用耦合的后果是，如果类型定义发生变化，那么该类型的用户可能必须改变<br />始终将变量的类型声明为包含所需操作的最通用的类或接口。

<a name="e23cdd3e"></a>
##### Inclusion or import coupling

Occurs when one component imports a package<br />(as in Java)<br />or when one component includes another<br />(as in C++).<br />The including or importing component is now exposed to everything in the included or imported component.<br />If the included/imported component changes something or adds something.<br />This may raise a conflict with something in the includer, forcing the includer to change.<br />An item in an imported component might have the same name as something you have already defined.

<a name="ad84f8ec"></a>
### Increase Abstraction增加抽象性

Ensure that your designs allow you to hide or defer consideration of details, thus reducing complexity

•A good abstraction is said to provide _information hiding_

•Abstractions allow you to understand the essence of a subsystem without having to know unnecessary details

确保你的设计允许你隐藏或推迟考虑细节，从而降低复杂性

-一个好的抽象被说成是提供_信息隐藏_。

-抽象化使你能够理解一个子系统的本质，而不必知道不必要的细节。

•Examples of abstractions:

—Classes

—UML associations

—Interfaces

—State machines

<a name="c823b611"></a>
### Increase reusability 增加重复利用性

Design the various aspects of your system so that they can be used again in other contexts

•Generalize your design as much as possible

•Follow the preceding design principles

•Design your system to contain hooks

•Simplify your design as much as possible

设计你的系统的各个方面，使它们可以在其他情况下再次使用。

-尽可能地使你的设计通用化

-遵循上述设计原则

-设计你的系统以包含钩子

-尽可能地简化你的设计。

<a name="148303bf"></a>
### Reuse where possible

Design with reuse is complementary to design for reusability<br />Actively reusing designs or code allows you to take advantage of the investment you or others have made in reusable components<br />Cloning should not be seen as a form of reuse

再利用设计与可再利用设计相辅相成。<br />积极重用设计或代码，可以让你利用你或其他人在可重用组件上的投资。<br />克隆不应被视为一种再利用的形式。

<a name="64a7e98e"></a>
### Design for flexibility

Actively anticipate changes that a design may have to undergo in the future, and prepare for them<br />Reduce coupling and increase cohesion<br />Create abstractions<br />Do not hard-code anything<br />Leave all options open<br />Do not restrict the options of people who have to modify the system later<br />Use reusable code and make code reusable

积极预测设计在未来可能要经历的变化，并为之做好准备。<br />减少耦合，增加内聚力<br />创建抽象<br />不要硬编码<br />让所有的选项保持开放<br />不要限制以后要修改系统的人的选择。<br />使用可重用的代码，使代码可重用。

<a name="5053dc4d"></a>
### Anticipate obsolescence 预测过时

Plan for changes in the technology or environment so the software will continue to run or can be easily changed<br />Avoid using early releases of technology<br />Avoid using software libraries that are specific to particular environments<br />Avoid using undocumented features or little-used features of software libraries<br />Avoid using software or special hardware from companies that are less likely to provide long-term support<br />Use standard languages and technologies that are supported by multiple vendors

为技术或环境的变化制定计划，使软件能够继续运行或易于改变。<br />避免使用早期发布的技术<br />避免使用特定环境下的软件库。<br />避免使用软件库中未记录的功能或很少使用的功能。<br />避免使用不太可能提供长期支持的公司的软件或特殊硬件。<br />使用多个供应商支持的标准语言和技术。

<a name="9032e542"></a>
### Design for Portability 便携性设计

Have the software run on as many platforms as possible<br />Avoid the use of facilities that are specific to one particular environment<br />E.g. a library only available in Microsoft Windows

让软件在尽可能多的平台上运行。<br />避免使用某一特定环境下特有的设施。<br />例如，只有在微软Windows中才能使用的库。

<a name="29cbbdd1"></a>
### Design for Testability 可测试性设计

Take steps to make testing easier<br />Design a program to automatically test the software<br />Ensure that all the functionality of the code can be driven by an external program, bypassing a graphical user interface<br />In Java, you can create a main() method in each class in order to exercise the other methods<br />Use Junit or similar frameworks

采取步骤使测试更容易<br />设计一个自动测试软件的程序<br />确保代码的所有功能都能由外部程序驱动，绕过图形用户界面。<br />在Java中，你可以在每个类中创建一个main()方法，以便行使其他方法。<br />使用Junit或类似框架

<a name="34e7b871"></a>
### Design defensively防御性设计

Never trust how others will try to use a component you are designing<br />Handle all cases where other code might attempt to use your component inappropriately<br />Check that all of the inputs to your component are valid: the preconditions<br />Unfortunately, over-zealous defensive design can result in unnecessarily repetitive checking

永远不要相信别人会如何使用你正在设计的组件。<br />处理所有其他代码可能试图不适当地使用您的组件的情况。<br />检查你的组件的所有输入是否有效：先决条件<br />遗憾的是，过于热衷的防守设计会导致不必要的重复检查

<a name="f24a08f3"></a>
### Design by contract按合同设计

A technique that allows you to design defensively in an efficient and systematic way<br />Key idea<br />each method has an explicit contract with its callers<br />The contract has a set of assertions that state:<br />What preconditions the called method requires to be true when it starts executing<br />What postconditions the called method agrees to ensure are true when it finishes executing<br />What invariants the called method agrees will not change as it executes<br />一种可以让您高效、系统地进行防御性设计的技术。<br />关键思想<br />每一个方法都与调用者有明确的契约。<br />合同有一组断言，说明。<br />当被调用的方法开始执行时，它需要什么前提条件为真？<br />当被调用的方法完成执行时，被调用的方法同意确保哪些后置条件为真。<br />被调用的方法所同意的不变量不会因为执行

<a name="c824f99c"></a>
## 设计步骤

Using priorities and objectives to decide among alternatives<br />Step 1: List and describe the alternatives for the design decision.<br />Step 2: List the advantages and disadvantages of each alternative with respect to your objectives and priorities.<br />Step 3: Determine whether any of the alternatives prevents you from meeting one or more of the objectives.<br />Step 4: Choose the alternative that helps you to best meet your objectives.<br />Step 5: Adjust priorities for subsequent decision making.

利用优先事项和目标在各种替代品中作出决定<br />第一步：列出并描述设计决策的备选方案。<br />第二步：根据你的目标和优先级，列出每个备选方案的优缺点。<br />第三步：确定是否有任何替代方案会妨碍您实现一个或多个目标。<br />第四步：选择能帮助您最好地实现目标的备选方案。<br />第5步：调整优先级，以便随后做出决策。

<a name="Exercise"></a>
## Exercise

**Which one of the following practices should be avoided in object-oriented programing?**<br />Creation of instance variables<br />`Creation of classes with plural names`<br />Declaration of attributes starting with lowercase letters<br />Declaration of variables with digits in their names<br />Creation of large arrays that might overwhelm the memory

**Imagine there is a class X in a framework, where X is designed to be subclassed (have subclasses created by a developer using the framework). There is a concrete method m in class X that does nothing (the body of the method is empty) but is called by some other method in class X. What would we call method m?**<br />A useless method<br />An accessor method<br />A slot method<br />A service method<br />`A hook method`

**Which one of the following options describe the behavior of a typical client-server system?**<br />`The server starts running before the clients, and clients initiate connections to the server`

**Consider a client-server system, where an administrator interacts with the user interface of the server, and two users interact with the user interface of connected client processes (i.e. there are two connected clients). At least how many threads must be running in this system?**   `8`

**Which of the following statements is true regarding the Java programming language?**<br />You can create at most two objects from the same class<br />String is a primitive type<br />`A class can extend only one class (using the “extend” keyword)`<br />A class can implement only one interface<br />You cannot extend abstract classes`（You have to extend it）`

**Which of the following statement is true about Abstract classes?**<br />You cannot declare a static variable in an abstract class<br />You cannot define concrete methods in an abstract class<br />Abstract classes can only extend other abstract classes<br />`You cannot create an instance of an abstract class`

**Which one of the following object-oriented mechanisms can be used to create a slot in a framework?**<br />`Create an abstract method that must be implemented by the application that uses the framework`

**Review the UML class diagram below. Given that each airplane type in the airline's fleet has a specific passenger capacity. What is the BEST strategy to adjust the model below to specify an airplane’s capacity?**

`Add an AirplaneType class with a capacity attribute and an association from SpecificFlight to AirplaneType`

**In UML, a rectangle that has inside of it a colon (:) followed by a name represents**: `An instance`

**Which one of the following statements is true regarding the UML Class diagram shown below?**（实心菱形）<br />`If the Vehicle instance is deleted, then all Wheel instances must be deleted`

**Which one of the following statements is true regarding class responsibilities?**<br />• A responsibility must correspond to a single operation in a class<br />• A responsibility must be implemented using public methods only<br />`• A responsibility may be realized by multiple operations in a class`<br />• A responsibility must be implemented using private methods only

**An OCL statement can be used to:**<br />• Update the value of an attribute<br />• Specify an algorithm<br />`• Limit the range of values of an attribute`<br />• Specify an association<br />• Specify a generalizationMatch each requirement to the type of requirement<br />_2_Quality requirement<br />_4_Process requirement<br />_1_Platform requirement<br />_2_Functional requirement

**• The libraries that will be used to implement the systemIn UML, use case extensions are used to:**<br />`• Add optional interactions`<br />• Express commonality between several different use cases<br />• Update the functionality of a previously defined use case<br />• Extend the functionality of a use case in a new version of the system

**You are designing a class hierarchy in Java. You discovered that class A in library L fits as a sub-class under one of the classes in your hierarchy. You would like to integrate class A into your hierarchy. However, class A is already part of its own hierarchy in library L. What is the best strategy to integrate class A into your class hierarchy?**<br />• Use the delegation pattern<br />`• Use the adapter pattern`<br />• Change the code of A so that it extends multiple classes<br />• Use the immutable pattern<br />• Integrate your class hierarchy into library L

Which one of the following statements is incorrect regarding UML state machines?<br />• A UML state machine can describe the behavior of a system, sub-system, or object<br />• Some but not all events cause the state machine to change its state<br />`• A transition is considered to occur instantaneously unless it is associated with an action`<br />• An activity cannot be associated with a transition as activities only execute inside of states

In the context of usability, efficiency of use refers to:<br />`• The speed with which an expert user can do their work`<br />• The speed with which a new user can become proficient with the system.<br />• The extent to which users like the system<br />• The extent to which it prevents the user from making errors, detects errors, and helps to correct errors
