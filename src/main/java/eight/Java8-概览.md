# Java语言

- 此版本中引入了Lambda Expressions（一种新的语言功能）。 它们使您可以将功能视为方法参数，或将代码视为数据。 Lambda表达式使您可以更紧凑地表示单方法接口（称为功能接口）的实例。

- 方法引用为已经具有名称的方法提供了易于阅读的lambda表达式。

- 默认方法允许将新功能添加到库的接口，并确保与为这些接口的较早版本编写的代码二进制兼容。

- 重复注释提供了将同一注释类型多次应用于同一声明或类型使用的能力。

- 类型注释提供了将注释应用到任何使用类型的地方的能力，而不仅仅是在声明上。 与可插拔类型系统一起使用时，此功能可改进代码的类型检查。

- 改进的类型推断。

- 方法参数反射。

# 集合

- 新的java.util.stream包中的类提供了Stream API，以支持对元素流进行功能样式的操作。 Stream API已集成到Collections API中，该API允许对集合进行批量操作，例如顺序或并行map-reduce转换。

- 具有键冲突的HashMap的性能改进

# 安全

- 默认情况下启用客户端TLS 1.2

- AccessController.doPrivileged的新变体，使代码可以声明其特权的子集，而不会阻止整个堆栈的遍历以检查其他权限

- 更强大的基于密码的加密算法

- JSSE服务器中的SSL / TLS服务器名称指示（SNI）扩展支持

- 支持AEAD算法：增强了SunJCE提供程序，以支持AES / GCM / NoPadding密码实现以及GCM算法参数。 并且增强了SunJSSE提供程序以支持基于AEAD模式的密码套件。 请参阅Oracle Providers文档，JEP 115。

- KeyStore增强功能，包括新的Domain KeyStore类型java.security.DomainLoadStoreParameter和keytool实用程序的新命令选项-importpassword

- SHA-224消息摘要

- 对NSA Suite B密码术的增强支持

- 更好地支持高熵随机数生成

- 新的java.security.cert.PKIXRevocationChecker类，用于配置X.509证书的吊销检查

- Windows的64位PKCS11

- Kerberos 5重播缓存中的新rcache类型

- 支持Kerberos 5协议转换和约束委派

- 默认情况下禁用Kerberos 5弱加密类型

- GSS-API / Kerberos 5机制的未绑定SASL

- 多个主机名的SASL服务

- JNI桥接到Mac OS X上的本机JGSS

- 在SunJSSE提供程序中支持强度更高的临时DH密钥

- 在JSSE中支持服务器端密码套件首选项定制

# JavaFX

- 新的Modena主题已在此版本中实现。 有关更多信息，请参见fxexperience.com上的博客。

- 新的SwingNode类使开发人员能够将Swing内容嵌入到JavaFX应用程序中。 请参阅SwingNode javadoc和在JavaFX应用程序中嵌入Swing内容。

- 新的UI控件包括DatePicker和TreeTableView控件。

- javafx.print包提供JavaFX Printing API的公共类。 有关更多信息，请参见javadoc。

- 现在，“ 3D图形”功能包括3D形状，相机，灯光，子场景，材质，拾取和抗锯齿。 新的Shape3D（Box，Cylinder，MeshView和Sphere子类），SubScene，Material，PickResult，LightBase（AmbientLight和PointLight子类）和SceneAntialiasing API类已添加到JavaFX 3D图形库中。 此版本中还更新了Camera API类。 有关javafx.scene.shape.Shape3D，javafx.scene.SubScene，javafx.scene.paint.Material，javafx.scene.input.PickResult，javafx.scene.SceneAntialiasing和JavaFX 3D图形入门的信息，请参见相应的类javadoc。 文献。

- WebView类提供了新功能和改进。 有关其他HTML5功能（包括Web套接字，Web Worker和Web字体）的更多信息，请查看HTML5的受支持功能。

- 增强的文本支持，包括双向文本和复杂的文本脚本，例如控件中的Thai和Hindi，以及文本节点中的多行，多样式文本。

- 此版本中已添加了对Hi-DPI显示的支持。

- CSS Styleable *类成为公共API。 有关更多信息，请参见javafx.css javadoc。

- 新的ScheduledService类允许自动重启服务。

- JavaFX现在可用于ARM平台。 JDK for ARM包括JavaFX的基础，图形和控件组件。

# 工具

- 提供了jjs命令来调用Nashorn引擎。

- java命令启动JavaFX应用程序。

- Java手册页已被重新编写。

- 提供了jdeps命令行工具来分析类文件。

- Java管理扩展（JMX）提供了对诊断命令的远程访问。

- jarsigner工具具有一个选项，可以从时间戳管理局（TSA）请求签名的时间戳。

