css文件地址：http://3gimg.qq.com/mig-web/common/pc_component/full_banner/css/ibanner_full.css
js文件地址：
http://3gimg.qq.com/mig-web/common/pc_component/full_banner/js/jquery-1.9.0.min.js
http://3gimg.qq.com/mig-web/common/pc_component/full_banner/js/ibanner_full.js
如何使用：
1：dom结构
<div class="banner" style="height:555px">
	<!--组件部分 start-->
	<div id="homeBanner" class="iBanner">
		<div class="iBanner-box">
			<!--box 和 box-active 这两个class必须给-->
			<div class="box box-active">
				<img src="#" alt="">
			</div>
			<div class="box">
				<a href="#"><img src="#" alt=""></a>
			</div>
		</div>
		<!--左右翻页功能，不需要的话删除此dom start-->
		<div class="prev-mask"><div class="previous"></div></div>
		<div class="next-mask"><div class="next"></div></div>
		<!--左右翻页功能，不需要的话删除此dom end-->
		<!--下方小按钮，不需要的话删除此dom start-->
		<div id="homeBannerNav" class="iBanner-nav" style="display: none;">
			<ul>
				<!--说明：这里的li的data-ibanner对应自身的组件id(为了可以在一个页面使用多个ibanner)，href #号后面的是对应要显示的图片的序号-->
				<li><a data-ibanner="#homeBanner" href="#0" class="highlight active"></a></li>
				<li><a data-ibanner="#homeBanner" href="#1"></a></li>
			</ul>
		</div>
		<!--下方小按钮，不需要的话删除此dom end-->
	</div>
	<!--组件部分end-->
</div>
2.将css拷贝至网页调用的样式表
3.初始化
<script type="text/javascript">
//homeBanner为组件div的id
var homeBanner = new iBanner('#homeBanner', {
	indicator:'#homeBannerNav', //下面的小按钮，不需要的话就不写这行
	backgroundColor:['#ff0000', '#000000'], //每张图的背景色
	/*
		# 变换事件
		# activeItem：目前正在播放的图片容器box
		# targetItem：下一张要播放的
	*/
	animate: function (activeItem, targetItem) {
	  activeItem.hide()
	  targetItem.show().css('opacity', 0.6).stop().animate({opacity: 1}, 500)
	},
	interval: 5000 //自动轮播时间
})
</script>