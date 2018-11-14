<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
{dede:include filename="meta_index.htm"/}
<!-----
<meta http-equiv="Content-Type" content="text/html; charset={dede:global.cfg_soft_lang/}" />
<title>{dede:global.cfg_webname/}</title>
<meta name="description" content="{dede:global.cfg_description/}" />
<meta name="keywords" content="{dede:global.cfg_keywords/}" />
<meta name="author" content="{dede:global.xinlv_author/}" />
<meta name="copyright" content="{dede:global.xinlv_shortname/}" />
<meta name="MSSmartTagsPreventParsing" content="True" />
<meta name="robots" content="all" />
<meta name="applicable-device"content="pc" />

<meta http-equiv=”Cache-Control” content=”no-transform” />   百度转码
<meta http-equiv=”Cache-Control” content=”no-siteapp” />     百度转码

<base href="{dede:global.xinlv_url/}/" />
<link rel="shortcut icon" href="{dede:global.xinlv_url/}/favicon.ico" type="image/x-icon" />
-----meta:end--->
<!---css:start--->
<link href="{dede:global.xinlv_url/}/xinlv/style3/xinlv_index.css" rel="stylesheet" media="screen" type="text/css" />
<!---js:start--->
<script language="javascript" type="text/javascript" src="{dede:global.xinlv_url/}/xinlv/style3/xinlv_index.js"></script>
<!---统计等调用--->
{dede:include filename="m_index.htm"/}
{dede:include filename="tj_head.htm"/}
</head>

{dede:include filename="header.htm"/}

<!---导航调用--->
{dede:channel type='top' row='10' currentstyle="<li class='nav_on'><a href='~typelink~' ~rel~><span>~typename~</span></a></li>"}
<li><a href='[field:typeurl/]' [field:rel/]><span>[field:typename/]</span></a></li>
{/dede:channel}
<!---一二级导航调用--->
{dede:channelartlist }
<a href="{dede:global.xinlv_url/}{dede:field name='typeurl'/}">{dede:field name='typename'/}</a>
<hr>
{dede:channel type='son' noself='yes'}
<a href="[field:global.xinlv_url/][field:typelink/]">[field:typename/]</a><br />
{/dede:channel}
{/dede:channelartlist}

<!---主栏目下子栏目调用--->
{dede:channel type='son' currentstyle="<a href='~typelink~' class='thisclass'>~typename~</a>"}
<a href='[field:global.xinlv_url/][field:typeurl/]'>[field:typename/]</a>
{/dede:channel}


<!---递增代码--->
[field:global name=autoindex/]
添加后序号就会自动增加，默认从1开始。
但是有时候我们可能不需要从1开始，比如从2开始，那么就需要这样写：
[field:global name=autoindex runphp="yes"]@me=@me+1;[/field:global]
相反，如果想让它从0开始,那就用这个代码:
[field:global name=autoindex runphp="yes"]@me=@me-1;[/field:global]
<!---栏目调用--->
{dede:type typeid='1'}<a href="[field:global.xinlv_url/][field:typelink/]" target="_blank" title="[field:typename/]"></a>{/dede:type}
链接：{dede:type typeid='1'}[field:global.xinlv_url/][field:typelink/]{/dede:type}
<!---文章调用--->
{dede:arclist row='5' titlelen='36' typeid='16' flag='h' noflag='h' limit='0,1' idlist='1' infolen='180'(内容简介长度为个字符) orderby='pubdate' (按时间排列) } 
 isweight='Y' orderby='weight' orderway='desc'(按权重排列)
<!---相关调用--->
{dede:likearticle row='8' titlelen='36' }  [field:global.xinlv_url/][field:arcurl/]  [field:title/]  {/dede:likearticle}
<!---Body调用--->
{dede:arclist row='10' typeid='11' addfields='body' channelid='1'}
[field:body/]
[field:body function='cn_substr(html2text(@me),1600)'/]...
{/dede:arclist}

<!---频道列表各文章调用：--->
{dede:channelartlist}
	<h2><a href="{dede:field.typeurl/}">{dede:field.typename/}</a></h2>
	{dede:arclist row='10' titlelen='50' channelid='' addfields='' flag='' isweight='' orderby='' orderway='' limit=''}
		<p><a href="[field:arcurl/]">[field:title/]</a></p>
	{/dede:arclist}
{/dede:channelartlist}


{dede:arclist row='5' titlelen='50' typeid='16'}
{dede:arclist  flag='h' row='' col='' infolen='' imgwidth='' imgheight='' listtype='' orderby='' keyword='' limit='0,1'}
标题：[field:title/] [field:shorttitle/]
图片：[field:global.xinlv_url/][field:picname/]
链接：[field:global.xinlv_url/][field:arcurl/]
简介：[field:info/]… [field:description function="cn_substr(@me,200)"/]… 栏目：[field:typename/] [field:typelink/] 
时间：[field:pubdate function="MyDate('Y-m-d',@me)"/]  
关键词：
<a href="javascript:void(0)">这个不会跳动</a> 
{/dede:arclist}

新字段调用：
{dede:arclist addfields='language,softtype'  channelid='3'} 
[field:textlink /] - [field:softtype /] - [field:language /]<br /> 
{/dede:arclist}

<!---幻灯Banner--->
{dede:myppt typeid='1' row='3'}
<li><a href="[field:global.xinlv_url/][field:url/]" target="_blank"><img alt="[field:title function='html2text(@me)'/]" width="978" height="375" src="[field:pic/]" /></a></li>
{/dede:myppt}

article:
{dede:myppt typeid='12' row='1'}<img alt="[field:title function='html2text(@me)'/]" src="[field:pic/]" />{/dede:myppt}

typeid 调用的幻灯分组id
row 调用的行数
url 链接地址
pic 图片地址
title 标题介绍
<!---热门关键词--->
{dede:tag row='10' getall='1' sort='month'}<a href='[field:link/]'>[field:tag /]</a>{/dede:tag}

{dede:global.xinlv_url/}/xinlv/digital23/images3/

公司简介1：{dede:sql sql='Select content,substring(content,1,300) as content from xinlv_arctype where id=1'}[field:content function='html2text(@me)'/]{/dede:sql}
公司简介2：{dede:sql sql='Select content from xinlv_arctype where id=1'}
[field:content/]
{/dede:sql}
{dede:include filename="footer.htm"/}
{dede:include filename="tj_body.htm"/}
