scrollObj = yScroller.init({
	container : "container",
	position : "relative",
	//��ǰҳ���뿪��Ļ���¼�
	onPageLeave : function(y) {
		var pageNum = Math.abs(y / document.body.clientHeight);
		/*do sth*/
	},
	//ҳ�������Ļ���¼�
	onPageEnter : function(y) {
		var pageNum = Math.abs(y /document.body.clientHeight);
		/*do sth*/
	}
});
//��ť��ε�ҳ�����
xxx.click = function(m) {
	//scrollTo(λ�ã�����ʱ��)
	scrollObj.scrollTo(n * document.body.clientHeight, 0.3);
}

demo:http://res.imtt.qq.com/actnew/worldcup2014/shoot/index.html