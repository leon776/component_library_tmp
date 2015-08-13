
##兼容IE8插件的轻量级插件：

* html5.js ([source](http://html5shim.googlecode.com/svn/trunk/html5.js)) – HTML5 支持

* respond.js ([source](https://github.com/scottjehl/Respond)) – 媒体查询支持(min-width/max-width)


##瀑布流实现：
* 思路1：

    响应式瀑布流，使用masonry.js ([source](http://www.jq22.com/jquery-info362))完成`定位布局`，通过媒体查询控制主体宽度，并适配浏览器窗口变化&缩放。
    
    [Demo](http://bbetter.me/demo/waterfall/index.html)

* 思路2：
 
    定宽瀑布流，使用`流体布局`，根据初始屏幕宽度计算可容纳列数。
 
     [Demo](http://bbetter.me/demo/waterfall/index.html)

##整体架构：

* 图片按前景图\背景图\雪碧图……建立img\images\global……目录；
* sass源文件按功能拆分，编译输出为压缩优化后的css；
* html公用结构拆分为jade模块调用，此项目较简只做头部模块抽取。

##模块化和组件化：

1. 按功能&嵌套需求进行划分&组合，并加入注释和说明，提高`维护效率`；
2. css进行细化和基础化定义，利用sass文件架构完成大量`模块的拆分&构建`；
3. 基础类不依赖父元素定义属性，便于`复用和移植`，配合多扩展类完成整体布局和个性化定义；
4. 采用sass的@extend，%Placeholders和Mixins组合高使用频率的css属性，保证代码的`一致性和可读性`。

##重构细节：

1. 使用jade书写html结构提高代码`组织性和可读性`；
2. 字色、字号、交互操作、间距、布局等视觉展现使用sass全局变量定义，`展现一致UI`，且方便批量修改；
3. 利用sass的参数&函数完成：

	* 布局中的宽高、间距值计算；
	* 获取图片占位元素的宽高值和background-position定位；
	* 结合媒体查询完成多分辨率下的瀑布流适配。


##代码质量和效率提升细节：

1. 详细页利用table-cell实现等高布局；
2. 使用伪元素实现图片替换、字符占位，减少冗余代码。


