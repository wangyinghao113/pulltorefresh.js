# pulltorefresh.js
模拟手机原生下拉刷新效果

一个小巧但功能强大的Javascript库，旨在为您的webapp的拉动刷新功能。不需要标记，高度可定制和无依赖关系！

###原文http://www.boxfactura.com/pulltorefresh.js/

###演示http://www.boxfactura.com/pulltorefresh.js/demos/basic.html


将JS文件包含在您的webapp中并进行初始化：

```
 PullToRefresh() {
        frames['PullToRefresh'].init({
            mainElement: '.bbs-container',
            onRefresh: function () { this.getData(); },//数据初始化
            instructionsPullToRefresh: '下拉刷新', //Pull down to refresh
            instructionsReleaseToRefresh: '松开刷新',
            instructionsRefreshing: '正在加载',
        });
    }
```



API

➡ distThreshold（整数，缺省60）

触发刷新所需的最小距离。

➡ distMax（整数，缺省80）

元素可能的最大距离。

➡ distReload（整数，缺省50）

后distThreshold达到和释放，元素都会有这样的高度。

➡ mainElement（字符串，默认：body）

在哪个元素之前，刷新元素将是？

➡ triggerElement（字符串，默认：body）

哪个元素应该触发拉刷？

➡ ptrElement（字符串，默认：.ptr）

主要元素有什么类？

➡ classPrefix（字符串，默认：ptr--）

什么类前缀的元素？

➡ cssProp（字符串，默认：min-height）

什么属性将用于计算元素的比例？

➡ iconArrow（字符串，默认：&#8675;）

两个图标instructionsPullToRefresh和instructionsReleaseToRefresh

➡ iconRefreshing（字符串，默认：&hellip;）

刷新过程中的图标。

➡ instructionsPullToRefresh（字符串，默认：Pull down to refresh）

初始指令字符串。

➡ instructionsReleaseToRefresh（字符串，默认：Release to refresh）

distThreshold到达时的指示字符串。

➡ instructionsRefreshing（字符串，默认：Refreshing）

清爽的文字。

➡ refreshTimeout（整数，缺省500）

延迟，以毫秒为单位onRefresh触发。

➡ onInit（功能）

初始化函数。

➡ onRefresh（功能）

什么拉拉刷新触发器？你可以回报承诺。默认为window.location.reload()

➡ resistanceFunction（功能）

阻力函数，接受一个参数，必须返回一个数字，上限为1.默认值为 t => Math.min(1, t / 2.5)

➡ passive（布尔值）

如果支持被动处理程序，该值将被传递{ passive: true|false }给touchmove侦听器。默认为false
