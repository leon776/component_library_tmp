css�ļ���ַ��http://3gimg.qq.com/mig-web/common/pc_component/full_banner/css/ibanner_full.css
js�ļ���ַ��
http://3gimg.qq.com/mig-web/common/pc_component/full_banner/js/jquery-1.9.0.min.js
http://3gimg.qq.com/mig-web/common/pc_component/full_banner/js/ibanner_full.js
���ʹ�ã�
1��dom�ṹ
<div class="banner" style="height:555px">
	<!--������� start-->
	<div id="homeBanner" class="iBanner">
		<div class="iBanner-box">
			<!--box �� box-active ������class�����-->
			<div class="box box-active">
				<img src="#" alt="">
			</div>
			<div class="box">
				<a href="#"><img src="#" alt=""></a>
			</div>
		</div>
		<!--���ҷ�ҳ���ܣ�����Ҫ�Ļ�ɾ����dom start-->
		<div class="prev-mask"><div class="previous"></div></div>
		<div class="next-mask"><div class="next"></div></div>
		<!--���ҷ�ҳ���ܣ�����Ҫ�Ļ�ɾ����dom end-->
		<!--�·�С��ť������Ҫ�Ļ�ɾ����dom start-->
		<div id="homeBannerNav" class="iBanner-nav" style="display: none;">
			<ul>
				<!--˵���������li��data-ibanner��Ӧ��������id(Ϊ�˿�����һ��ҳ��ʹ�ö��ibanner)��href #�ź�����Ƕ�ӦҪ��ʾ��ͼƬ�����-->
				<li><a data-ibanner="#homeBanner" href="#0" class="highlight active"></a></li>
				<li><a data-ibanner="#homeBanner" href="#1"></a></li>
			</ul>
		</div>
		<!--�·�С��ť������Ҫ�Ļ�ɾ����dom end-->
	</div>
	<!--�������end-->
</div>
2.��css��������ҳ���õ���ʽ��
3.��ʼ��
<script type="text/javascript">
//homeBannerΪ���div��id
var homeBanner = new iBanner('#homeBanner', {
	indicator:'#homeBannerNav', //�����С��ť������Ҫ�Ļ��Ͳ�д����
	backgroundColor:['#ff0000', '#000000'], //ÿ��ͼ�ı���ɫ
	/*
		# �任�¼�
		# activeItem��Ŀǰ���ڲ��ŵ�ͼƬ����box
		# targetItem����һ��Ҫ���ŵ�
	*/
	animate: function (activeItem, targetItem) {
	  activeItem.hide()
	  targetItem.show().css('opacity', 0.6).stop().animate({opacity: 1}, 500)
	},
	interval: 5000 //�Զ��ֲ�ʱ��
})
</script>