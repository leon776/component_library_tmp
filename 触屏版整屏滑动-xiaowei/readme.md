scrollObj = yScroller.init({
	container : "container",
	position : "relative",
	//当前页面离开屏幕的事件
	onPageLeave : function(y) {
		var pageNum = Math.abs(y / document.body.clientHeight);
		/*do sth*/
	},
	//页面进入屏幕的事件
	onPageEnter : function(y) {
		var pageNum = Math.abs(y /document.body.clientHeight);
		/*do sth*/
	}
});
//按钮如何当页面滚动
xxx.click = function(m) {
	//scrollTo(位置，经过时间)
	scrollObj.scrollTo(n * document.body.clientHeight, 0.3);
}

demo:http://res.imtt.qq.com/actnew/worldcup2014/shoot/index.html