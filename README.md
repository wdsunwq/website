# website
网站用文档
文章命名规则：/article/{aid}.html		detail
			  /products/{aid}.html
			  /news/{aid}.html
			  /case/{aid}.html
列表命名规则：/list_{tid}_{page}.html   /demo/contact_{tid}.html	/demo/list_{tid}_{page}.html  /demo/machine3.html

关于我们	about.html
创始人说,发展历程,荣誉资质,企业相册,团队展示,企业文化,企业愿景,优势
founder.html	history.html  /honor.html /show.html  team.html culture.html vision.html /strengths.html
企业简介
创始人说,企业文化,发展历程,创新与研发,企业架构,优势

企业博客	/blog_{tid}_{page}.html
企业日记,行业动态,产品百科,技术咨询,标准文件,资料下载,常见问题
/diary_{page}.html /news_{page}.html /baike_{page}.html  /faq_{page}.html /article_{page}.html /article_{tid}_{page}.html	standard_{page}.html
产品中心	/products_{page}.html	/products_{tid}_{page}.html
业务领域/产业布局	industry.html
应用案列	/case_{tid}_{page}.html 

在线展示 online_visit.html	factory_show.html
荣誉资质,产品认证,企业相册,工厂展示,团队展示,国际合作,客户见证,合作企业,企业电视台
/honor.html	renzheng	 /show.html		team.html
客户见证	/witness.html
合作企业	/customer.html
人力资源	hr_resources
为什么选择JOOV,人才理念,工作在JOOV,人才发展,人才招聘
why_choose	hr_concept.html		lifestyle	hr_development.html		job.html
联系我们	contact.html	人才招聘:hr.html	企业电视台:/video.html
banner:  {dede:global.xinlv_url/}/uploads/bn/bn_730.260_1.jpg
		{dede:global.xinlv_url/}/uploads/shop.jpg
			  /list_{tid}_{page}.html
			  /list_{tid}{page}.html
joov命名：	  /demo/business.html
			  /demo/travel.html
			  /demo/photography.html
			  /demo/entertainment.html
			  /demo/others_{tid}.html
meta标签说明		  
http://www.cssue.com/xhtml-css/html5-css3/mobile-meta.html
font-family: "Microsoft YaHei","Arial","黑体","宋体",sans-serif;
数据表前缀：xinlv_
{dede:global.xinlv_url/}/xinlv/xinlv150630/style3/
{dede:global.xinlv_url/}/xinlv/xinlv150630/images3/
/templets/kf3/
/templets/style3/
/templets/images3/
../images3/
../images3/css/
/templets/kf3/
../kf3/
singlepage/

{dede:include filename="header.htm"/}

{dede:include filename="machine18/footer.htm"/}

导航栏单个调用：{dede:type typeid='1'} [field:global.xinlv_url/][field:typelink/]    [field:typelink/]  list.php?tid=[field:id/] [field:typename/]  {/dede:type}
view.php?aid=[field:id/]
单个栏目名称：{dede:type typeid='1'}[field:typename/]{/dede:type}

站点根网址：{dede:global.cfg_basehost/}
1.调用根网址：{dede:global.xinlv_url/} [field:global.xinlv_url/]
2.移动网址：{dede:global.m_url/}	[field:global.m_url/]
3.BBS：		{dede:global.xinlv_bbs/}
4.域名：	{dede:global.xinlv_domain/}
备案号：  {dede:global.cfg_beian/}
5.版权：    {dede:global.xinlv_powerby/}
6.24h电话：{dede:global.xinlv_tel/}		[field:global.xinlv_tel/]
7..手机： {dede:global.xinlv_mp/}
8.座机：    {dede:global.xinlv_zuoji/}
8.传真：    {dede:global.xinlv_fax/}
9.QQ： 	  {dede:global.xinlv_qq/}	[field:global.xinlv_qq/]
微信：{dede:global.xinlv_wechat/}
Skype：xinlv_skype  	 
11.邮箱： 	  {dede:global.xinlv_email/} [field:global.xinlv_email/]
<a href="mailto:{dede:global.xinlv_email/}">	
12.地址： 	  {dede:global.xinlv_address/}
13.联系人：  {dede:global.xinlv_attn/}
邮编
14.作者：	{dede:global.xinlv_author/}
15.公司名：{dede:global.xinlv_company/}		[field:global.xinlv_company/]
16.公司简称：{dede:global.xinlv_shortname/}	[field:global.xinlv_shortname/]
Banner	home products case blog news faq honor show hr about contact 

http://wpa.qq.com/msgrd?v=3&uin=[field:global.xinlv_qq/]&site=qq&menu=yes
广告语1：{dede:global.xinlv_adyi/}
广告语2：{dede:global.xinlv_ader/}
广告语3：{dede:global.xinlv_adsan/}
主关键词：{dede:global.xinlv_keywords/}		[field:global.xinlv_keywords/]
热门关键词：{dede:hotwords num='6'/}
8.统计：  {dede:global.tongji_head/}
9.统计：  {dede:global.tongji_body/}
字体：font-family:"Microsoft YaHe" font-family:"\5FAE\8F6F\96C5\9ED1"   微软雅黑
		宋体	\5b8b\4f53	黑体 \9ed1\4f53
百度站长后台token：{dede:global.baidutoken/}
网站域名：{dede:global.baiduhost/}
<a href="[^"]*"    <a href="#"
facebook：  {dede:global.facebook/}
twitter：  {dede:global.twitter/}
linkedin：  {dede:global.linkedin/}
youtube：	{dede:global.youtube/}


http://wpa.qq.com/msgrd?v=3&uin=2739433677&site=qq&menu=yes
友情链接：{dede:flink linktype='2' row='24'}<li>[field:link /]</li>{/dede:flink} 
a71f1a  链接红色  6a6a6a

手机网站：
插件模块：module_hot

font-weight:normal

禁止右键 复制 选择：
<script type="text/javascript">
    window.onerror = function () { return true; }
    document.oncontextmenu = new Function("event.returnValue=false;");
    document.onselectstart = new Function("event.returnValue=false;");
    document.oncontextmenu = function (e) { return false; } 
</script>

