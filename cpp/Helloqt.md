### 0. 读作 cute~

qt常常被用来开发“严肃”的程序，生产力软件或者军工等高安全项目，不过，它读 cute😀，为了维持严肃的形象， 大多数人都读 Q  T。

### 1. qt的核心是C++

qt的核心是C++。尽管qt公司试图使qt并不局限与C++,例如，pyqt 和 qml 中的js，但是都没有获得很大的成功。qt的成功和C++紧密关联，如果不是C++,我们不会选择qt,qt的出现也使作为系统级编程语言的C++可以较为方便的开发应用层的应用程序。qt是C++技术体系中极为重要的一部分，它在编程世界中最大的意义是可以使系统级别的开发和应用级别的开发紧密的结合起来。

### 2. qt 可以做什么？它的前景

qt被众人所知的是开发PC端桌面GUI,在跨平台（linux,mac,windows）和linux平台几乎是统治级别；在windows平台，它是C++，而且领先MFC。时至今日，qt早不局限于做gui,也不局限于pc,甚至也不局限于C++，但qt的优势和大部分应用场景仍然是PC端桌面C++/GUI。现在，PC端软件开发热度降低，但是在生产力软件开发上，例如wps,kde，工业CAD等等，PC开发仍然不可替代。

回顾历史，关于前端，最开始是PC端开发为主流，后来，移动端开发兴起，现在至未来，web前端技术则会占据越来越重要的地位。PC端作为生产力工具运行的必要环境，它的需求不会减少，生产力工具要求效率和GUi,qt会是第一位的选择，在国内，我们更需要生产力软件，qt的需求尤其会增多；qt的另一个优势是嵌入式系统（资源紧张，基于linux或者直接裸mcu)，在为嵌入式系统开发界面上，qt几乎没有竞争对手。

qt也可以开发移动端。据说，有很多工业级别的应用和对保密要求高的应用使用qt,但总的来说，qt开发移动端并不活跃。


### 3. qt的竞争力分析

|平台|可能更合适的选择|推荐程度|评价|
|---|---|---|---|
|嵌入式平台(GUI)|几乎没有|⭐⭐⭐⭐⭐|几乎没有竞争对手|
|Linux|wxWidgets，Electron|⭐⭐⭐⭐⭐|qt吧，没必要选其它的了。Electron可以做到的qt也可以|
|Windows|微软，Electron，duilib|⭐⭐⭐⭐|当需要C++时，qt是远比MFC,duilib要好的选择。桌面端，生产力软件占大多数，如果是生产力软件，还是qt(C++)。另外，微软从 winform -> wpf -> maui 😱换个不停，微软就是想把你绑定在它的平台上，然后收费。如果老板愿意付费，没什么问题，但是老板通常不愿意付费。。。受难的还是程序员|
|macos，ios|原生,flutter，maui，前端技术|⭐⭐|好像只能静态链接qt库，所以只能使用qt的商业版。。。我没试过(穷)|
|android|原生,flutter，前端技术，maui|⭐⭐⭐|使用qt开发安卓还是可以的|

总结：

1. 在PC端和嵌入式推荐qt
2. 移动端android 还是可以的
3. qt好像对收费越来越渴望了，但qt本身是开放的，估计会比微软好些？

现在web前端可以完成绝大部分业务，少部分需要高性能、低资源占用的场景只能使用qt/c++，也可以因此大胆猜测：以后前端只有两种形式，一种是在数量上占据大多数的，相对较为轻便的，以web技术为核心的前端，另一种是较为沉重的，以C++技术为核心的生产力前端；考虑平台，移动端没有高效的生产力，后面可能会越来越多的以web为主，原生开发作为胶水的可能性很大，桌面端是浏览器+生产力软件。qt的前景还是很好的，尤其在桌面端和嵌入式。在移动端，因为厂商肯定不是第一支持，qt只能作为一个小众的选择。

### 4. qt的技术路线

#### 4.1 qwidget 纯C++

#### 4.2 qtquick qml+js+c++,核心仍然是C++

#### 4.3 pyqt

没有用过。我觉得这个的意义仅仅是：Python也可以开发gui了！

### 5. qt的问题

1. 商业化问题。希望收费更多的是让老板承受，而不是程序员。同时，也感觉到因为商业化，qt 在降低对社区版本的支持。
2. 质量与开发。在windows上开发gui,qt仍然比不上C#。qml至今与xaml相比，还有一些差距。使用qml的感觉总是，第一下感觉很好，后来遇到问题，然后不知道怎么办。qml面向未来，但欠缺成熟，可能是因为qt公司没钱，这就带来了第一个问题。

### 5. 我与qt

非常幸运，我的第一门编程语言是C++,如果不是qt,我根本不可能去写C++。qt仅仅需要一点C++就可以了，qt对于c++的重大意义是：它可以让一个c++初学者，特别是以c++为第一门语言的编程初学者能够做出来东西，我想不到除了qt，还有什么可以有类似的作用。

我一直想做后端开发，还有后来学习了web前端技术（对比我之前用qt写界面😢），我对qt的投入越来越少；但qt仍然是我重要的技术栈。同时，我学习其它的知识，不管是对c++有更深的理解，还是web前端技术,或者其它别的什么，我都能反过来更好的使用qt。

与qt做个尽可能完美的离别，使用三个project

1. 使用qt开发一个自动打印工具`快完成了`
2. 开发一个桌面便签`也完成了一部分`
3. Windows installer `也是桌面端的一个总结`