### Javac tool

- javac命令的-parameters选项可用于存储形式参数名称，并使Reflection API能够检索形式参数名称。

- Javac规范（JLS）15.21节中的相等运算符的类型规则现在已由javac命令正确执行。

- javac工具现在支持检查javadoc注释的内容，以查找运行javadoc时生成的文件中可能导致各种问题的问题，例如无效的HTML或可访问性问题。 新的-Xdoclint选项启用了该功能。 有关更多详细信息，请参见运行“ javac -X”的输出。 此功能在javadoc工具中也可用，并且默认情况下在此功能中启用。

- 现在，javac工具提供了根据需要生成本机头的功能。 这样就无需在构建管道中单独运行javah工具。 通过使用新的-h选项在javac中启用此功能，该选项用于指定应在其中写入头文件的目录。 头文件将为任何具有本机方法或以java.lang.annotation.Native类型的新注释注释的常量字段的类生成。

### Javadoc tool

- javadoc工具支持新的DocTree API，使您能够将Javadoc注释作为抽象语法树进行遍历。

- javadoc工具支持新的Javadoc Access API，该API使您可以直接从Java应用程序调用Javadoc工具，而无需执行新过程。 有关更多信息，请参见javadoc新功能页面。

- Javadoc工具现在支持检查javadoc注释的内容中是否存在运行javadoc时生成的文件中可能导致各种问题的问题，例如无效的HTML或可访问性问题。 该功能默认情况下处于启用状态，也可以通过新的-Xdoclint选项进行控制。 有关更多详细信息，请参见运行“ javadoc -X”的输出。 该功能在javac工具中也可用，尽管默认情况下未启用该功能。

# 国际化

- Unicode增强功能，包括对Unicode 6.2.0的支持

- 采用Unicode CLDR数据和java.locale.providers系统属性

- 新的日历和语言环境API

- 能够安装自定义资源包作为扩展

# 部署

对于沙箱applet和Java Web Start应用程序，现在使用URLPermission允许连接回它们启动时所在的服务器。SocketPermission不再被授予。在所有安全级别上，主JAR文件的JAR文件清单中都需要Permissions属性。

# Date-Time 包

一套新的软件包，提供了全面的日期时间模型。

# 脚本

Rhino javascript引擎已被Nashorn Javascript引擎替换。

# Pack200

- Pack200对常量池条目和JSR 292引入的新字节码的支持

- JDK8支持由JSR-292，JSR-308和JSR-335指定的类文件更改

# IO 和 NIO

- 基于Solaris事件端口机制的Solaris新SelectorProvider实现。 若要使用，请将系统属性java.nio.channels.spi.Selector设置为值sun.nio.ch.EventPortSelectorProvider。

- 减小<JDK_HOME> /jre/lib/charsets.jar文件的大小

- java.lang.String（byte []，*）构造函数和java.lang.String.getBytes（）方法的性能改进。

# java.lang 和 java.util 包

- 并行数组排序

- 标准编码和解码Base64

- 无符号算术支持

# JDBC

- JDBC-ODBC桥已被删除。

- JDBC 4.2引入了新功能。

# Java DB

JDK 8包含Java DB 10.10。

# 网络

- 添加了类java.net.URLPermission。

- 在类java.net.HttpURLConnection中，如果安装了安全管理器，则调用该请求打开连接需要权限。

# 并发

- 类和接口已添加到java.util.concurrent包中。

- 已将方法添加到java.util.concurrent.ConcurrentHashMap类中，以支持基于新添加的流功能和lambda表达式的聚合操作。

- 已将类添加到java.util.concurrent.atomic包中，以支持可伸缩的可更新变量。

- 已将方法添加到java.util.concurrent.ForkJoinPool类中以支持公共池。

- 添加了java.util.concurrent.locks.StampedLock类，以提供具有三种模式的基于功能的锁，用于控制读/写访问。

# HotSpot

- 添加了硬件内在函数以使用高级加密标准（AES）。 UseAES和UseAESIntrinsics标志可用于为Intel硬件启用基于硬件的AES内在函数。 硬件必须是2010或更新的Westmere硬件。

注意：仅服务器虚拟机支持AES内在函数。

例如，要启用硬件AES，请使用以下标志：

-XX：+ UseAES -XX：+ UseAESIntrinsics

要禁用硬件AES，请使用以下标志：

-XX：-UseAES -XX：-UseAESIntrinsics

- 删除PermGen。

- 用于方法调用的字节码指令支持Java编程语言中的默认方法。

# 参考

[What's New in JDK 8](https://www.oracle.com/technetwork/java/javase/8-whats-new-2157071.html)