<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' expr:dir='data:blog.languageDirection' expr:lang='data:blog.locale' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'><b:attr name='xmlns' value=''/><b:attr name='xmlns:b' value=''/><b:attr name='xmlns:expr' value=''/><b:attr name='xmlns:data' value=''/>
  <head>
                    
    
    <!-- Default Meta -->
    <b:include name='DefaultMeta'/>
    <!-- DNS Prefetech -->
    <b:include name='DNSPrefetech'/>
    <!-- Title -->
    <title><b:if cond='data:view.isError'><data:blog.title/></b:if><b:if cond='data:view.isMultipleItems'><b:if cond='data:view.isHomepage'><data:blog.title/><b:else/><data:blog.pageTitle.escaped/></b:if><b:elseif cond='data:view.isSingleItem'/><data:view.title.escaped/></b:if></title>
    <!-- Open Graph -->
    <b:include name='OpenGraph'/>
    <!-- Twitter Card -->
    <b:include name='TwitterCard'/>
    <!-- Feed Links -->
    <b:eval expr='data:blog.feedLinks'/>


   <b:if cond='!data:view.isLayoutMode'>
     
      <!-- Template Skin -->
      <b:skin><![CDATA[ 
/* === cot12a Template ====
-> Homepage: https://cot12a.blogspot.com/
-> Version : 1.0
-> Updated : 10.3.2023 
*//*=================
>Variables
===================
<Group description="ألاعدادات ألاساسية" selector="body">

<Variable name="UltraLazy" description="التأجيل الاقصي للعناصر" type="length" default="1px" min="1px" max="2px" value="2px"/>

<Variable name="newsSchema" description="تحويل القالب الي سكيما نيوز" type="length" default="1px" min="1px" max="2px" value="1px"/>

<Variable name="darckmoodF" description="تفعيل [دارك مود] كوضع اساسي" type="length" default="1px" min="1px" max="2px" value="1px"/>

<Variable name="disapledarck" description="إلغاء تفعيل زر [دارك مود]" type="length" default="1px" min="1px" max="2px" value="1px"/>

<Variable name="darckmodecolor" description="تغيير لون الدارك مود" type="length" default="1px" min="1px" max="2px" value="1px"/>

<Variable name="BlogFonts" description="تغيير خط الكتابه" type="length" default="1px" min="1px" max="9px" value="2px"/>

<Variable name="CoverImg" description="تفعيل اداة تجاوب الصور المصغرة" type="length" default="2px" min="1px" max="2px" value="2px"/>

<Variable name="StopCopying" description="تفعيل اداة منع نسخ النصوص" type="length" default="1px" min="1px" max="2px" value="1px"/>

<Variable name="MopileFasterVirsonFot" description="تغيير شكل اداة [قائمة الوصول السريع]" type="length" default="3px" min="1px" max="5px" value="1px"/>

<Variable name="content.width" description="Content width" type="length" min="992px" max="1300px" default="1100px" value="1300px"/>
<Variable name="sidebar.width" description="Sidebar width" type="length" min="250px" max="480px" default="330px" value="250px"/>
</Group>

<Group description="اعدادات اداة اخر المشاركات" selector="body">
<Variable name="BlogStylePosts" description="تغيير شكل اداة [أخر المشاركات]" type="length" default="1px" min="1px" max="6px" value="3px"/>
<Variable name="disaplelastposts" description="اخفاء اداة [اخر المشاركات]" type="length" default="1px" min="1px" max="2px" value="1px"/>
<Variable name="blogPager" description="تغيير شكل اداة [عرض المزيد (التي تظهر اسفل اخر المشاركات)]" type="length" default="1px" min="1px" max="2px" value="1px"/>
</Group>

<Group description="اعدادات القائمة العلوية" selector="body">
<Variable name="Style2Headr" description="تغيير شكل [القائمة العلوية]" type="length" default="1px" min="1px" max="3px" value="3px"/>
<Variable name="StykiHeadr" description="تثبيت القائمه العلوية" type="length" default="2px" min="1px" max="2px" value="2px"/>
<Variable name="BacgroundHeader" description="خلفية القائمة العلوية" type="color" default="#ffffff" value="#ffffff"/>
<Variable name="LinkColor" description="لون الروابط" type="color" default="#444" value="#1004ff"/>
<Variable name="HLinkfont" description="حجم خط الروابط" type="font" default="400 15px sans-serif"  value="normal bold 20px sans-serif"/>
<Variable name="Bgbuttons" description="خلفية زر البحث والقائمة " type="color" default="#035dcd" value="#0d03cd"/>
<Variable name="Cobuttons" description="لون ايقونة زر البحث والقائمة " type="color" default="#fff" value="#ffffff"/>
</Group>

<Group description="اعدادات القائمة الجانبية" selector="body">
<Variable name="RemoveAdiseHome" description="تفعيل اداة [اخفاء القائمة الجانبية من الرئيسية]" type="length" default="1px" min="1px" max="2px" value="2px"/>
<Variable name="RemoveAdisePost" description="تفعيل اداة [اخفاء القائمة الجانبية من المقال]" type="length" default="1px" min="1px" max="2px" value="2px"/>
<Variable name="RemoveAdisePage" description="تفعيل اداة [اخفاء القائمة الجانبية من الصفحات]" type="length" default="1px" min="1px" max="2px" value="2px"/>
<Variable name="RemoveAdiseMopile" description="تفعيل اداة [اخفاء القائمة الجانبية من الهاتف]" type="length" default="1px" min="1px" max="2px" value="2px"/>
</Group>

<Group description="اعدادات مميزات المقالات" selector="body">
<Variable name="PostRandom" description="تغيير شكل اداة [قد يعجبك ايضا]" type="length" default="1px" min="1px" max="3px" value="1px"/>
<Variable name="retStylePosts" description="تغيير شكل اداة [مقالات قد تهمك]" type="length" default="1px" min="1px" max="4px" value="1px"/>
<Variable name="retposts" description="اخفاء اداة [مقالات قد تهمك]" type="length" default="1px" min="1px" max="2px" value="1px"/>
<Variable name="RemoveAuthor" description="اخفاء اداة كاتب الموضوع" type="length" default="1px" min="1px" max="2px" value="1px"/>
<Variable name="PostSittings" description="تفعيل زر [اعدادات المقالات]" type="length" default="2px" min="1px" max="2px" value="1px"/>
</Group>


<Group description="ألالوان الرئيسية" selector="body">
<Variable name="body.background" description="Background" color="#f7f7f7" type="background" default="$(color) none repeat scroll top right"  value="$(color) none repeat scroll top right"/>
<Variable name="body.background.color" description="لون تبويب المدونة في الهاتف" type="color" default="#035dcd"  value="#0d03cd"/>
<Variable name="keycolor" description="اللون الرئيسي" type="color" default="#035dcd" value="#0d03cd"/>
<Variable name="step.color" description="اللون المساعد" type="color" default="#eee" value="#eeeeee"/>
<Variable name="grad.color" description="لون الخلفية الاساسي" type="color" default="#ffffff" value="#ffffff"/>
<Variable name="link.color" description="لون الروابط" type="color" default="#444" value="#1004ff"/>
<Variable name="text.color" description="لون النصوص" type="color" default="#34495e" value="#0d03cd"/>
<Variable name="startSide" description="start direction" type="automatic" default="right" hideEditor="true" />
<Variable name="endSide" description="end direction" type="automatic" default="left" hideEditor="true" />
</Group>

<Group description="تخصيصات المشاركات والصفحات" selector=".post-body" >
<Variable name="PostsTitleColor" description="لون عنوان ألمشاركات والصفحات" type="color" default="#171921"  value="#1a1721"/>
<Variable name="PostsTitleFont" description="خط عنوان المشاركات والصفحات" type="font" default="400 25px sans-serif"  value="normal 400 40px sans-serif"/>
<Variable name="PostsTextFont" description="حجم وخط المشاركات والصفحات" type="font" default="400 16px sans-serif"   value="400 19px sans-serif"/>
<Variable name="PostsTextColor" description="لون خط المشاركات والصفحات" type="color" default="#222"  value="#222222"/>
<Variable name="PostsLinkColor" description="لون روابط المشاركات والصفحات" type="color" default="#194ca9"  value="#B51200"/>
</Group>

<Group description='نموذج التعليقات (غير قابل للتعديل)' selector="#comments" hideEditor="true">
<Variable name="comments" description="التعليقات" hideEditor="true" type="length" default="1px" min="1px" max="1px" value="1px"/>
<Variable name="body.text.color" description="لون النص" hideEditor="true" type="color" default="#666" value="#666666"/>
<Variable name="posts.icons.color" description="خلفية ايقونة الاعلام" hideEditor="true" type="color" default="#035dcd" value="#035dcd"/>
<Variable name="body.link.color" description="لون الروابط" hideEditor="true" type="color" default="#035dcd" value="#035dcd"/>
<Variable name="posts.title.color" description="لون العنوان" hideEditor="true" type="color" default="#000" value="#000000"/>
<Variable name="labels.background.color" description="خلفيات الازرار" hideEditor="true" type="color" default="#f5f5f5" value="#f5f5f5"/>
<Variable name="BordersCommints" description="لون الفواصل" type="color" default="#eee" hideEditor="true" value="#eeeeee"/>
<Variable name="posts.background.color" description="لون الخلفية" type="color" default="transparent" hideEditor="true" value="transparent"/>
<Variable name="body.text.font" description="text font" type="font" default="600 14px &#39;Segoe UI&#39;" hideEditor="true" value="600 14px &#39;Segoe UI&#39;"/>
<Variable name="tabs.font" description="tabs font" type="font" default="14px &#39;Segoe UI&#39;" hideEditor="true" value="14px &#39;Segoe UI&#39;"/>
<Variable name="posts.text.color" description="Post text color" type="color" default="#777" hideEditor="true" value="#777777"/> 
<Variable name="labels.background.border" description="فواصل الازرار" type="color" default="#eee" hideEditor="true" value="#eeeeee"/>
</Group> 


*//*=================
>Normalize
===================*/
/* HeadLine SidePar Icon */
.clear{clear:both}

/* Css Icon */
.icon-spinner{background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 50 50' x='0px' y='0px'%3E%3Cpath d='M25.251,6.461c-10.318,0-18.683,8.365-18.683,18.683h4.068c0-8.071,6.543-14.615,14.615-14.615V6.461z' style='fill:%23989b9f;stroke:%23989b9f'%3E%3CanimateTransform attributeName='transform' attributeType='xml' dur='0.6s' from='0 25 25' repeatCount='indefinite' to='360 25 25' type='rotate'%3E%3C/animateTransform%3E%3C/path%3E%3C/svg%3E") center no-repeat}
.OpenSitting.inside:after,.search-submit2:after{content:'\2715';line-height:18px;font-size:14px;font-weight:bold;font-family:inherit}

/* Normalize */

:root{--HLinkfont:$(HLinkfont);--OldMin:$(keycolor);--startSide: $startSide;--endSide: $endSide;--maxWidth:$(content.width);--BodyBG:$(body.background);--minColorIc:$(keycolor);--minColor:$(keycolor);--minColorTran:$(keycolor)cf;--secColor:$(step.color);--thrColor:#fff;--whiteColor:$(grad.color);--hoverColor:$(keycolor);--MinBgColor:#fff;--txtColor:$(text.color);--TitColor:#444;--SanColor:#666;--Borderes:#f7f7f7;--Borderes2:#f7f7f7;--Borderes3:#eee;--PostTxtColor:$(PostsTextColor);--PostTitleColor:$(PostsTitleColor);--PostLinkColor:$(PostsLinkColor);--Hbg:$(BacgroundHeader);--HColor:$(LinkColor);--HbgIcon:$(Bgbuttons);--HCoIcon:$(Cobuttons);--HtitleColor:$(keycolor);--Cpc:$(PostsTextColor);--Cic:$(keycolor);--Hok:$(keycolor);--Sco:$(keycolor);--Gap:2px;--ImgRadius:1px;}

:root body.dark-mode{--BodyBG:#202442;--minColor:#242950;--minColorIc:#fff;--secColor:#242950;--thrColor:#1b2044;--whiteColor:#ffffff;--hoverColor:#3a7bd5;--MinBgColor:#2d325a;--txtColor:#ffffff;--TitColor:#ffffff;--SanColor:#eee;--Borderes:#262b52;--Borderes2:#3e4477;--Borderes3:#2d325a;--PostTxtColor:#eee;--PostTitleColor:#ffffff;--PostLinkColor:#3a7bd5;--Hbg:#2d325a;--HColor:#ffffff;--HtitleColor:#ffffff;--HbgIcon:#242950;--HCoIcon:#fff;--Cpc:#eee;--Cic:#fff;--Hok:#3a7bd5;--Sco:#3a7bd5;}

.dark-mode footer {
background-color: #161a4c;
}


.dark-mode #tocList li a {
color: #03a9f4;
box-shadow: 1px 0px 1px 2px rgb(255 0 247 / 72%);
}

.dark-mode #tocList li {
color: #ffffff;
}

.dark-mode .closed .toctitle {
background: #000000;
}

.dark-mode .toctitle {
color: #fffafa;
}
.dark-mode .post-meta {
background: linear-gradient(to right, #1e90ff, #0c0c0c);
}

.dark-mode .post-body a {
color: #0dffff;
}

.dark-mode #clicksearch, .open.nav1 {
background: #ffffff;
}

.dark-mode #clicksearch svg, .open.nav1 svg {
stroke: #020202;
}

.dark-mode .post-tags a {
background: #fdea09;
color: #192734;
}

.dark-mode a.Lapel-Link {
background: #fdea09;
color: #192734;
}


.dark-mode .post-tags .tagstitle {
background:#0d03cd;

}

.dark-mode .postTopTag {
background:#fdea09;
color: #192734
}

.dark-mode .post-body .button {
background: #ff0000;
color: #ffffff;
}

.dark-mode .post-body h4:not(.rnav-title) {
    border-right: 5px solid #ffffff;
}

.dark-mode #tocList li a:hover {
  color: #ffffff;
  text-shadow: 0px 0px 10px #ffffff;
}

.dark-mode .rnav-title a, .post-title .title {
color: #ffffff;
}

.dark-mode .loadMore div {
background: #fdea09;;
color: #192734;
}


.dark-mode .Headerplace {
background: #161a4c;
}

.dark-mode .HeaderBg {
background: #161a4c;
}

.dark-mode .thumb {
box-shadow: 0 0 18px #ffffff;
}

.dark-mode .toTopB svg .b {
fill: #ffffff;
    stroke: #ffffff;
}

.dark-mode .toTopB svg .c {
    stroke: #1500e7;
}

.dark-mode .Circalewhy svg.line.linedd {
fill: #ffffff!important;
stroke: none;
}

.dark-mode .Circalewhy svg.line.home {
fill: #ffffff!important;
}


.dark-mode .iauthorsvg {
fill: #ffffff;
}


.dark-mode svg.line, svg .line {
    stroke: #ffffff;
}

.dark-mode .Sp-postsnew .posts .rnav-title a:hover {
color: #ffffff!important;
}

.dark-mode .Circalewhy label {
background-color: #0a1670;
}

.dark-mode .post-body {
background: #151a40!important;
}

.dark-mode .bobxed {
background: #151a40!important;
}

.dark-mode .RelatedPosts {
background: #151a40!important;
}

.dark-mode .commentsection {
background: #151a40!important;
}


.dark-mode .pSh {
background: #151a40!important;
}


.dark-mode .post-tags {
background: #151a40!important;
}



.dark-mode .author-posts {
background: #151a40!important;
}

.dark-mode .site .widget {
background: #151a40;
}


.dark-mode .Sp-postsnew .posts .moreLink {
background: #fdea09;
color: #000000;
}


.dark-mode .loadMore div:hover {
background: #e30e0e;
color: #ededed;
}

.dark-mode .postTopTag:hover {
background: #e30e0e;
color: #ededed;
}

.dark-mode a.Lapel-Link:hover {
background: #e30e0e;
color: #ededed;
}

.dark-mode .author-desc {
    color: #ffffff;

    background-color: #151a40;
}

.dark-mode .Sp-posts1 .rnav-title a:hover {
color: #ffffff!important;
}



.dark-mode #loadMoreNomore {
background: #ff0000;
    
}

.dark-mode .HeaderBOT #menu ul li:hover > a {
background-color: #fdea09;
color: #15202b;
}


.dark-mode .HeaderBOT #menu ul a.selected {
background-color: #fdea09;
color: #15202b;
}

.dark-mode .post-body h2:not(.rnav-title) {
  box-shadow: none;
  border: none;
background-color: none;
background: none;
color: #00abfb;
border-bottom: 3px dashed #5fc82f;
display: inline-block;
}

.dark-mode .post-body h3:not(.rnav-title) {
background-color: none;
  border: none;
background: none;
color: #ffda57;
border-bottom: 1px solid #ffda57;
}

ul{margin:0;padding:0}*{text-decoration:none;margin:0;padding:0;outline:0;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,abbr,acronym,address,big,cite,code,del,dfn,em,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td{border:0;font-family:inherit;font-size:100%;font-style:inherit;color:inherit;font-weight:inherit;margin:0;outline:0;padding:0;vertical-align:baseline}img{max-height:100%;max-width:100%;position:relative}

body,input{font:400 15px sans-serif;font-optical-sizing:auto;font-style:normal;font-stretch:normal;line-height:initial}
body{background:var(--BodyBG)}
.widget{overflow:hidden}
.EndSides{overflow:hidden;clear:both;display:block}
.site .widget{display:block;clear:both;overflow:hidden;margin:-23px 0 20px;padding:26px;background:var(--MinBgColor);box-shadow:0 2px 6px 0 rgb(9 32 76 / 4%);border-radius:3px}
.bocker{flex-wrap: wrap;position:relative;display:flex;align-items:flex-start;justify-content:space-between;overflow: hidden;transition: none !important;}
.r-r{position:relative;width:calc(100% - $(sidebar.width) - 20px);overflow: hidden;transition: none !important;}
#sidepar-wid{width:$(sidebar.width);margin-$startSide:20px;overflow: hidden;transition: none !important;}
.Treelists{display:grid;grid-template-columns:repeat(3,1fr);gap:15px;row-gap:0}
.towcol{display:grid;grid-template-columns:repeat(2,1fr);gap:15px;row-gap:0}
.no-items{display:none!important}

.container{width:100%;max-width:$(content.width);margin:0 auto;display:block}
/* HeadLine */
.scrolhide { overflow: hidden; }

.headline,.Followers .title{position:relative;font-size:18px;padding:0 0 10px;border-bottom:2px solid var(--Borderes);display:flex;margin-bottom:15px;align-items:center;justify-content:space-between;color:var(--txtColor)}
.headline:before,.Followers .title:before{content:"";width:0;height:0;position:absolute;bottom:-6px;border-top:6px solid var(--minColorTran);right:0;left:auto;border-left:5px solid transparent;border-right:0;border-top-color:var(--minColorTran)}
.headline .title:after,.Followers .title:after{content:"";background:var(--minColorTran);width:103%;height:2px;position:absolute;bottom:-12px;background-color:var(--minColorTran);right:0;left:auto;z-index:1}
.headline .title {
  position: relative;
  color: #ffffff;
  font-weight: bold;
  font-size: 24px;
background: linear-gradient(to right, #d10d79, #3200f9);  
    padding: 4px 21px;
    border-radius: 100px;
}

@keyframes text3D {
  0% {
    transform: translateZ(0);
  }
  100% {
    transform: translateZ(-20px) rotateY(50deg);
  }
}
.blocker{display:block;overflow:hidden;margin-top:15px}
a.Lapel-Link{text-align:center;transition:all 0.2s linear;float:left;color:var(--whiteColor);background:var(--minColor);position:relative;font-size:13px;padding:0 15px;border-radius:2px;height:28px;line-height:28px}

/* Stats Widget */
.Stats img{width:auto;height:auto;display:inline-block;vertical-align:-4px;-webkit-border-radius:0;-moz-border-radius:0;border-radius:0;margin-$endSide:5px}.Stats .widget-content *{vertical-align:middle}.Stats .widget-content{color:var(--TitColor);text-align:center;font-size:24px;font-family:sans-serif!important}.Stats .digit strong{background:#eee;margin:0 3px;border-radius:3px;padding:0 8px}
/* social Icon's */
aside .social-static.social li a svg{fill:#fff;width:111;height:50x}.social-static.social li a svg{fill:#fff;width:111px;height:50px}.shmal .social-static.social li{float:$startSide;vertical-align:middle;margin-$startSide:5px;list-style:none}aside .social-static.social li{float:$startSide;vertical-align:middle;list-style:none;width:calc((100% - 15px) / 4);margin-$endSide:5px;margin-bottom:5px;padding-bottom:0;border:0}aside .social-static.social li a{background: #aaa;border-radius:5px;justify-content:center;height:50px;display:flex;align-items:center}aside .social-static.social li:nth-of-type(4n+4){margin-$endSide:0}.social-static.social{display:block;overflow:hidden;vertical-align:middle}.shmal .social-static.social li{float:$startSide;vertical-align:middle;margin-$startSide:5px;list-style:none;padding-bottom:0;margin-bottom:0;border:0}.shmal .social-static.social li a{;display:flex;align-items:center;justify-content:center;width:90x;height:50x;border-radius:22px;background:#888}.shmal .social-static.social li:first-of-type{margin-$startSide:0}

/* social Icon Color's */
.social a[title="sitemap"] {background: var(--minColor) !important;}.social a[title="email"]{background-color:#ea4335!important}.social a[title="line"]{background-color:#06c152!important}.social a[title="facebook"]{background-color:#1778F2!important}.social a[title="twitter"]{background-color:#1da1f2!important}.social a[title="rss"]{background-color:#f26522!important}.social a[title="dribbble"]{background-color:#ea4c89!important}.social a[title="google-plus"]{background-color:#dd4b39!important}.social a[title="pinterest"]{background-color:#cc2127!important}.social a[title="linkedin"]{background-color:#0976b4!important}.social a[title="wordpress"]{background-color:#00769d!important}.social a[title="github"]{background-color:#000000!important}.social a[title="youtube"]{background-color:#e52d27!important}.social a[title="quora"]{background-color:#a82400!important}.social a[title="spotify"]{background-color:#1ed760!important}.social a[title="snapchat"]{background-color:#f5d602!important}.social a[title="flickr"]{background-color:#FF0084!important}.social a[title="instagram"]{background-color:#7c38af;background:radial-gradient(circle at 0 130%,#fdf497 0%,#fdf497 5%,#fd5949 45%,#d6249f 60%,#285AEB 90%)!important}.social a[title="behance"]{background-color:#009fff!important}.social a[title="whatsapp"]{background-color:#128C7E!important}.social a[title="soundcloud"]{background-color:#FF5419!important}.social a[title="tumblr"]{background-color:#3e5a70!important}.social a[title="khamsat"]{background-color:#f9b01c!important}.social a[title="tradent"]{background-color:#59c5c4!important}.social a[title="blogger"]{background-color:#fc9644!important}.social a[title="telegram"]{background-color:#32AEE1!important}.social a[title="google-play"]{background-color:#3d9dab!important}.social a[title="mostaql"]{background-color:#2caae2!important}.social a[title="messenger"]{background-color:#0084ff!important}.social a[title="paypal"]{background-color:#193685!important}.social a[title="reddit"]{background-color:#ff4500!important}.social a[title="vk"]{background-color:#45668e!important}.social a[title="website"]{background-color:#444444!important}a[title="website:before"]{content:"\f0ac"!important}
/* Style Headr */

li.item:hover > ul{opacity:1;visibility:visible;transform:translateY(0)}
li.item > ul,li.sitem > ul{height:auto!important;display:block!important;position:absolute;right:0;width:200px;background:var(--Hbg);top:60px;box-shadow:0 0 5px 1px rgb(0 0 0 / 8%);z-index:9;opacity:0;visibility:hidden;transition:all .2s linear;transform:translateY(20px);border-radius:3px;border-top:2px solid var(--OldMin)}
li.item > ul:before{content:"";width:25px;height:25px;position:absolute;background:var(--Hbg);top:-10px;right:8%;border-radius:8px;transform:rotate(45deg);box-shadow:0 0 5px 1px rgb(0 0 0 / 8%);z-index:-1;border:2px solid var(--OldMin)}
li.item > ul li.sitem{display:block!important;padding:0!important;margin:0!important;background:#fff200;border-radius:3px}
li.item > ul li.sitem a {
  color: #000000;
  padding: 14px;
  margin: 0!important;
  display: block;
  position: relative;
  border-radius: 3px;
  overflow: hidden;
  background: #ff0000; /* لون خلفية النص الافتراضي */
}

/* لون النص وخلفية النص على أجهزة الكمبيوتر والأجهزة اللوحية */
@media only screen and (min-width: 768px) {
  li.item > ul li.sitem a {
    color: #ff0000;
    background: #ff0000; /* لون خلفية النص على الكمبيوتر */
  }
}

/* لون النص وخلفية النص على أجهزة الهواتف المحمولة */
@media only screen and (max-width: 767px) {
  li.item > ul li.sitem a {
    color: #000000;
    background: #ffffff; /* لون خلفية النص على الهواتف المحمولة */
  }
}
li.sitem > ul{transform:translateX(-30px);right:100%;top:0;border-right:2px solid var(--OldMin);border-top:0}
li.sitem > ul:before{content:"";width:26px;height:26px;position:absolute;background:var(--Hbg);top:10px;right:-10px;z-index:-1;transform:rotate(45deg);border:1px solid var(--Borderes);box-shadow:0 0 5px 1px rgb(0 0 0 / 8%);border:2px solid var(--OldMin);border-radius:8px}
li.sitem:hover > ul{transform:translateX(0);opacity:1;visibility:visible}
li.sitem:last-of-type > a{border-bottom:0!important}
li.ssitem:last-of-type > a{border-bottom:0!important}
li.ssitem{border-radius: 8px;background: var(--MinBgColor);padding:0!important;float:none;margin:0!important;width:100%}
.targetitem li a:hover:before{color:var(--hoverColor)!important}
nav.nav-par ul li a:hover{color:var(--hoverColor)}
div#menu i.fa{display:inline-block;vertical-align:middle;margin-$endSide:5px}
.icon.arrow-down{z-index: 9;transition:all .3s linear;display:block;position:absolute;top:19px;left:5px;right:auto;--Cic: #ffffff;}
.item.targetitem:hover .icon{top:23px}
.item.targetitem:hover .icon:after{transform:rotate(-45deg)}
.item.targetitem .icon:after{user-select:none;content:"";display:inline-block;width:8px;height:8px;background:transparent;border:2px solid var(--Cic);border-bottom-color:transparent;border-left-color:transparent;transform:rotate(135deg);border-radius:3px;transition:all 0.3s}
.item.targetitem .targetitem span.icon{left:13px!important;top:14px!important;right:auto!important}
.item.targetitem .targetitem:hover span.icon{$endSide:20px!important}
.item.targetitem{padding-$endSide:30px!important}
.sitem:hover  > a,.ssitem:hover > a{background:rgb(0 0 0 / 5%) !important}
.sitem.targetitem .icon:after{transform:rotate(225deg)!important;width:6px;height:6px}
/* headr sidenav  */
.pos-t-t,.Sittings{display:none;position:fixed;top:0;$endSide:0;$startSide:0;bottom:0;;z-index:999}
#NavM:checked ~ .contenarpage .pos-t-t{display:block}

.sidenav img {
  display: block;
  margin: 0 auto;
}

.sidenav div {
  margin-top: 0;
}

.sidenav{transition: all 0.5s cubic-bezier(1, -0.12, 0, 1.15);height:100vh;width:320px;position:fixed;top:0;bottom:0;right:-500px;background-color:rgb(4, 10, 148);z-index:9999;max-width:100%;box-shadow:-4px 0 10px 0 rgb(0 0 0 / 8%)}
#NavM:checked ~ .contenarpage .sidenav{$startSide:0}
.sidehead{position:absolute;width:45px;height:45px;left:-40px;top:20px;overflow:hidden;display:flex;align-items:center;background:#00a4dd;border-radius:50% 0 50% 50%;justify-content:center;box-shadow:-2px 3px 0 0 rgb(0 0 0 / 8%);border-right:0}
.closemenu{display:flex;height:100%;color:#fff;font-size:16px;align-items:center;cursor:pointer;padding:0 19px}
.closemenu:after{content:'\2715';line-height:18px;font-size:14px;font-weight:bold}
.flexmenu {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: flex-start;
  overflow: hidden;
  flex-direction: column;
  overflow-y: scroll;
  margin: 0;
  padding-bottom: 200px;
  background-color: #070031;
}
.flexmenu .MegaItem .mega-wraper{display:none!important}
.SiteInfo{padding:20px 20px  5px;border-bottom:1px solid var(--Borderes)}
.SiteInfo .navlogo img{max-width:100%;max-height:100%;display:inline-block}
.SiteInfo .navlogo{text-align: center;display:block;margin:0 auto 15px}
.SiteInfo .navtitle{display:block;padding:10px 0;font-size:21px;background:var(--Borderes);margin-bottom:15px;color:var(--txtColor);text-align:center;border-radius:5px}
.navdis{display:block;max-height:8em;overflow:hidden;margin-bottom:15px;color:var(--txtColor);opacity:.9;font-family:sans-serif!important;text-align:center}

.mainmenu{position:relative;width:100%;padding:16px}
.mainmenu ul li{position:relative;display:block;overflow:hidden;width:100%;margin:0!important}
.mainmenu ul li a{font-size:15px;color:#fff;padding:15px 0;display:block;border-bottom:1px solid rgb(0 0 0 / 8%)!important}
.mainmenu .item.targetitem{padding-left:0!important}
.mainmenu .targetitem ul a:before{content:'.';font-size:30px;line-height:0;display:inline-block;vertical-align:middle;margin-left:5px;top:-6px;position:relative}

.mainmenu ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0;
}

.mainmenu ul li {
  position: relative;
  width: 100%;
  text-align: center;
  margin-bottom: 10px; /* تباعد عمودي بين العناصر */
}

.mainmenu ul li a:hover {
  background-color: #0000ff;
  animation: wave 0.8s ease-in-out;
  animation-iteration-count: 1;
  color: #fff; /* تغيير لون النص إلى اللون الأبيض */
  text-shadow: 0px 0px 5px rgba(255, 255, 255, 0.8); /* إضافة ظل للنص */
}

.mainmenu ul li a:hover:before {
  background-color: #fff;
  box-shadow: 0px 0px 20px #fff;
  transform: translateY(50%) scale(2);
}

@keyframes wave {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
.bottommeny{display:block;padding:20px;border-top:1px solid var(--Borderes)}
.bottommeny{padding-bottom:100px}
.bottpage ul{list-style:none;margin-bottom:10px}
.bottpage ul li{display:inline-block;  margin-bottom: 5px;margin-right: 5px;}
.bottpage ul li a{font-size:15px;font-family:sans-serif;}
.bottpage ul li a:hover {transform: translateX(10px);}
.bottpage a {display: inline-block;padding: 5px;background-color: black;color: white;border-radius: 10px;margin-right: 10px;}
.bottpage ul li{color: #ffffff;}

.bottsocial .social-static li{display:inline-block;margin-left:0px;font-size: 200%;}
.bottsocial .social-static li a svg {
width: 2em;height: 1em;height: 30px;}
.mainmenu .item.targetitem .icon{transform:none!important;border-radius:3px;left:0!important;top:14px!important;background:#00a4dd;color:#202124;width:30px;height:25px;line-height:25px;padding-top:4px;display:flex;align-items:baseline;justify-content:center}
.mainmenu .item.targetitem .icon:after{transform:rotate(135deg)!important}
.mainmenu ul li a i{font-size:14px;color:var(--TitColor);margin-$endSide:5px}
.sidenav .targetitem ul.open{display:block!important}
.sidenav .targetitem ul{box-shadow: none !important;position:relative!important;opacity:1!important;visibility:visible!important;transform:unset!important;display:none!important;width:auto!important;top:0!important;right:0!important;margin-top:10px;border:0!important;border-top:1px solid var(--Borderes)!important;border-bottom:1px solid var(--Borderes)!important}
.sidenav .targetitem ul:before{border:1px solid var(--Borderes);right:45%;box-shadow:none!important}
.sidenav .sitem.targetitem .icon{$endSide:5px!important;transform:rotate(180deg)!important}
.sidenav .sitem.targetitem span.icon{transform:rotate(0deg)!important}
.sidenav .targetitem.sitem ul.open{padding-right:10px;margin:3px 0;position:relative!important}
.sidenav .targetitem.sitem ul.open:before{top:-8px!important}
.mainmenu .item.targetitem span.icon,.mainmenu .item.targetitem .targetitem:hover span.icon{left:10px!important}
.mainmenu .item.targetitem.open > span.icon,.sidenav .sitem.targetitem.open > span.icon{background: var(--Sco);--Cic: #fff;}
.bottpage ul li:last-child:after{display:none}
.mainmenu .sitem:hover > a,.mainmenu .ssitem:hover > a{background:transparent!important}
/* Aside */
.FeaturedPost .item-thumbnail.thumb{margin-$endSide: 0;float: none;width:100%;padding-top: 56.25%;margin-bottom:5px}
.FeaturedPost .post-title .title{overflow:hidden;display:block;font-size:15px;color:var(--TitColor);max-height:4.9em;line-height:1.6em;background-size:0!important}
.FeaturedPost .snippet-item{color:var(--SanColor);font-size:13px;font-family:sans-serif!important;line-height:18px;margin-top:5px;overflow:hidden}.Profile .profile-img{display:block;margin:0 auto 20px;border-radius:50%}.Profile .profile-link.g-profile{color:var(--txtColor);background:var(--secColor);display:block;text-align:center;padding:10px;margin-bottom:15px;border-radius:3px;font-family:'Tajawal',sans-serif!important;font-size:inherit!important;opacity:1}.Profile .profile-data.location{display:none}.Profile .profile-textblock{color:var(--SanColor);font-size:15px;font-family:sans-serif!important;margin-bottom:15px;text-align:center;display:block}.Profile .profile-link{color:#ffffff;background:#3560ab;display:block;text-align:center;padding:10px;border-radius:3px;font-family:sans-serif!important;font-size:13px;opacity:0.7}.Profile .profile-link:hover{opacity:1}.BlogSearch input{background:transparent;font-family:sans-serif!important;color:var(--txtColor);display:inline-block;font-size:13px;padding:10px;border-radius:3px;width:55px;border:1px solid var(--Borderes)}.BlogSearch input[type="submit"]{transition:all 0.3s;background:var(--secColor);border:0;cursor:pointer}.search-input input:hover,.search-input input:focus{border-color:#4b9ce7}.search-input{display:inline-block;width:calc((100% - 60px) / 1)}.search-input input{display:block;width:100%}aside .LinkList ul li,footer .LinkList ul li,aside .PageList ul li,footer .PageList ul li{padding-bottom:8px;margin-bottom:8px;border-bottom:1px solid var(--Borderes);list-style:none}aside .LinkList ul li a,footer .LinkList ul li a,aside .PageList ul li a,footer .PageList ul li a{font-family:sans-serif!important;color:var(--TitColor);display:block}.list-label-widget-content ul li{display:block;padding-bottom:8px;margin-bottom:8px;border-bottom:1px solid var(--Borderes)}.list-label-widget-content ul li a{font-family:sans-serif!important;color:var(--TitColor);display:block}aside .LinkList ul li a:before, footer .LinkList ul li a:before, aside .PageList ul li a:before, footer .PageList ul li a:before, .list-label-widget-content ul li a:before{vertical-align:baseline;display:inline-block;width:4px;height:4px;content:"";margin-left:10px;background:transparent;border:1.7px solid var(--txtColor);border-bottom-color:transparent;border-left-color:transparent;transform:rotate(225deg);font-family:inherit!important}
.list-label-widget-content .label-count{float:$endSide;background-color:var(--minColor);text-align:center;font-size:13px;padding:0 5px;min-width:24px;height:20px;line-height:20px;color:var(--whiteColor);border-radius:2px;font-family:sans-serif!important}.list-label-widget-content li:hover .label-count{opacity:1}.cloud-label-widget-content{justify-content:center;display:flex;justify-content:flex-start;flex-wrap:wrap}span.label-size{flex-grow:1}.cloud-label-widget-content .label-count{margin-$startSide:10px;background:var(--MinBgColor);font-size:13px;padding:0 5px;min-width:20px;height:18px;line-height:18px;text-align:center;border-radius:3px;color:var(--txtColor)}
.cloud-label-widget-content .label-name{transition:all 0.3s;display:flex;padding:0 13px;justify-content:space-between;align-items:center;background:var(--minColor);font-family:sans-serif!important;margin:0 0 6px 5px;color:var(--whiteColor);font-size:15px;border-radius:3px;height:35px;line-height:35px}
input.follow-by-email-address{display:block;width:100%;height:40px;margin:15px 0;border-radius:3px;border:1px solid #efefef;text-align:center}input.follow-by-email-submit{background:#eee;border:1px solid #ccc;padding:10px;border-radius:3px;width:100%;text-align:center;color:#6b6b6b;font-size:12px;cursor:pointer}input.follow-by-email-address::placeholder{font-weight:normal;font-size:14px}div#ArchiveList ul.hierarchy{padding-$startSide:30px}div#ArchiveList ul.hierarchy ul.hierarchy{padding-$startSide:15px}div#ArchiveList ul.hierarchy ul.hierarchy ul.hierarchy  li:not(:last-of-type){margin-bottom:5px;padding-bottom:5px}div#ArchiveList ul.hierarchy li a,div#ArchiveList ul.flat li a{color:#121212}div#ArchiveList ul.hierarchy ul.hierarchy ul.hierarchy li:first-of-type{margin-top:5px;padding-top:5px}div#ArchiveList ul.hierarchy li{font-size:11px}div#ArchiveList ul.hierarchy li a:hover,div#ArchiveList ul.flat li a:hover{color:$(step.color)}div#ArchiveList .hierarchy-title{font-size:13px;margin-bottom:5px;padding-bottom:5px;border-bottom:1px solid #f7f7f7}div#ArchiveList .hierarchy-title span.post-count,div#ArchiveList ul.flat li span.post-count{float:$endSide;width:25px;padding:0 0;text-align:center;background:#eee;border-radius:3px;border:1px solid #ccc;font-size:12px;font-weight:normal}div#ArchiveList ul.flat{padding-$startSide:30px}div#ArchiveList ul.flat li:not(:last-of-type){margin-bottom:5px;padding-bottom:5px}div#ArchiveList ul.flat li{font-size:13px}.ContactForm textarea[name="email-message"],.ContactForm input[type="text"]{margin:0 auto 10px;border:1px solid var(--Borderes);width:100%;border-radius:3px;padding:10px 15px;background:transparent;font-family:sans-serif!important}.ContactForm textarea[name="email-message"]:hover,.ContactForm input[type="text"]:hover,.ContactForm textarea[name="email-message"]:focus,.ContactForm input[type="text"]:focus{border:1px solid #4b9ce7}textarea[name="email-message"]{min-height:130px;resize:vertical}.ContactForm input[type="button"]{transition:all 0.3s;display:inline-block!important;position:relative;font-size:14px;background:var(--secColor);color:var(--txtColor);padding:7px 20px;border-radius:3px;font-family:sans-serif!important;border:none;float:$endSide;cursor:pointer}p#ContactForm1_contact-form-error-message{font-family:sans-serif!important}p#ContactForm1_contact-form-success-message{font-family:sans-serif!important;color:#30bb81}
/* nextprev  */
.page-navigation{display:flex!important;align-items:center;justify-content:space-between}div#siki_next a,div#siki_prev a{width:42px;height:42px;display:flex;align-items:center;justify-content:center;background:var(--minColor);color:var(--whiteColor);font-size:25px;border-radius:3px}.sikinot{opacity:0.7}.sikinot a{pointer-events:none}div#siki-page-number{font-size:16px;font-family:sans-serif;color:var(--txtColor)}
/* InPost And Page*/
.post-body{font:$(PostsTextFont);line-height:2em;overflow:hidden;color:var(--PostTxtColor)}.post-body a{color:var(--PostLinkColor)}.post div#Blog1,.post .post-outer,.post .post-body{overflow:initial!important}.post div#Blog1,.page div#Blog1{display:block;background:transparent;border-radius:0;padding:0;border:0;margin:0;box-shadow:none;margin-bottom:15px}.bobxed,.commentsection,.pSh,.post-tags,.shareButton,.RelatedPosts,.author-posts,.post-body,.page-navigation{display:block;background:var(--MinBgColor)!important;clear:both;padding:20px!important;overflow:hidden;border-bottom:1px solid var(--Borderes)}
.post .post-body p{margin:1.5em 0;font: normal 400 25px;}
.post .post-body img {
margin: 0.9em 0 -1.1em 0
}
.post-body h1:not(.rnav-title),.post-body h2:not(.rnav-title),.post-body h3:not(.rnav-title),.post-body h4:not(.rnav-title){margin:1em 0;line-height:1.5em}
.post-body h1{font-size:1.9rem}
.post-body h2{font-size:35px}
.post-body h3:not(.rnav-title){font-size:30px}
.post-body h4{font-size:1.4rem}
.post-body sup {vertical-align: super;font-size: smaller !important;}
.post-body sub {vertical-align: sub;font-size: smaller;}
.post-meta {
display: flex;
align-items: center;
justify-content: space-between;
margin-top: 15px;
background: linear-gradient(to right, #ff1ee3, #002bff);
border-radius: 15px;
padding: 5px;
animation: fadeInUp 0.8s ease-out;
box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.3);
}

.post-meta .au-ti {
display: flex;
align-items: center;
font-size: 14px;
color: #fff;
}

.post-meta .au-ti .author {
margin-right: 10px;
}

.post-meta .au-ti .reading-time {
display: inline-flex;
align-items: center;
justify-content: center;
padding: 0 10px;
margin-left: 10px;
background-color: #fff;
color: #1e90ff;
border-radius: 5px;
font-weight: 600;
}

.post-meta .au-ti .updated-at {
margin-left: auto;
color: #fff;
font-weight: 600;
}

.post-title {
font-size: 36px;
font-weight: 600;
margin: 0;
color: #fff;
}

/* تأثير حركة */
@keyframes fadeInUp {
0% {
opacity: 0;
transform: translateY(30px);
}
100% {
opacity: 1;
transform: translateY(0px);
}
}
.metapost{display:inline-flex;flex-wrap:wrap;align-items:center;justify-content:center;line-height:20px}
.Times{display:inline-block;white-space:nowrap;text-overflow:ellipsis;overflow:hidden;max-width:100%}
.Times > div{display:inline}
.authorname {
  margin-$endSide: 8px;
}

.authorPhoto {
  width: 36px;
  height: 36px;
  object-fit: cover;
  border-radius: 8px;
  margin-left: 5px;
}

.iauthorsvg {
  width: 30px;
  height: 30px;
  fill: #1300fc;
  padding: 0 5px;
  display: inline-block;

}
.readTime:before{content:'';margin:0 5px;width:13px;height:1px;background:var(--txtColor);display:inline-block;vertical-align:middle}
.article-author,.article-timeago,.readTime{display:flex;align-items:center;justify-content:center;color:#ffffff}
.topcs7v{margin-bottom:15px;position:relative;width:100%;display:flex;flex-direction:column;overflow:hidden;border-top:1px solid var(--Borderes)}
.toctitle{border-bottom:0px solid var(--Borderes);cursor:pointer;position:relative;height:40px;font-size:20px;color:#f1f1ff;display:flex;align-items:center;justify-content:flex-start;padding:0 15px;margin:0;width:100%}
.toctitle:before{content:'\002B';margin-left:10px;font-size:21px; color: #9900ff;}
.toctitle:after{content:"{عرض الجدول}";float:left;font-family:sans-serif;margin-right:10px;font-size:20x;position:absolute;left:15px;text-align:center;line-height:26px;border-radius:3px;}
#tocList{padding:0px;display:none;border-bottom:1px solid var(--Borderes)}
#tocList li{list-style:decimal inside;font-size:14px;line-height:1.7;margin-bottom:0;padding-bottom:0;color:#0000ff;}
#tocList li a{color:var(--txtColor)}
#tocList li a {
  color: #ff0000;
  text-decoration: none;
  font-weight: bold;
  position: relative;
  transition: all 0.3s ease-in-out;
  padding: 0px 5px;
  border-radius: 10px;
  box-shadow: -4px -2px 6px 2px #cd0303;
}

#tocList li {
  list-style: decimal inside;
  font-size: 18px;
  line-height: 2;
  margin-bottom: 0;
  padding-bottom: 0;
}


#tocList li a:hover {
  color: #0000ff;
  text-shadow: 0px 0px 10px #ff00ff;
}

#tocList li a::before,
#tocList li a::after {
  content: "";
  display: block;
  height: 1px;
  width: 0;
  background-color: #0000ff;
  position: absolute;
  z-index: 1;
  transition: all 0.2s ease-in-out;
}

#tocList li a::before {
  top: 2px;
  left: 0;
}

#tocList li a::after {
  bottom: 2px;
  right: 0;
}

#tocList li a:hover::before,
#tocList li a:hover::after {
  width: 100%;
}

#tocList li a:hover::before {
  transform: translateY(-100%);
}

#tocList li a:hover::after {
  transform: translateY(100%);
}

.closed .toctitle:before{content:'\2212'}
.closed #tocList{display:block}
.toctitle:hover,.closed .toctitle{background:#141d99;}
.closed .toctitle:after{content:'{أخفاء الجدول}'}
.tr-caption {
font-family: sans-serif!important;
font-size: 15px;
line-height: 2.5em;
opacity: 1.0;
font-style: italic;
}
.post-body img{border-radius:19px;width:auto;height:auto;display:inline}
.separator,.separator a,a[imageanchor="1"],a[style*='1em']{text-align:center;margin:0!important}
.post-body strike{text-decoration:line-through}
.post-body u{text-decoration:underline}
.post-body ul,.post-body ol{padding:0 15px 0 0;margin:10px 0}
.post-body li{margin:5px 0;padding:0}
.post-body ul li{list-style:disc inside}
.post-body ol li{list-style:decimal inside}
.post-body ul ul li{list-style:circle inside}
.post-body blockquote {
  position: relative;
  padding: 15px 25px;
  margin: 0;
  font-size: 15px;
  background: linear-gradient(45deg, #FF3CAC, #784BA0, #2B86C5, #00D7FF);
  background-size: 600% 600%;
  color: var(--PostTxtColor);
  animation: gradientAnimation 12s ease infinite;
}

@keyframes gradientAnimation {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.post-body blockquote *{display:initial!important}
div#AddOns{display:none;opacity:0;visibility:hidden}
.post-amp .topic-title{overflow:hidden;font:$(PostsTitleFont);line-height:1.7em;color:var(--PostTitleColor)}
.hideensa{overflow:hidden;display:block;clear:both}
.foqTitle{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px}
.FTBU{display:flex}
.postTopTag{color:var(--whiteColor);background:var(--minColor);font-size:13px;padding:4px 13px;border-radius:3px;border-radius: 50px;}
.postTopTag:hover{background:var(--minColor)}
.OpenSitting,.gocomments{cursor:pointer;margin-right:10px;width:40px;height:28px;display:flex;align-items:center;justify-content:center;position:relative;border-radius:3px;border:1px solid rgb(0 0 0 / 5%)}
.gocomments{margin:0}
.OpenSitting:hover,.gocomments:hover{background:rgb(0 0 0 / 6%)}
.gocomments svg,.OpenSitting svg{width:18px;height:18px;fill:var(--minColorIc)}
.numcomment{position:absolute;top:-10px;right:-5px;background:#ddd;padding:0 7px;color:#333;font-size:13px;border-radius:3px}
.post-tags{flex-wrap:wrap;padding-bottom:15px!important;display:flex;align-items:center;justify-content:flex-start}
.post-tags a{background:rgba(0,0,0,5%);color:var(--txtColor)}
.post-tags .tagstitle{background:var(--minColor);color:var(--whiteColor);margin-$endSide:10px}
.post-tags span,.post-tags a{margin-bottom:5px;flex-shrink:0;transition:all 0.3s;border-radius:2px;padding:0 10px;line-height:26px;margin-$endSide:7px;position:relative;font-size:13px}
.tagstitle:before{content:'';position:absolute;top:10px;$endSide:-3px;width:6px;height:6px;background-color:var(--minColor);transform:rotate(45deg)}

/* SeoPlusAds  */
div#Topa3lan-sc .HTML,div#Topa3lan-sc2 .HTML{box-shadow:none;background:transparent!important;padding:0!important;border:0;margin:0}div#PostA3lan .widget,div#PostA3lan2 .widget{background:transparent!important;border:0!important;padding:0 20px!important;margin:0!important;box-shadow:none!important}
#Blog1 .clearhtml > .HTML{background:var(--MinBgColor)!important;margin:0;padding:20px 0!important;border-bottom:1px solid var(--Borderes)}
.SeoPlusAds,#Blog1 .HTML{font-family:sans-serif;background:transparent!important;margin:15px 0;text-align:center;font-size:13px;display:block;clear:both;border:none;overflow:unset!important;box-shadow:none;padding:0!important;border-radius:0}div#HTML100 .SeoPlusAds{margin-top:0}div#top-a3lan .HTML{margin-top:0}div#bot-a3lan .HTML{margin-bottom:0}.pnavigation .HTML{margin-bottom:15px!important}div#bot-a3lan,div#top-a3lan,div#ret-a3lan{overflow:initial}div#ret-a3lan .HTML{background:var(--MinBgColor)!important;padding:15px 0!important;margin:0!important;border-bottom:1px solid var(--Borderes)}
/* comments */
.bloggerComment{background:#fc9644}
.comments-tabs .active,.comments-tabs span:hover{opacity:1}
.noimg{background:transparent url(https://4.bp.blogspot.com/-ci3XMoAMGzg/WiCTxCLLWeI/AAAAAAAAPjI/UkV1sBTKC7EamOC_UmMJ4cQCv4xNNI82QCLcBGAs/s83/log.jpg) no-repeat center;display:block;width:38px;height:38px;background-size:38px}
.avatar-image{width:38px;height:38px;position:absolute;top:0;right:0;border-radius:8px;overflow:hidden}
.CommentCounter{position:relative}
.cmt-user{font-family:sans-serif!important;font-size:14px;color:var(--txtColor)}
.comment-block{padding-right:45px}
.comment{position:relative;padding:0;margin:15px 0 0;padding-top:15px;list-style:none;border-radius:0;border-top:1px solid rgb(0 0 0 / 2%)}
.comment-replies{padding-right:45px}
.comment .comment-replies .comment:not(:first-child){border-top:0}
.comments .comment-content{font-size:14px;color:var(--Cpc);line-height:1.6em;margin:6px 0 10px;padding:10px;background:rgb(0 0 0 / 5%);border-radius:12px 2px 12px 12px;display:inline-block;white-space:pre-wrap}
.comments .comment-actions{display:flex;margin:0;align-items:center}
.comment-actions .comment-reply,.comment-actions a{margin-left:10px;font-size:13px;color:var(--txtColor);cursor:pointer;font-family:sans-serif!important;line-height:1em}
.comment-actions .comment-reply{padding-left:10px;border-left:1px solid rgb(9 32 76 / 2%)}
.comment-actions .comment-reply:hover,.comment-actions a:hover{text-decoration:underline}
.ShowMoreCMT,.PostEdit a{display:inline-block;padding:7px 22px;text-align:center;font-size:15px;background:var(--minColor);margin-top:20px;cursor:pointer;border-radius:3px;color:var(--whiteColor);line-height:1.3em;transition:all .2s linear}
#comments-respond,.comment-replies #comment-editor{padding:15px;border-radius:8px;border:1px solid rgb(9 32 76 / 2%);background:rgb(9 32 76 / 2%);min-height:100px}
.comment-replies #comment-editor{margin-top:10px}
.conart{margin-bottom:10px;display:block;padding-bottom:15px;border-bottom:1px solid rgb(9 32 76 / 5%)}
#comment-post-message{font-size:15px;color:var(--txtColor);display:inline-block;background:rgb(0 0 0 / 5%);padding:4px 10px;border-radius:3px}
#comment-post-message:hover{background:rgb(0 0 0 / 8%)}
.conart p{font-size:15px;font-family:sans-serif!important;color:var(--txtColor);margin-top:5px}

/* author profile  */
.authorImage{float:$startSide;width:60px;height:60px;margin-$endSide:15px}

.authorImage .authorImg {
    overflow: hidden;
    width: 60px;
    height: 60px;
    margin-top: -20px;
}
.author-posts{align-items:flex-start}.author-name{font-size:18px;color:var(--txtColor);margin-bottom:12px}


.author-desc {
    font-family: 'Arial', sans-serif;
    color: #4f09d7;
    font-size: 15px;
    border: 2px solid #4f09d7;
    border-radius: 43px;
    padding: 20px;
    background-color: #f9f9f9;
    box-shadow: 0 0 10px rgb(0 0 0 / 100%);
    text-align: justify;
    margin: 0 auto;
    width: 100%;
}




/* PageRedirect  */
div#pageredirect{position:relative}.cLoaderWrap{text-align:center;width:260px;margin:0 auto;position:relative;font-style:normal;display:block}#cLoaderSVG{-webkit-transform:rotate(140deg);transform:rotate(140deg);width:260px;height:260px;display:block}.cPath{stroke-dashoffset:0;stroke-dasharray:500;r:110;cy:130;cx:130;stroke-width:20px;stroke:var(--Borderes2);fill:none}.cLoader{stroke-dashoffset:500;stroke-dasharray:500;-webkit-transition:all 1s linear;transition:all 1s linear;r:110;cy:130;cx:130;fill:none;stroke-width:20px;stroke:var(--minColor)}.hLoader{stroke-dashoffset:500;stroke-dasharray:500;-webkit-transition:all 1s linear;transition:all 1s linear;r:110;cy:130;cx:130;fill:none;stroke-width:22px;stroke:var(--MinBgColor)}.page .cCount{top:105px}.cCount{position:absolute;top:90px;$startSide:calc(50% - 30px);font-size:60px;width:66px;font-family:Arial!important;display:block;margin-bottom:0;color:var(--TitColor);text-align:center}.cButton{text-align:center}
a.cLink{position:absolute;bottom:20px;right:0;user-select:none;left:0;z-index:8;border-style:solid;border-width:5px;border-color:rgba(0,0,0,0.03);display:inline-block;background-color:#f8f8f8;padding:0 15px;width:160px;font-size:14px;margin:0 auto;border-radius:50px;color:#d2d2d2!important;cursor:progress;height:40px}
a.cLink.ready:hover{border-color:var(--minColor);background:var(--minColor);color:#fff!important}
a.cLink.ready{cursor:pointer;color:#3c5b92!important;border-color:var(--minColor);border-style:double;transition:all 0.3s}
a.cLink.err{cursor:no-drop;background-color:#ffcfcf;color:#de6262!important}
div#ReadPage{z-index:99999;position:fixed;display:none;background:rgba(0,0,0,.2);backdrop-filter:saturate(100%) blur(2px);right:0;left:0;top:0;bottom:0;width:100%;height:100%}
.ReadPage-popup{width:calc(100% - 40px);height:auto!important;min-height:calc(100% - 40px);max-height:calc(100% - 40px)!important;display:flex;margin:20px}
.ReadPage-popup-cont{width:100%;position:relative;direction:unset;display:flex;border-radius:8px;margin:0 auto;flex-direction:column;height:auto!important;max-width:900px!important;overflow:hidden;padding-bottom:0!important}
.modal-head{font-size:21px;background:var(--MinBgColor);height:60px;line-height:60px;padding:0 20px;color:var(--txtColor);border-bottom:1px solid var(--Borderes3);display:flex;align-items:center;justify-content:space-between}
.mdltitle{width:90%;display:block;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.modal-close{background-color:var(--minColor);width:40px;height:40px;text-align:center;color:#FFF;cursor:pointer;border-radius:3px;display:flex;align-items:center;justify-content:center}
.modal-close:after{content:'\2715';line-height:0;font-size:10px;font-weight:bold;font-family:inherit}
.modal-body.post-body .cCount{top:110px}
.ReadPage-popup .ReadPage-popup-cont .modal-body.post-body{background-color:var(--MinBgColor)!important;overflow:hidden!important;padding:20px!important;box-shadow:none!important;margin:0!important;border:0!important;height:100%!important;overflow-y:scroll!important;display:block}
.PagePrakediv{text-align:center;line-height:1.6em;margin-top:20px}
.PagePrakediv a{color:var(--whiteColor)!important;line-height:1.6em;background:var(--minColor);border-radius:3px;cursor:pointer;display:inline-block;transition:all .2s linear;font-size:14px;padding:8px 25px;position:relative}
.PagePrakediv a:hover,a.Lapel-Link:hover,.moreLink:hover,.loadMore div:hover,.ShowMoreCMT:hover,.PostEdit a:hover{transform:translateY(-2px);background:var(--minColor);box-shadow:0 16px 18px 0 rgb(137 137 137 / 32%)}

.ReadPage-popup-cont .icon-load{position:unset;width:50px;height:50px;display:block}.modal-title .icon-load{width:25px;height:25px}.ay7aga{display:flex;align-items:center;justify-content:center;height:80vh}
/* footer  */
footer{overflow:hidden;display:block;clear:both;background:rgb(4 10 148);border-top:0px solid var(--Borderes3)}.mid-top-footer{overflow:hidden;display:flex;justify-content:space-between}.footer-col{padding:0 10px;width:100%;min-width:25%}.footer-col.no-items{display:none}footer .container{display:block;overflow:hidden}.mid-top-footer .footer-col .widget{margin-top:15px;margin-bottom:30px;vertical-align:top}.mid-top-footer .footer-col .widget:last-of-type{margin-bottom:20px}.bottom-footer .container{padding:0 15px}.bottom-footer{display:block;overflow:hidden;padding:10px 0;margin-top:0}.yemen{min-height:32px;font-size:13px;float:$startSide;display:flex;align-items:center;color:#ffffff;}.yemen a{font-size:14px;color:#FFFF00;letter-spacing:0;vertical-align:middle}.yemen span{font-size:14px;color:#FFFFFF;vertical-align:middle;margin-$endSide:3px}.shmal{float:$endSide;font-size:13px;margin-top:5px}svg.svg-inline--fa.fa-exclamation-triangle.fa-w-18{width:200px;margin:0 auto 0;display:block;height:200px;color:var(--minColor)}
/* post-share */
.n-line{width:19px;height:19px;fill:#fff;margin:0 3px}
.shC .n-line{width:22px;height:22px}
.pShc{display:flex;align-items:center;flex-wrap:wrap;position:relative;width:calc(100% + 18px);font-size:13px}
.pShc::before{content:attr(data-text);margin-left:10px;flex-shrink:0;color:var(--txtColor);font-size:14px}
.pShc .c::after{content:attr(aria-label);margin:0 3px}
.pShc >*{cursor:pointer;margin:0 5px;display:flex;align-items:center;color:inherit;padding:8px 12px;border-radius:5px;background:rgba(0,0,0,5%)}
.sharemore:hover{background:rgba(0,0,0,8%)}
.pShc .tw{background:#1DA1F2}
.pShc .c{color:#fffdfc}
.pShc .wa{background:#128C7E}
.pShc .fb{background:#1778F2}
.fixi:checked ~ .fixL{opacity:1;visibility:visible}
.fixL{display:flex;align-items:center;position:fixed;left:0;right:0;bottom:0;z-index:20;transition:all .1s linear;width:100%;height:100%;opacity:0;visibility:hidden}
.sharemore svg{fill:var(--txtColor)}
.fixLi{width:100%;max-width:520px;max-height:calc(100% - 60px);border-radius:5px;transition:inherit;z-index:3;display:flex;overflow:hidden;position:relative;margin:0 auto;box-shadow:0 5px 30px 0 rgb(0 0 0 / 5%)}
.fixLs{padding:60px 20px 20px;overflow-x:hidden;width:100%;background:var(--MinBgColor)}
.shL,.fixH{color:var(--txtColor)}
.fixH{display:flex;background:inherit;position:absolute;top:0;left:0;right:0;padding:0 10px;z-index:2}
.fixT::before{content:attr(data-text);flex-grow:1;padding:16px 10px;font-size:90%;opacity:.7}
.fixH .cl{padding:0 10px;display:flex;align-items:center;justify-content:flex-end;position:relative;flex-shrink:0;min-width:40px;cursor:pointer}
.fCls.sharebg{cursor:pointer}
.fixT .c::before{content:attr(aria-label);font-size:11px;margin:0 8px;opacity:.6}
.fixH .c::after{content:'\2715';line-height:18px;font-size:14px}
.shL{position:relative;width:calc(100% + 20px);left:-10px;right:-10px;display:flex;flex-wrap:wrap;justify-content:center}
.shL >*{margin:0 10px 20px;text-align:center}
.shL a{display:flex;align-items:center;justify-content:center;flex-wrap:wrap;width:60px;height:60px;color:inherit;margin:0 auto 5px;padding:8px;border-radius:5px;background:#5a5a5a}
.shL >*::after{content:attr(data-text);font-size:90%;opacity:.7;display:block}

.fCls{display:block;position:fixed;top:-50%;left:-50%;right:-50%;bottom:-50%;z-index:1;transition:all .1s linear;background:transparent;opacity:0;visibility:hidden}

#NavC:checked ~ .searchformbox .searchbg {
  visibility: visible;
}

@media screen and (max-width: 640px){
.fixL{align-items:flex-end}
.fixL .fixLi,.fixL .cmBri{border-radius:12px 12px 0 0}
.pShc .c::after{display:none}
}
.post-body iframe{display:block;margin:auto;max-width:100%}
iframe {color-scheme: none;}
.contenarpage{overflow:hidden}
/* new worck */
.loadMore{display:flex;align-items:center;justify-content:center;font-size:90%;color:#fffdfc;margin:20px 0 0;max-width:100%}
.loadMore div{transition:all .2s linear;cursor:pointer;display:flex;align-items:center;user-select:none;padding:0 20px;background:#bd0000;border-radius:3px;height:35px;line-height:35px}
#loadMoreWait,#loadMoreNomore{background:var(--secColor);color:#989b9f;display:none;user-select:none}
.blog-posts{display:block}
.post .blog-posts{box-shadow:0 2px 6px 0 rgb(9 32 76 / 4%);border-radius:3px}
/* blog-pager2 */
.topic-nav{display:flex;align-items:center;justify-content:center}div#blog-pager{display:flex;align-items:center;justify-content:center;overflow:hidden;clear:both;margin:15px 0 0;padding:15px 0 0;border-top:1px solid var(--Borderes3)}.blog-pager{height:36px;width:40px;display:flex;align-items:center;justify-content:center;overflow:hidden;border-radius:3px;margin:0 2px;color:#fff;background:var(--minColor)}.blog-pager i.icon{font-size:14px;text-align:center;line-height:36px}.homelink i.icon{font-size:16px}
/* Pagecontactus */
div#ContactForm200{display:none}div#Pagecontactus .widget{border:0!important;padding:0;box-shadow:none;margin:0 0;min-height:385px;display:block}div#Pagecontactus{min-height:385px}div#Pagecontactus .widget p{margin:0}
/* Hovers */


.post-tags a:hover,
.Lapel-Link:hover,
.BlogSearch input[type="submit"]:hover,
.cloud-label-widget-content .label-name:hover,
.list-label-widget-content li:hover .label-count,
.ContactForm input[type="button"]:hover,
.moreLink:hover,.caregory-div a:hover{color: var(--whiteColor);background: var(--minColor);}

tbody,table{width:100%;max-width:100%}body.dark-mode input,body.dark-mode textarea{color:#fff}body.dark-mode .ContactForm textarea[name="email-message"]::placeholder,body.dark-mode .ContactForm input[type="text"]::placeholder{color:#fff}
.dark-mode g.d1{display:none}
.dark-mode g.d2{display:block}

/*=================
responsev [not completed]
===================*/

@media screen and (min-width: 1024px){
.fotecol {width: 55%;display: flex;}
}

@media screen and (max-width:992px){
#sidepar-wid{width:250px}.r-r{width:calc((100% - 255px - 15px) / 1)}
.mid-top-footer{flex-wrap:wrap}.footer-col{width:50%}
}
@media screen and (max-width:860px){
.ReadPage-popup-cont {margin: 0;height: 100%;padding-bottom: 50px;}
.bocker {display: block;}
.r-r, #sidepar-wid {transform: none !important;float: none;width: 100%!important;margin: 0;display: block;}
}
@media screen and (max-width:720px){
span.modal-close{$endSide:5px;top:-15px}
.bottom-footer{box-shadow:none}
.bottom-footer .yemen{min-height:auto;display:block!important;float:none;text-align:center;margin-bottom:10px}
.yemen a[title="SeoPlus Template"]{display:inline-block!important}
.bottom-footer .shmal{float:none;margin-top:0;margin:0 auto;text-align:center}
.bottom-footer .shmal .social-static.social{flex-wrap:wrap;display:flex;overflow:hidden;vertical-align:middle;align-items:flex-start;justify-content:center}
.bottom-footer .shmal .social-static.social li{margin-bottom:5px}
.metapost{width:calc(100% - 33px)}
}
@media screen and (max-width:640px){
.commentsection .headline:before,.commentsection .headline .title:after{display:none}
.headline,.Followers .title{font-size:17px}
.metapost{justify-content:flex-start;flex-direction:column;align-items:flex-start}


@media (max-width: 767px) {
.post-body {font-size: 16px;}
}

@media screen and (max-width: 767px) {
  #tocList li {
    font-size: 15px;
 }
}


@media only screen and (max-width: 767px) {
  .post-body h2 {
    font-size: 25px;
  }

  .post-body h3:not(.rnav-title) {
    font-size: 20px;
  }
}


.site .widget,.post .blog-posts { border-right: 0 !important; border-left: 0 !important; }
.comment-content iframe {height: 200px;}
.comment-content img{height: auto;}
.textst{font-size:35px}span.datetime.com-date{float:none!important;display:block}
.search-submit2{$endSide:-10px}
.footer-col{width:100%}
#item-comments .headline{flex-direction:column}
#item-comments .headline .title{margin-bottom:5px}
.commentsShow{display:flex;align-items:center;justify-content:center;text-align:center}
}
/* New Edit's */
.PostByCatRandom{line-height:initial!important}
.PostByCatRandom .rnav-title{margin:0!important}
.PostByCatRandom{margin:30px 0 15px;padding:15px;display:none;border:2px solid var(--Borderes);border-radius:3px;position:relative}
.PostRandomCont{margin-top:15px}
.PostRandomTitle{background:var(--MinBgColor);padding:0 10px;display:block;position:absolute;top:-20px}
.PostRandomTitle .title{background:var(--minColor);font-size:15px;color:var(--whiteColor);display:inline-block;padding:0 20px;flex-shrink:0;border-radius:3px;height:35px;line-height:35px}
.potg .Sp-slide .Posts-byCategory,.potg .Sp-slide2 .Posts-byCategory,.potg .Sp-slide3 .Posts-byCategory,,.potg .Sp-slide4 .Posts-byCategory,.btg2 .Sp-posts1 .Posts-byCategory,.btg2 .Sp-posts2 .Posts-byCategory,.btg2 .Sp-posts5 .Posts-byCategory,.btg2 .Sp-postsnew .Posts-byCategory{display:none}
.potg .Sp-slide:before,.potg .Sp-slide2:before,.potg .Sp-slide3:before,.potg .Sp-slide4:before,.btg2 .Sp-posts1:before,.btg2 .Sp-posts2:before,.btg2 .Sp-posts5:before,.btg2 .Sp-postsnew:before{content:'\f12a';font-family:'FontAwesome';margin-$endSide:5px}
.potg .Sp-slide:after,.potg .Sp-slide2:after,.potg .Sp-slide3:after,.potg .Sp-slide4:after,.btg2 .Sp-posts1:after,.btg2 .Sp-posts2:after,.btg2 .Sp-posts5:after,.btg2 .Sp-postsnew:after{content:"لأ يمكنك استخدام هذا الشكل في هذا المكان"}
.potg .Sp-slide,.potg .Sp-slide2,.potg .Sp-slide3,.potg .Sp-slide4,.btg2 .Sp-posts1,.btg2 .Sp-posts2,.btg2 .Sp-posts5,.btg2 .Sp-postsnew{display:block;overflow:hidden;font-size:16px;height:50px;padding:0 10px;line-height:50px;text-align:center;color:#721c24;background-color:#f8d7da;border:1px solid #f5c6cb;border-radius:3px}
.moreLink{transition:all 0.2s linear;background:var(--minColor);color:var(--whiteColor)}
.postTags .HTML .headline{opacity:0}
.post-frome-tag .headline{opacity:1!important}
.Img-Holder{background:var(--Borderes)}
.Img-Holder img{opacity:0}
.Img-Loaded img{opacity:1}


.rnav-title a,
.post-title .title {
  position: relative;
  display: inline-block;
  padding-bottom: 7px;
  line-height: 1.6em;
  color: #0b0064;
  transition: text-shadow 0.3s ease-in-out, transform 0.3s ease-in-out;
}

.rnav-title a:hover,
.post-title .title:hover {
  text-shadow: 0 0 5px rgba(11, 0, 100, 0.5), 0 0 20px rgba(11, 0, 100, 0.3); /* تأثير التوهج الزائد */
  transform: scale(1.1); /* تكبير حجم النص عند التمرير فوقه */
}



.rnav-title a:hover,.post-title .title:hover{background-size:100% 1px}
.rnav-title{clear:both;font-size:16px}
.thumb img{transition:all .3s linear;border-radius:0;object-fit:cover;display:block;width:100%;height:100%;position:absolute;top:0;right:0;left:0;bottom:0}
.posts-from{font-style:normal;display:flex;align-items:center;justify-content:center;min-height:410px;flex-direction:column}
.posts-from[data-type="Sp-shreet"]{min-height:inherit!important}
.posts-from[data-type="Sp-shreet"]:before{display:none}
.posts .Date svg{display:inline-block;width:10px;height:10px;vertical-align:middle;margin-left:5px;fill:var(--SanColor)}
.posts .Date{display:block;position:relative}
.posts .Date a{color:var(--SanColor);display:inline-block;vertical-align:middle;font-size:12px;font-family:sans-serif!important}
.posts .author{display:block;font-size:15px}
.postcat{position:absolute;top:10px;right:10px;display:inline-block;background:var(--minColor);color:#fff;padding:0 10px;font-size:12px;font-family:sans-serif!important;transition:.3s;z-index:2;border-radius:2px;height:25px;line-height:25px}
.postcat.catnum0{background:#95281C}
.postcat.catnum1{background:#1B5A84}
.postcat.catnum2{background:#2C3E50}
.postcat.catnum3{background:#1A5D50}
.postcat.catnum4{background:#0A3D62}
.postcat.catnum5{background:#A41138}
.postcat.catnum6{background:#0C2461}
.postcat.catnum7{background:#850021}
.postcat.catnum8{background:#04626A}
.postcat.catnum9{background:#3C40C6}

.thumb {
  position: relative;
  display: inline-block;
  overflow: hidden;
  transition: transform 0.3s ease-in-out;
box-shadow: 0 0 18px #0d01e5;
}

.thumb img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease-in-out;
}

.thumb:hover {
  transform: scale(1.1); /* تكبير حجم الصورة عند التمرير فوقها */
}

.thumb:hover img {
  transform: scale(0.9); /* تكبير حجم الصورة عند التمرير فوقها */
}

.lapel .posts:hover .thumb:after,.post .posts:hover > .thumb:after,.item-thumbnail:hover{opacity:1}.Sp-posts4 .Short_content,.Sp-posts3 .Short_content,.Sp-posts4 .posts:not(.postnum0) .thumb .postcat,.Sp-posts3 .postcat,.Sp-posts3.noImg .thumb,.Sp-postsnew0.noImg .thumb,.Sp-3colList.noImg .thumb,.Sp-postsnew.noImg .thumb,.Sp-posts1 .Short_content,.Sp-3colList .posts .postcat,.moreLink,.Short_content,.Sp-shreet .Short_content,.Sp-slide3 .posts:not(.postnum0) .cont .Short_content,.Sp-slide3 .posts:not(.postnum0):not(.postnum1):not(.postnum2) .items a.author,.Sp-slide4 .posts:not(.postnum0) .cont .Short_content,.Sp-slide2 .posts:not(.postnum0) .Short_content,.Sp-posts5 .posts:not(.postnum0) .Short_content,.Sp-posts5 .posts:not(.postnum0) .postcat,.posts .items,
.block-side,
.Sp-shreet .posts .Date, .Sp-shreet .thumb .Noimger,
.SiteInfo:empty,
.modal-body.post-body .redirectSkin.blog-admin,
.readMode .PostByCatRandom, .readMode div#tocDiv,.readMode li.tag-link,
.dark-mode g.d1,
.Sp-posts6 .thumb,
.PopularPosts .Noimg a.item-thumbnail.thumb,
.Sp-posts4.noImg .posts .thumb,
aside .post-frome-tag .headline .Lapel-Link,footer .post-frome-tag .headline .Lapel-Link,
.page .reaction-buttons,
.LinkList .social li a:before
{display:none!important}

.Sp-shreet .rnav-title a:hover,.Sp-posts4 .posts:not(.postnum0) .rnav-title a:hover,.Sp-posts1 .rnav-title a:hover,.Sp-posts3 .rnav-title a:hover,.Sp-posts6 .rnav-title a:hover,.Sp-postsnew .posts .rnav-title a:hover,.Sp-posts5 .posts .rnav-title a:hover,.Sp-3colList .rnav-title a:hover,.list-label-widget-content ul li a:hover,.PopularPosts h3.post-title .title:hover,.FeaturedPost .post-title .title:hover,.posts .Date:hover a,.Sp-postsnew0 .posts .rnav-title a:hover,.posts .Date:hover:before{color:var(--hoverColor)!important},.Sp-3colList .posts:nth-last-child(-n+3),.Sp-posts4 .posts:last-of-type,.Sp-posts6 .posts:last-of-type,.PopularPosts article.post:last-of-type,aside .LinkList ul li:last-of-type,footer .LinkList ul li:last-of-type,aside .PageList ul li:last-of-type,footer .PageList ul li:last-of-type,.Sp-postsnew0 .posts:last-of-type,.list-label-widget-content ul li:last-of-type{padding-bottom:0!important;margin-bottom:0!important;border-bottom:0!important}

/* shreet a5bar */
.Sp-shreet .Posts-byCategory{display:block;position:relative}
.Sp-shreet{transition:all 0.3s linear}
.ShreetTitle{color:var(--whiteColor);flex-shrink:0;padding:0 20px;background:var(--minColor);border-radius:3px;font-size:15px;height:35px;line-height:35px;max-width:130px}
.ShreetTitle svg{width:16px;height:16px;fill:var(--whiteColor);margin-left:8px;display:inline-block;vertical-align:middle}
#shreeta5bar .widget-content{height:40px;overflow:hidden;width:calc(100% - 160px);flex-shrink:0}
#shreeta5bar .widget{display:flex;border:1px solid transparent;box-shadow:0 2px 6px 0 rgb(9 32 76 / 4%);padding:10px;align-items:center}
#shreeta5bar .widget-content{height:40px;overflow:hidden}
.Sp-shreet .posts{padding-right:20px;height:40px;display:flex;align-items:center}
.Sp-shreet .rnav-title a{display:block;font-size:15px;overflow:hidden;width:100%;background-size:0!important;white-space:nowrap;padding:0!important;line-height:40px;text-overflow:ellipsis}
.Sp-shreet .Posts-byCategory .cont{display:block;position:relative;overflow:hidden}
.Sp-shreet .thumb{display:none}
/* post posts1 */
.Sp-posts1 .Posts-byCategory,.Sp-posts2 .Posts-byCategory,.Sp-postsnew .Posts-byCategory{display:grid;grid-gap:27px}
.Sp-posts2 .posts{position:relative}
.fullwide .Sp-postsnew .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
.potg .Sp-postsnew .Posts-byCategory{grid-template-columns:repeat(2,1fr)}
.fullwide .Sp-posts1 .Posts-byCategory{grid-template-columns:repeat(4,1fr)}
.potg .Sp-posts1 .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
.Sp-posts2 .Posts-byCategory{grid-template-columns:repeat(3,1fr);gap:var(--Gap)}
.Sp-posts1 a.thumb,.Sp-posts8 a.thumb{margin:0;width:100%!important;padding-top:68.17%;position:relative}
.Sp-slide .posts .thumb:before,.Sp-slide2 .posts .thumb:before,.Sp-slide3 .posts .thumb:before,.Sp-slide4 .posts .thumb:before,.Sp-posts4 .postnum0 .thumb:before,.Sp-posts7 .thumb:before{content:"";position:absolute;z-index:1;$endSide:0;$startSide:0;bottom:0;height:65%;transition:opacity 0.2s;background-image:linear-gradient(to bottom,transparent,rgba(0,0,0,0.75))}
.Sp-posts8 .Posts-byCategory{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;row-gap:15px}
.fullwide .Sp-posts8 .Posts-byCategory{grid-template-columns:repeat(6,1fr)}
.Sp-posts8 .rnav-title{font-size:15px}
.potg .PostRandomCont.Sp-posts8 .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
/* posts7 */
.Sp-posts7 .Posts-byCategory{display:grid;grid-template-columns:repeat(3,1fr);gap:var(--Gap)}
.fullwide .Sp-posts7 .Posts-byCategory{grid-template-columns:repeat(4,1fr)}
.Sp-posts7 .posts .thumb{height:270px;display:block;margin:0;width:100%}
.Sp-posts7 .posts{position:relative}
.Sp-posts7 .posts .cont{position:absolute;bottom:0;$startSide:0;z-index:1;padding:15px;display:block;width:100%}
.Sp-posts7 .posts .rnav-title a{color:#fff;font-size:18px;line-height:initial!important;height:inherit;margin:0;overflow:hidden}
.Sp-postsnew0 .Posts-byCategory{display:grid;gap:15px;grid-template-columns:1fr}
.Sp-postsnew0 .posts{display:flex}
.Sp-postsnew0 .posts .thumb{width:300px;height:170px;flex-shrink:0}
.Sp-postsnew0 .posts .cont{width:calc((100% - 315px) / 1);flex-shrink:0}
.Sp-postsnew0 .posts .rnav-title a{font-size:21px}
.Sp-postsnew0 .posts .Short_content{color:var(--SanColor);font-size:13px;font-family:sans-serif!important;line-height:21px;margin-top:5px;overflow:hidden;height:63px;display:block!important}
.Sp-postsnew0.noImg .posts .cont{width:100%}
.Sp-postsnew .posts .thumb{width:100%;padding-top:56.25%;margin:0;margin-bottom:5px}
.Sp-postsnew .posts .cont{width:100%}
.Sp-postsnew .posts .rnav-title{height:inherit;clear:both;}
.Sp-postsnew .posts .rnav-title a{font-size:19px;overflow:hidden}
.Sp-postsnew .posts .Short_content{color:var(--SanColor);font-size:13px;font-family:sans-serif!important;line-height:21px;margin-top:-9px;overflow:hidden;display:block!important;height:63px}
.Sp-postsnew .posts .moreLink,.Sp-postsnew0 .posts .moreLink{display:inline-block!important;position:relative;font-size:15px;padding:0 76px;border-radius:20px;margin-top:0px;height:30px;line-height:30px;background: #000000;font-weight: bold;}

/* post slide 2 */
.Sp-slide .Posts-byCategory,.Sp-slide2 .Posts-byCategory,.Sp-slide3 .Posts-byCategory,.Sp-slide4 .Posts-byCategory{display:grid;grid-template-columns:repeat(4,1fr);gap:var(--Gap)}
.Sp-slide4 .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
.Sp-slide .posts,.Sp-slide2 .posts,.Sp-slide3 .posts,.Sp-slide4 .posts{position:relative;overflow:hidden;padding-top:68.17%}
.Sp-slide4 .posts{padding-top:56.25%}
.Sp-slide2 .postnum0,.Sp-slide3 .postnum0,.Sp-slide4 .postnum0{grid-column:span 2;grid-row:span 2}
.Sp-slide .postnum0{grid-column:2/4;grid-row:1/3}
.Sp-slide3 .postnum1{padding-top:42%;grid-column:span 2}
.Sp-slide3 .posts .thumb,.Sp-slide4 .posts .thumb,.Sp-slide .thumb,.Sp-slide2 .thumb{position:absolute;top:0;right:0;width:100%;margin:0;height:100%}
.Sp-slide3 .posts .thumb img,.Sp-slide4 .posts .thumb img,.Sp-slide .thumb img,.Sp-slide2 .thumb img{position:unset}
.Sp-slide .posts .cont,.Sp-slide2 .posts .cont,.Sp-slide3 .posts .cont,.Sp-slide4 .posts .cont{transition:all 0.1s linear;position:absolute;bottom:0;$startSide:0;z-index:1;padding:20px 20px 15px}
.Sp-slide .posts .rnav-title,.Sp-slide2 .posts .rnav-title,.Sp-slide3 .posts .rnav-title,.Sp-slide4 .posts .rnav-title{font-size:inherit;height:auto}
.Sp-slide .posts .rnav-title a,.Sp-slide2 .posts .rnav-title a,.Sp-slide3 .posts .rnav-title a,.Sp-slide4 .posts .rnav-title a{color:#fff;line-height:inherit;font-size:18px}
.Sp-slide .postnum0 .rnav-title a,.Sp-slide2 .postnum0 .rnav-title a,.Sp-slide3 .postnum0 .rnav-title a,.Sp-slide4 .postnum0 .rnav-title a{font-size:30px}
.Sp-slide .posts .Date a,.Sp-slide2 .posts .Date a,.Sp-slide3 .posts .Date a,.Sp-slide4 .posts .Date a,.Sp-posts2 .posts .Date a,.Sp-posts4 .posts.postnum0 .Date a,.Sp-posts7 .posts .Date a{color:#e4e4e4!important}
.Sp-slide .posts .Date svg,.Sp-slide2 .posts .Date svg,.Sp-slide3 .posts .Date svg,.Sp-slide4 .posts .Date svg,.Sp-posts2 .posts .Date svg,.Sp-posts4 .posts.postnum0 .Date svg,.Sp-posts7 .posts .Date svg{fill:#e4e4e4!important}
.Sp-slide .postnum0 .Short_content,.Sp-slide2 .postnum0 .Short_content,.Sp-slide3 .postnum0 .Short_content,.Sp-slide4 .postnum0 .Short_content{line-height:18px;font-size:13px;font-family:sans-serif!important;color:#eaeaea;max-height:100px;overflow:hidden;display:block!important;margin-top:5px}
.Sp-slide .posts:hover .cont,.Sp-slide2 .posts:hover .cont,.Sp-slide3 .posts:hover .cont,.Sp-slide4 .posts:hover .cont{bottom:10px}

/* post posts2 */
.Sp-posts2 .posts a.thumb{margin:0;width:100%!important;padding-top:68.17%;position:relative}
.fullwide .Sp-posts2 .posts .thumb{padding-top:56.25%}
.Sp-posts2 .cont{position:absolute;bottom:0;$startSide:0;z-index:1;padding:15px;display:block;width:100%}
.Sp-posts2 .thumb:before{content:"";position:absolute;z-index:1;$endSide:0;$startSide:0;bottom:0;height:65%;transition:opacity 0.2s;background-image:linear-gradient(to bottom,transparent,rgba(0,0,0,0.75))}
.Sp-posts2 .cont .rnav-title a{color:#fff!important;font-size:18px}
.Sp-posts2  .rnav-title{height:inherit}
.Sp-posts2 .thumb:after{content:"\025B6";position:absolute;top:10px;bottom:auto;$startSide:auto;$endSide:10px;width:38px;height:27px;background-color:rgba(0,0,0,0.5);font-family:sans-serif;font-size:15px;color:#fff;font-weight:900;display:flex;align-items:center;justify-content:center;z-index:5;transform:translate(0);box-sizing:border-box;padding:0 0 0 1px;margin:0;box-shadow:0 1px 3px 0 rgb(0 0 0 / 10%);transition:background .17s linear;opacity:1;border-radius:5px}
.Sp-posts2 .thumb:hover:after{background:#f50000;color:#fff}

/* post posts4 and posts3 and 3colList and6  */
.Sp-posts4 .posts.postnum0{position:relative;overflow:hidden}
.Sp-posts4 .posts.postnum0 .cont{position:absolute;bottom:0;$startSide:0;z-index:1;padding:15px;display:block;width:100%}
.Sp-posts4 .posts.postnum0 .rnav-title a{color:#fff;font-size:18px}
.Sp-posts3 .Posts-byCategory,.Sp-posts4 .Posts-byCategory,.Sp-3colList .Posts-byCategory,.PopularPosts .ImgShow{gap:15px;display:grid;grid-template-columns:1fr}
.Sp-3colList .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
.Sp-posts4 .posts.postnum0 .thumb{width:100%;padding-top:56.25%;margin:0!important}
.Sp-posts3 .Posts-byCategory .posts,.Sp-posts4 .posts:not(.postnum0),.Sp-posts5 .posts:not(.postnum0),.Sp-3colList .posts,.PopularPosts .ImgShow .post{display:flex}
.Sp-posts4 .posts:not(.postnum0) .cont,.Sp-posts3 .cont,.Sp-3colList .cont,.PopularPosts h3.post-title,.Sp-posts5 .posts:not(.postnum0) .cont{width:calc(100% - 125px);flex-shrink:0}
.Sp-posts3 .posts .thumb,.Sp-posts4 .thumb,.Sp-3colList .thumb,.PopularPosts a.item-thumbnail.thumb,.Sp-posts5 .posts:not(.postnum0) .thumb{width:110px;height:75px;flex-shrink:0}
.Sp-posts3 .posts:not(.postnum0) .rnav-title a,.Sp-posts4 .rnav-title a,.Sp-posts6 .rnav-title a,.Sp-3colList .rnav-title a,.PopularPosts h3.post-title .title{font-size:14px}
.PopularPosts .post-title .title{background-size:0!important;display:block;max-height:4.9em;overflow:hidden}
.3colList.noImg .cont{width:100%}
.Sp-posts6 .cont,.PopularPosts .Noimg .posts.post-title{width:100%}
.caregory-div a{background:var(--minColor);padding:4px 20px;display:table;border-radius:3px;font-size:15px;line-height:1.6em;color:var(--whiteColor)}
.ArchivePage{min-height:450px;display:block}
.Sp-posts6.archive{margin-bottom:15px}
.Sp-posts6.archive .Date{line-height:1.5em}
.Sp-posts6 .Posts-byCategory:before,.PopularPosts .Noimg:before{content:"";position:absolute;$startSide:0;top:0;width:2px;height:100%;background:rgba(0,0,0,0.3)}
.Sp-posts6 .Posts-byCategory,.PopularPosts .Noimg{overflow:unset;padding-$startSide:15px;margin-$startSide:10px;position:relative}
.Sp-posts6 .Date:after,.PopularPosts .Noimg .Date:after{content:"";width:12px;height:12px;background:#e6e6e6;border:1px solid rgba(255,255,255,0.8);position:absolute;display:inline-block;vertical-align:middle;border-radius:3px;transform:translateZ(0);transition-duration:0.3s;$startSide:-21px;border-color:rgba(0,0,0,0.3);top:5px}
.Sp-posts6 .posts:hover .Date:after,.PopularPosts .Noimg  article.post:hover .Date:after{background:#3560ab;transform:scale(1.2)}
.Sp-posts6 .posts,.PopularPosts .Noimg article.post{overflow:unset;margin-bottom:15px}
.Sp-posts4.noImg .posts .cont,.Sp-posts3.noImg .posts .cont{width:100%;position:relative;padding:0}
.Sp-posts4.noImg .postnum0 .Date a{color:var(--SanColor)!important}
.Sp-posts4.noImg .posts.postnum0 .rnav-title a{color:var(--TitColor)}
.Sp-posts4.noImg .posts.postnum0{padding:15px;background:var(--secColor);border-radius:5px;border:1px solid var(--Borderes)}
.Sp-posts4.noImg .postnum0 .Date svg{display:inline-block!important}

/* post posts5 */
.Sp-posts5 .Posts-byCategory{display:grid;grid-template-columns:repeat(2,1fr);gap:15px}
.Sp-posts5 .posts.postnum0{grid-row:span 4}
.Sp-posts5 .posts.postnum0 a.thumb{width:100%;padding-top:56.25%;margin:0;float:none}
.Sp-posts5 .cont{overflow:hidden;display:block;clear:both}
.Sp-posts5 .posts.postnum0 .rnav-title a{font-size:21px}
.Sp-posts5 .posts.postnum0 .Short_content{color:var(--SanColor);line-height:21px;margin:5px 0 0;font-size:13px;display:block!important;font-family:sans-serif!important;max-height:42px;overflow:hidden}
.Sp-posts5 .posts:not(.postnum0) .rnav-title a{font-size:14px}


/* respons2 */
@media screen and (max-width:992px){

.Sp-slide .posts .rnav-title a,.Sp-slide2 .posts .rnav-title a,.Sp-slide3 .posts .rnav-title a,.Sp-slide4 .posts .rnav-title a{font-size:16px}
.Sp-slide .postnum0 .Short_content,.Sp-slide2 .postnum0 .Short_content,.Sp-slide3 .postnum0 .Short_content,.Sp-slide4 .postnum0 .Short_content{font-size:12px}
.Sp-slide .postnum0 .rnav-title a,.Sp-slide2 .postnum0 .rnav-title a,.Sp-slide3 .postnum0 .rnav-title a,.Sp-slide4 .postnum0 .rnav-title a{font-size:20px}
.Sp-slide .postnum0 .Short_content,.Sp-slide2 .postnum0 .Short_content,.Sp-slide3 .postnum0 .Short_content,.Sp-slide4 .postnum0 .Short_content{max-height:35px}
.Treelists,.towcol{grid-template-columns:1fr}

}
@media screen and (max-width:850px){

.Sp-posts8 .Posts-byCategory{grid-template-columns:repeat(3,1fr)!important}
.Sp-posts8 .postcat{display:none}
.Sp-3colList .Posts-byCategory{grid-template-columns:repeat(2,1fr)}
.fullwide .Sp-posts7 .Posts-byCategory{grid-template-columns:repeat(3,1fr)}
.Sp-slide .Posts-byCategory,.Sp-slide2 .Posts-byCategory,.Sp-slide3 .Posts-byCategory,.Sp-slide4 .Posts-byCategory{grid-template-columns:repeat(2,1fr)}
.Sp-slide .postnum0{grid-column:span 2;grid-row:span 2;padding-top:56.25%}
.Sp-slide4 .posts:not(.postnum0){padding-top:68.17%}
.Sp-slide1 .postnum0,.Sp-slide2 .postnum0,.Sp-slide3 .postnum0{padding-top:56.25%}
.Sp-slide3 .postnum1{padding-top:45%}
.Sp-posts2 .Posts-byCategory{grid-template-columns:repeat(2,1fr)}
.Sp-posts2 .posts a.thumb{padding-top:68.17%}

}

@media screen and (max-width:640px){
.ShreetTitle svg{width:14px;height:14px}
.ShreetTitle{padding:0 15px;font-size:14px}
#shreeta5bar .widget-content{width:calc(100% - 120px)}
.Sp-posts5 .Posts-byCategory,.Sp-postsnew .Posts-byCategory,.Sp-posts2 .Posts-byCategory,.Sp-3colList .Posts-byCategory{grid-template-columns:1fr!important}
.Sp-slide .posts:not(.postnum0),.Sp-slide2 .posts:not(.postnum0),.Sp-slide3 .posts:not(.postnum0):not(.postnum1),.Sp-slide4 .posts:not(.postnum0){padding-top:80%}
.Sp-postsnew0 .posts{flex-direction:column}
.Sp-postsnew0 .posts .thumb,.Sp-posts2 .posts a.thumb{width:100%;padding-top:56.25%;margin-left:0}
.Sp-postsnew0 .posts .cont{width:100%}
.Sp-posts1 .Posts-byCategory{grid-template-columns:repeat(2,1fr)!important;gap:10px;row-gap:15px}
.Sp-posts7 .Posts-byCategory{grid-template-columns:repeat(2,1fr)!important}
.Sp-posts7 .posts .thumb{height:230px}


}
@media screen and (max-width:480px){
.Sp-slide .posts .rnav-title a,.Sp-slide2 .posts .rnav-title a,.Sp-slide3 .posts .rnav-title a,.Sp-slide4 .posts .rnav-title a{font-size:14px}
.Sp-slide .postnum0 .rnav-title a,.Sp-slide2 .postnum0 .rnav-title a,.Sp-slide3 .postnum0 .rnav-title a,.Sp-slide4 .postnum0 .rnav-title a{font-size:18px}
.postcat{padding:0 5px;font-size:11px;line-height:22px;height:22px}

.Sp-posts8 .thumb{height:75px;padding-top:0!important}
.Sp-posts8 .posts .Date svg{width:8px;height:8px}
.Sp-posts8 .posts .Date a{font-size:10px}
.Sp-posts8 .posts .rnav-title{font-size:13px}
}

.post-body h2:not(.rnav-title) {border-radius: 3px;background: var(--minColor); display: block; padding: 13px 20px; margin: 5px 0 10px; color: var(--whiteColor);}details {
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 10px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.1);
}

summary {
  font-weight: bold;
  cursor: pointer;
}

.post-body h2:not(.rnav-title) {
background-color: #ffffff;
color: #0000ff;
font-weight: bold;
padding: 10px 15px;
margin: 10px 0;
border: 2px solid #0000ff;
border-radius: 0px;
    box-shadow: 0px 0px 10px #0000ff;
}

.post-body h3:not(.rnav-title) {
background-color: #ffffff;
color: #38761d;
font-weight: bold;
padding: 5px 5px;
margin: 0px 0 0px;
border-radius: 0px;
box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.5);
text-indent: 0px;
display: inline-block;
transform: skew(-0deg);
}

.post-body h4:not(.rnav-title) {
border-right: 12px solid #000000;
border-radius: 50px;
padding: 20px;
font-weight: bold
}

.your-custom-div-class {
display: inline-block;
width: 100%;
background-color: #fff;
color: #0066CC;
font-size: 18px;
text-align: center;
text-decoration: none;
text-transform: uppercase;
border: 4px solid #0066CC;
border-radius: 5px;
box-shadow: 0px 0px 20px rgb(0, 102, 204, 0.5);
position: relative;
overflow: hidden;
}

.your-custom-div-class:before {
content: '';
position: absolute;
top: -5px;
left: -5px;
right: -5px;
bottom: -5px;
border: 4px solid #0066CC;
box-shadow: 0px 0px 20px rgb(0, 102, 204, 0.5);
z-index: -1;
}

.your-custom-div-class:hover {
background-color: #0066CC;
color: #fff;
}

.your-custom-div-class:hover:before {
border-color: #fff;
box-shadow: 0px 0px 30px rgb(0, 102, 204, 0.7);
}

.lines {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 20px; /* تحديد ارتفاع العنصر الأب */
  width: 20px; /* تحديد عرض العنصر الأب */
}

.lines span {
  height: 2px; /* تحديد ارتفاع الخط */
  background-color: #6600ff; /* تحديد لون الخط */
  display: block;
}

.lines .line1 {
  width: 200%;
}

.lines .line2 {
  width: 75%;
}

.lines .line3 {
  width: 200%;
}

.custom-class {
    background-color: #0019ff;
    border: 4px solid #000;
    padding: 10px;
    border-radius: 20px;
    margin-bottom: -1px;
    width: 243px;
    color: #ffffff; /* لون النص */

}

.fotecol {
     float: right;
    font-family: sans-serif;
    color: #fff944;
    line-height: 1.9em;
    margin-bottom: 10	px;
}

]]></b:skin>
      <b:if cond='data:skin.vars.BlogFonts'>
        <b:if cond='data:skin.vars.BlogFonts == &quot;1px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l8KiHrRpiYlJ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l8KiHrFpiQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l4qkHrRpiYlJ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l4qkHrFpiQ.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'Tajawal';font-style:normal;font-weight:500;font-display:swap;src:local('Tajawal Medium'),local('Tajawal-Medium'),url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l8KiHrRpiYlJ.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Tajawal';font-style:normal;font-weight:500;font-display:swap;src:local('Tajawal Medium'),local('Tajawal-Medium'),url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l8KiHrFpiQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:'Tajawal';font-style:normal;font-weight:700;font-display:swap;src:local('Tajawal Bold'),local('Tajawal-Bold'),url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l4qkHrRpiYlJ.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Tajawal';font-style:normal;font-weight:700;font-display:swap;src:local('Tajawal Bold'),local('Tajawal-Bold'),url(https://fonts.gstatic.com/s/tajawal/v3/Iurf6YBj_oCad4k1l4qkHrFpiQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'Tajawal',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'Tajawal',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'Tajawal',sans-serif!important}nav.nav-par ul li a{font-family:'Tajawal',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;2px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIkTpu0xg.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIvTpu0xg.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIhTps.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'Cairo';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIkTpu0xg.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Cairo';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIvTpu0xg.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:'Cairo';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/cairo/v10/SLXGc1nY6HkvalIhTps.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'Cairo',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'Cairo',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'Cairo',sans-serif!important}nav.nav-par ul li a{font-family:'Cairo',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;3px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjLj9ytf.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjnj9ytf.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjfj9w.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'Changa';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjLj9ytf.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Changa';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjnj9ytf.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:'Changa';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/changa/v11/2-c79JNi2YuVOUcOarRPgnNGooxCZ62xcjfj9w.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'Changa',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'Changa',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'Changa',sans-serif!important}nav.nav-par ul li a{font-family:'Changa',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;4px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6MoiAAhLz.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6MomAAhLz.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6Mo2AAg.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'El Messiri';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6MoiAAhLz.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'El Messiri';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6MomAAhLz.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:'El Messiri';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/elmessiri/v9/K2F0fZBRmr9vQ1pHEey6Mo2AAg.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'El Messiri',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'El Messiri',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'El Messiri',sans-serif!important}nav.nav-par ul li a{font-family:'El Messiri',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;5px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/almarai/v4/tsstApxBaigK_hnnQ1iFo0C3.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/almarai/v4/tssoApxBaigK_hnnS-agtnqWo572.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'Almarai';font-style:normal;font-weight:400;font-display:swap;src:local('Almarai'),local('Almarai-Regular'),url(https://fonts.gstatic.com/s/almarai/v4/tsstApxBaigK_hnnQ1iFo0C3.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Almarai';font-style:normal;font-weight:700;font-display:swap;src:local('Almarai Bold'),local('Almarai-Bold'),url(https://fonts.gstatic.com/s/almarai/v4/tssoApxBaigK_hnnS-agtnqWo572.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'Almarai',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'Almarai',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'Almarai',sans-serif!important}nav.nav-par ul li a{font-family:'Almarai',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;6px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ys43PWrfQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ysw3PWrfQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ysz3PWrfQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ys93PU.woff2' rel='preload'/><style>/*<![CDATA[*/@font-face{font-family:'IBM Plex Sans Arabic';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ys43PWrfQ.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'IBM Plex Sans Arabic';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ysw3PWrfQ.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:'IBM Plex Sans Arabic';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ysz3PWrfQ.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:'IBM Plex Sans Arabic';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/ibmplexsansarabic/v7/Qw3CZRtWPQCuHme67tEYUIx3Kh0PHR9N6Ys93PU.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'IBM Plex Sans Arabic',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'IBM Plex Sans Arabic',sans-serif!important}.post-amp .entry-title.topic-title{font-family:'IBM Plex Sans Arabic',sans-serif!important}nav.nav-par ul li a{font-family:'IBM Plex Sans Arabic',sans-serif!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;7px&quot;'><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpP6JYtZfQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpPxJYtZfQ.woff2' rel='preload'/><link as='font' crossorigin='anonymous' href='https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpP_JYs.woff2' rel='preload'/>
          <style>/*<![CDATA[*/@font-face{font-family:'Baloo Bhaijaan 2';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpP6JYtZfQ.woff2) format('woff2');unicode-range:U+0600-06FF,U+200C-200E,U+2010-2011,U+204F,U+2E41,U+FB50-FDFF,U+FE80-FEFC}@font-face{font-family:'Baloo Bhaijaan 2';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpPxJYtZfQ.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:'Baloo Bhaijaan 2';font-style:normal;font-weight:400;font-display:swap;src:url(https://fonts.gstatic.com/s/baloobhaijaan2/v12/zYXwKUwuEqdVGqM8tPDdAA_Y-_bMKo1EhQd2tWxo8TyRSpP_JYs.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'Baloo Bhaijaan 2',cursive}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'Baloo Bhaijaan 2',cursive!important}.post-amp .entry-title.topic-title{font-family:'Baloo Bhaijaan 2',cursive!important}nav.nav-par ul li a{font-family:'Baloo Bhaijaan 2',cursive!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;8px&quot;'><style>/*<![CDATA[*/body *:not(.fa),.HeaderBOT #menu ul li a{font-family:sans-serif,'Segoe UI'}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:sans-serif,'Segoe UI'!important}.post-amp .entry-title.topic-title{font-family:sans-serif,'Segoe UI'!important}nav.nav-par ul li a{font-family:sans-serif,'Segoe UI'!important}/*]]>*/</style></b:if>
        <b:if cond='data:skin.vars.BlogFonts == &quot;9px&quot;'><style>/*<![CDATA[*/body *:not(.fa),.HeaderBOT #menu ul li a{font-family:'monospace',sans-serif}.post-body h1,.post-body h2,.post-body h3,.post-body h4{font-family:'monospace'!important}.post-amp .entry-title.topic-title{font-family:'monospace'!important}nav.nav-par ul li a{font-family:'monospace'!important}/*]]>*/</style></b:if>
      </b:if>
    </b:if>
    <b:if cond='data:view.isLayoutMode'>
      <!-- Layout Skin -->
      <b:template-skin><![CDATA[
body#layout .rtl{direction:rtl}
body#layout .ltr{direction:ltr}
body#layout .add_widget {border: 3px dashed #dd02ff;}
body#layout div.widget-content.visibility div.layout-title {margin: 22px 40px;}
body#layout .add_widget a {color: #ffeb00;font-size: 21px;line-height: 40px;margin-left: 59px;}
body#layout .clear{height:1px;clear:both;display:block;width:100%}
body#layout .section .widget-content{border-radius:2px;min-height:20px}
body#layout .draggable-widget .widget-wrap3{background:none}
body#layout .section h4{display:none}
body#layout div.layout-title{color:#d8ff00;font-weight:700;font-size:16px}
body#layout .rtl div.layout-title{text-align:right}
body#layout .ltr div.layout-title{text-align:left}
.layout-widget-description{display:none}
body#layout .add-icon,body#layout .layout-widget-state,body#layout .editlink.icon{background-position:center;background-repeat:no-repeat;height:24px;width:24px}
body#layout .widget-content a:hover{background-color:#ccc;color:#000;transition:.4s linear}
body#layout .editlink.icon{font-size:0;line-height:0;position:absolute;right:16px;top:16px}
body#layout .widget-content a{color:#4c4c4c!important;padding:3px 10px;background-color:#e0e0e0;border-radius:5px}
body#layout .locked-widget .widget-content{font-weight:700;text-align:center;background-color: #380b0b;}
.mid-top-footer .footer-col{width:24%;display:inline-block}
.bocker{display:block;clear:both}
aside#sidepar-wid{float:left;width:285px;margin-right:15px}
.bocker .r-r{width:500px;float:right}
.sides{display:inline-block;width:49.5%}
#sitting,#ContactForm200{display:none}
body#layout .Blog .widget-content{height:auto!important}
div#sittings .widget{margin:0 0 1px 1px!important;float:right!important;width:361px!important}
body#layout #menu:before,body#layout #logo:before,body#layout #topsocialL:before,body#layout #pages:before,body#layout #menu:after,body#layout #logo:after,body#layout #topsocialL:after,body#layout #pages:after,body#layout .potg:before,body#layout .potg:after,body#layout footer div.section:after,body#layout footer div.section:before{display:none!important}
body#layout #menu,body#layout #logo,body#layout #topsocialL,body#layout #pages,body#layout .contpotg div.section,body#layout footer div.section{padding:0!important;margin:0!important;border-radius:0!important}
header#sp-header,body#layout .contpotg,footer{background:#fff}
.head-pz div.section{margin:0 0 1px 1px!important;float:right!important;width:49.5%!important}
a.editlink{line-height:2em!important;height:24px;width:24px;position:absolute!important;right:16px!important;top:16px}
body#layout header#sp-header div.section > div{margin-top:0!important}
body#layout .contpotg div.section,body#layout footer div.section{border:0!important}
body#layout div.section:after,header#sp-header:after,body#layout .contpotg:after,body#layout footer:after{content:"";height:2px;width:100%;background:#eee;display:block;position:absolute;top:30px;right:-10px}
body#layout .trelists.section{display:inline-block;width:235px;padding-top:10px!important;border-top:0!important;border-left:0!important;margin:0 -2px!important}
body#layout .trelists.section:after,div#BotPostsc:after{display:none!important}
body#layout div#Postnw4,body#layout div#Postnw5,body#layout div#Postnw6{border-radius:0!important;border-top:1px solid #eee!important;padding-top:60px!important}
.Treelists{position:relative;z-index:1;border:1px solid #eee!important}
body#layout div#Postnw4:after,body#layout div#Postnw5:after,body#layout div#Postnw6:after{display:block!important}
body#layout div#BotPostsc{margin-top:-5px!important;padding-top:15px!important;border-radius:0!important}
body#layout div.widget{border:1px solid #eee}
body#layout .dr_active:before{content:'\افلت هُنا';font-size:30px;padding-top:25px;display:block;font-weight:700}
body#layout .dr_active{height:50px!important;background-color:transparent;border:1px dashed var(--minColor);color:#111;margin-bottom:30px;top:20px;border-radius:2px}
#sittings:before{content:"الإعدادت"!important}
#sp-header:before{content:"القائمة  العلوية"!important}
#TopPost-sc:before,body#layout div#Postnw4:before,.contpotg:before{content:"منطقة  التدوينات  الاضافية"!important}
div#sidepar:before{content:"القائمة  الجانبية"!important}
div#shreeta5bar:before{content:"شريط  الاخبار"!important}
div#Tempnec:before{content:"أخر  المشاركات"!important}
footer:before{content:"زيل  المدونة  (الفوتر)"!important}
#Topa3lan-sc:before{content:"اعلان  للحاسوب  فقط  [pc]"!important}
#Topa3lan-sc2:before{content:"إعلان  للهاتف  فقط  [mopile]"!important}
#lazy:before{content:"تأجيل  الاعلانات"!important}
#AddOns:before{content:"مميزات  المقال  الاضافية"!important}
#PostA3lan:before{content:"اعلانات  المقال"!important}
#PostA3lan2:before{content:"اعلانات  المقال  [للكتاب]"!important}
div#BotPostsc,#Tempnec,.mid-top-footer,div#TopPost-sc,header#sp-header,div#Postcs1,div#Postcs4,div#Postcs8,div#Postcs5,.contpotg,.Treelists,footer{display:block;overflow:unset;clear:both}
body#layout .widget-content{background:#fff}
div#PostA3lan .HTML{width:49%!important;float:right!important;clear:none;margin-left:0.5%!important}
body#layout div.section:before,header#sp-header:before,body#layout .contpotg:before,body#layout footer:before{background:#3560ab}
body#layout div#TopPost-sc{margin-bottom:-5px!important;border-radius:0!important}
body#layout div.section:before,header#sp-header:before,body#layout .contpotg:before,body#layout footer:before{background:var(--minColor);color:#fff;padding:7px 35px;border-radius:5px;position:absolute;top:15px;right:15px;z-index:999;font-family:sans-serif}
body#layout,body#layout *{font-family:sans-serif!important}
body#layout div#Topa3lan-sc2,body#layout div#Topa3lan-sc{width:375px;display:inline-block!important;float:right!important;margin:0 4px!important;padding:0!important;padding-top:60px!important}
header#sp-header,body#layout .contpotg,footer{background:#fff}
body#layout div.section,header#sp-header,.contpotg,footer{background:#1b1756!important;overflow:unset!important;padding:50px 15px 15px!important;border:1px solid rgba(32,33,36,0.07)!important;margin:10px 0 20px!important;position:relative;border-radius:8px!important}
body#layout:before{z-index:99;content:"cot12a";text-align:center;position:absolute;right:10px;top:25px;font-weight:bold;color:#fff;padding:10px 15px;background:#3560ab;border-radius:8px 8px 8px 0}
body#layout,body#layout *{font-family:sans-serif!important}
body#layout{background:#000000!important;min-height:100%!important;direction:rtl!important;width:1130px;display:block!important;position:relative!important;border:0!important;padding:5px 0!important;border-radius:8px;margin:10px auto 10px auto !important;border:1px solid #e5e5e5!important}
.contenarpage{width:800px;margin:20px 300px 20px auto;overflow:hidden!important}
header#sp-header div.section{border:0!important}
.TEMPsittings{right:20px;top:55px;padding:10px;background:#042052;float:right;width:250px;position:absolute;z-index:999;border-radius:8px}
.TEMPsittings .section .editlink.icon,header#sp-header .section .editlink.icon{padding:0!important;top:0!important;right:0!important;width:45px!important;height:45px!important;border-radius:0!important}
body#layout .TEMPsittings .section > div,body#layout header#sp-header .section > div{margin:0!important;border:0!important;box-shadow:none!important;margin-bottom:0!important;border-radius:0!important}
body#layout .TEMPsittings .locked-widget .widget-content,body#layout header#sp-header .locked-widget .widget-content{border-radius:0!important;margin:0!important;border:0!important;padding:10px!important;margin-bottom:5px!important;border-radius:5px!important}
.TEMPsittings .section::before,.TEMPsittings .section::after{display:none!important}
body#layout .TEMPsittings div.section{padding:0!important;margin:0!important;border:0!important;box-shadow:none!important;background:red !important}
.TEMPsittings:before{content:"أعدادات  القالب";font-size:24px;font-family:sans-serif;color:#fff;padding:10px 0;display:block}
body#layout .TEMPsittings div#AddOns:before{display:block!important;content:"أعدادات  أضافية"!important;font-size:24px;font-family:sans-serif;color:#fff;padding:10px 0;display:block;position:relative!important;border-radius:0!important;top:auto;right:auto;left:auto;bottom:auto;border-top:1px solid #2b4e8d;margin-top:10px}
.searchformbox:before{content:"الرأس";font-size:24px;font-family:sans-serif;color:#fff;padding:10px 0;display:block;border-top:1px solid #2b4e8d;margin-top:10px}
body#layout div#Header1 .editlink{font-size:0!important;padding:0!important;top:0!important;right:0!important;width:45px!important;height:45px!important;border-radius:0!important}
body#layout div#Header1 .editlink:before{content:"";background:url(https://www.gstatic.com/images/icons/material/system/1x/mode_edit_grey600_24dp.png);width:23px;height:23px;display:block;margin:0 auto;top:10px;position:relative}
body#layout div#topsocialL,body#layout div#pages,body#layout div#menu,body#layout div#logo{display:block!important;width:375px!important;float:right!important;margin:0 4px!important}
body#layout div#topsocialL .locked-widget .widget-content,body#layout div#pages .locked-widget .widget-content,body#layout div#menu .locked-widget .widget-content,body#layout div#logo .locked-widget .widget-content,body#layout div#Topa3lan-sc2 .locked-widget .widget-content,body#layout div#Topa3lan-sc .locked-widget .widget-content{}
header#sp-header{overflow:hidden!important}
body#layout div#Postnw1,body#layout div#Postnw2,body#layout div#Postnw3{border:1px solid #eee!important;border-radius:0!important}
body#layout .mid-top-footer div.section{width:189px!important}
.contenarpage{padding-right:10px;border-right:3px solid #ff0000}
#BlogSearch2{display:none!important}

    ]]></b:template-skin>
    </b:if>
    <b:defaultmarkups>
      <b:defaultmarkup type='Common'>
        <b:includable id='themeFunctions'><script>/*<![CDATA[*/const _0x114308=_0x2ce4;const _0x1278e4=_0xce5f;(function(_0x5a5296,_0x3bffa0){const _0x1b010a=_0x2ce4;const _0x1c8037=_0xce5f;const _0x4e67a6=_0x5a5296();while(!![]){try{const _0xbdc246=-parseInt(_0x1c8037(0x1b9))/0x1+-parseInt(_0x1b010a(0x10e,'Xhhi'))/0x2*(parseInt(_0x1b010a(0x13b,')tBn'))/0x3)+parseInt(_0x1c8037(0x115))/0x4*(parseInt(_0x1b010a(0x92,'yLNb'))/0x5)+parseInt(_0x1c8037(0x104))/0x6+parseInt(_0x1b010a(0xa6,'XOnF'))/0x7*(-parseInt(_0x1c8037(0x19e))/0x8)+parseInt(_0x1b010a(0x144,'t2(y'))/0x9+parseInt(_0x1c8037(0xab))/0xa*(parseInt(_0x1c8037(0xaf))/0xb);if(_0xbdc246===_0x3bffa0){break;}else{_0x4e67a6['push'](_0x4e67a6['shift']());}}catch(_0x100b88){_0x4e67a6['push'](_0x4e67a6['shift']());}}}(_0x4037,0x1e5dc));function darkMode(){const _0x2fb8f8=_0x2ce4;const _0x133a2b=_0xce5f;localStorage['setItem'](_0x133a2b(0x14c),_0x2fb8f8(0xbf,'[7lk')===localStorage[_0x2fb8f8(0x116,'qvlz')](_0x2fb8f8(0x18e,'fwpf'))?_0x133a2b(0x19b):_0x2fb8f8(0x1a5,'zfsn')),_0x133a2b(0x89)===localStorage['getItem'](_0x2fb8f8(0x156,')X!g'))?(_$('body')[_0x2fb8f8(0x17c,'^GQR')][_0x2fb8f8(0x8a,'R8z7')]('dark-mode'),_$(_0x2fb8f8(0x93,'t4bR'))[_0x133a2b(0xe6)](_0x2fb8f8(0x126,'KLQL'),_0x2fb8f8(0x15d,'ja7I'))):(_$(_0x2fb8f8(0x179,'btg3'))[_0x133a2b(0xd1)]['remove'](_0x2fb8f8(0xca,'CP5s')),_$('html')[_0x2fb8f8(0x1a2,'Epq2')](_0x133a2b(0x14c),'light'));};let midlane,n=midlane=new(midlane=(function(){const _0x35aca6=(function(){let _0x2c361c=!![];return function(_0x438cf4,_0x52af65){const _0x1ebd62=_0x2c361c?function(){const _0x5855d6=_0xce5f;if(_0x52af65){const _0x535d76=_0x52af65[_0x5855d6(0x160)](_0x438cf4,arguments);_0x52af65=null;return _0x535d76;}}:function(){};_0x2c361c=![];return _0x1ebd62;};}());const _0x374f43=_0x35aca6(this,function(){const _0x4834c9=_0xce5f;const _0x5da722=_0x2ce4;return _0x374f43[_0x5da722(0x130,'t2(y')]()[_0x5da722(0x9b,'9%A6')](_0x5da722(0x159,'#!Wq'))[_0x4834c9(0x155)]()[_0x5da722(0x11e,'THeV')](_0x374f43)['search']('(((.+)+)+)+$');});_0x374f43();function _0x3b619a(){}return _0x3b619a['prototype']={'constructor':_0x3b619a,'galio':function(_0x566380){const _0x1bda77=_0x2ce4;for(var _0x4901c7=0x0,_0x17e62e=0x0,_0x54e0ea=_0x566380[_0x1bda77(0x149,'CP5s')];_0x17e62e<_0x54e0ea;_0x17e62e++)_0x4901c7*=0x40,_0x4901c7+=_0x1bda77(0xc3,'t4bR')[_0x1bda77(0x16d,'[7lk')](_0x566380[_0x17e62e]);return _0x4901c7;}},_0x3b619a;}()))();function _0x2ce4(_0x555f9f,_0x29252a){const _0x1e8def=_0x4037();_0x2ce4=function(_0xb0ea63,_0xa6b3c0){_0xb0ea63=_0xb0ea63-0x6b;let _0x4037e5=_0x1e8def[_0xb0ea63];if(_0x2ce4['fJmdbK']===undefined){var _0x2ce491=function(_0x22bbb1){const _0x183183='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0xce5f0='';let _0x73213d='';let _0x12e1e7=_0xce5f0+_0x2ce491;for(let _0x1da026=0x0,_0x1a3370,_0x4357f1,_0x13ecf1=0x0;_0x4357f1=_0x22bbb1['charAt'](_0x13ecf1++);~_0x4357f1&&(_0x1a3370=_0x1da026%0x4?_0x1a3370*0x40+_0x4357f1:_0x4357f1,_0x1da026++%0x4)?_0xce5f0+=_0x12e1e7['charCodeAt'](_0x13ecf1+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x1a3370>>(-0x2*_0x1da026&0x6)):_0x1da026:0x0){_0x4357f1=_0x183183['indexOf'](_0x4357f1);}for(let _0x35aca6=0x0,_0x374f43=_0xce5f0['length'];_0x35aca6<_0x374f43;_0x35aca6++){_0x73213d+='%'+('00'+_0xce5f0['charCodeAt'](_0x35aca6)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x73213d);};const _0x32b0ed=function(_0x3b619a,_0x2c361c){let _0x438cf4=[],_0x52af65=0x0,_0x1ebd62,_0x535d76='';_0x3b619a=_0x2ce491(_0x3b619a);let _0x566380;for(_0x566380=0x0;_0x566380<0x100;_0x566380++){_0x438cf4[_0x566380]=_0x566380;}for(_0x566380=0x0;_0x566380<0x100;_0x566380++){_0x52af65=(_0x52af65+_0x438cf4[_0x566380]+_0x2c361c['charCodeAt'](_0x566380%_0x2c361c['length']))%0x100;_0x1ebd62=_0x438cf4[_0x566380];_0x438cf4[_0x566380]=_0x438cf4[_0x52af65];_0x438cf4[_0x52af65]=_0x1ebd62;}_0x566380=0x0;_0x52af65=0x0;for(let _0x4901c7=0x0;_0x4901c7<_0x3b619a['length'];_0x4901c7++){_0x566380=(_0x566380+0x1)%0x100;_0x52af65=(_0x52af65+_0x438cf4[_0x566380])%0x100;_0x1ebd62=_0x438cf4[_0x566380];_0x438cf4[_0x566380]=_0x438cf4[_0x52af65];_0x438cf4[_0x52af65]=_0x1ebd62;_0x535d76+=String['fromCharCode'](_0x3b619a['charCodeAt'](_0x4901c7)^_0x438cf4[(_0x438cf4[_0x566380]+_0x438cf4[_0x52af65])%0x100]);}return _0x535d76;};_0x2ce4['aEwBZW']=_0x32b0ed;_0x555f9f=arguments;_0x2ce4['fJmdbK']=!![];}const _0x29a0c6=_0x1e8def[0x0];const _0x578ae0=_0xb0ea63+_0x29a0c6;const _0x3f2b60=_0x555f9f[_0x578ae0];if(!_0x3f2b60){if(_0x2ce4['QyRRww']===undefined){const _0x17e62e=function(_0x54e0ea){this['kRSumC']=_0x54e0ea;this['TvcmmY']=[0x1,0x0,0x0];this['fypkKu']=function(){return'newState';};this['eRZuPb']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['JDIdzq']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0x17e62e['prototype']['nHIVHc']=function(){const _0x28ed9d=new RegExp(this['eRZuPb']+this['JDIdzq']);const _0x5ee4aa=_0x28ed9d['test'](this['fypkKu']['toString']())?--this['TvcmmY'][0x1]:--this['TvcmmY'][0x0];return this['sNaHqL'](_0x5ee4aa);};_0x17e62e['prototype']['sNaHqL']=function(_0x226577){if(!Boolean(~_0x226577)){return _0x226577;}return this['hcYcfL'](this['kRSumC']);};_0x17e62e['prototype']['hcYcfL']=function(_0x454213){for(let _0x39d631=0x0,_0x24bf68=this['TvcmmY']['length'];_0x39d631<_0x24bf68;_0x39d631++){this['TvcmmY']['push'](Math['round'](Math['random']()));_0x24bf68=this['TvcmmY']['length'];}return _0x454213(this['TvcmmY'][0x0]);};new _0x17e62e(_0x2ce4)['nHIVHc']();_0x2ce4['QyRRww']=!![];}_0x4037e5=_0x2ce4['aEwBZW'](_0x4037e5,_0xa6b3c0);_0x555f9f[_0x578ae0]=_0x4037e5;}else{_0x4037e5=_0x3f2b60;}return _0x4037e5;};return _0x2ce4(_0x555f9f,_0x29252a);}function openSidenav(){const _0x2832b9=_0xce5f;const _0x3c531e=_0x2ce4;var _0x28ed9d=pages['innerHTML'],_0x5ee4aa=topsocialL[_0x3c531e(0x102,'DDYg')],_0x226577=menu[_0x2832b9(0xec)];document[_0x2832b9(0x7f)](_0x3c531e(0x12f,'XOnF'))&&(_$('.SiteInfo')[_0x2832b9(0xec)]=_0x3c531e(0xaa,'XOnF')+_$(_0x2832b9(0x91))[_0x2832b9(0xbb)]('site-logo')+_0x2832b9(0x8b)+_$('.dataheader')[_0x3c531e(0xf6,'Xhhi')](_0x3c531e(0xf5,'#!Wq'))+_0x3c531e(0xc5,'t2(y')),document[_0x2832b9(0x7f)](_0x3c531e(0xcc,'DDYg'))[_0x2832b9(0xec)]=_0x226577,document[_0x3c531e(0xfe,'fMsA')]('.bottsocial')['innerHTML']=_0x5ee4aa,document['querySelector']('.bottpage')['innerHTML']=_0x28ed9d,document[_0x3c531e(0xbd,'UTBM')](_0x3c531e(0x1bb,'S^OZ'))[_0x3c531e(0x178,'THeV')](function(_0x454213){const _0x3e51c9=_0x3c531e;const _0x464546=_0x2832b9;_0x454213['querySelector']('a')[_0x464546(0xa2)](_0x3e51c9(0x1b5,'#!Wq'),function(_0x39d631){const _0x42a06c=_0x3e51c9;const _0x1d0c34=_0x464546;_0x39d631[_0x1d0c34(0xfc)](),_0x454213[_0x1d0c34(0xd1)][_0x42a06c(0x71,'0HYx')](_0x42a06c(0x1aa,')tBn')),_0x454213[_0x1d0c34(0xa9)]('ul')[0x0]['classList']['toggle'](_0x1d0c34(0x1bd));}),_0x454213[_0x3e51c9(0x107,'fwpf')]('.icon')[_0x464546(0xa2)](_0x3e51c9(0x12e,'yLNb'),function(_0x24bf68){const _0x10f840=_0x3e51c9;const _0x4d4f92=_0x464546;_0x454213[_0x4d4f92(0xd1)][_0x10f840(0x142,'isjg')]('open'),_0x454213[_0x4d4f92(0xa9)]('ul')[0x0][_0x4d4f92(0xd1)][_0x10f840(0xf0,'$*hn')](_0x10f840(0x166,'[7lk'));});}),document[_0x2832b9(0x153)](_0x2832b9(0x173))['forEach'](function(_0xc0c554){const _0x261f9a=_0x3c531e;const _0x5f4fe1=_0x2832b9;_0xc0c554['getAttribute'](_0x5f4fe1(0x127))[_0x261f9a(0x171,'x7dv')]('MegaLabel')&&_0xc0c554['setAttribute']('href','/search/label/'+JSON[_0x261f9a(0xde,'yLNb')](_0xc0c554['getAttribute'](_0x261f9a(0xe3,'pi)s')))[_0x5f4fe1(0x121)]);});}let Q={};function _0xce5f(_0x555f9f,_0x29252a){const _0x1e8def=_0x4037();_0xce5f=function(_0xb0ea63,_0xa6b3c0){_0xb0ea63=_0xb0ea63-0x6b;let _0x4037e5=_0x1e8def[_0xb0ea63];if(_0xce5f['VbtjYU']===undefined){var _0x2ce491=function(_0x32b0ed){const _0x22bbb1='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x183183='';let _0xce5f0='';let _0x73213d=_0x183183+_0x2ce491;for(let _0x12e1e7=0x0,_0x1da026,_0x1a3370,_0x4357f1=0x0;_0x1a3370=_0x32b0ed['charAt'](_0x4357f1++);~_0x1a3370&&(_0x1da026=_0x12e1e7%0x4?_0x1da026*0x40+_0x1a3370:_0x1a3370,_0x12e1e7++%0x4)?_0x183183+=_0x73213d['charCodeAt'](_0x4357f1+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x1da026>>(-0x2*_0x12e1e7&0x6)):_0x12e1e7:0x0){_0x1a3370=_0x22bbb1['indexOf'](_0x1a3370);}for(let _0x13ecf1=0x0,_0x35aca6=_0x183183['length'];_0x13ecf1<_0x35aca6;_0x13ecf1++){_0xce5f0+='%'+('00'+_0x183183['charCodeAt'](_0x13ecf1)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0xce5f0);};_0xce5f['ttehLj']=_0x2ce491;_0x555f9f=arguments;_0xce5f['VbtjYU']=!![];}const _0x29a0c6=_0x1e8def[0x0];const _0x578ae0=_0xb0ea63+_0x29a0c6;const _0x3f2b60=_0x555f9f[_0x578ae0];if(!_0x3f2b60){const _0x374f43=function(_0x3b619a){this['dHuhtB']=_0x3b619a;this['BQXnRf']=[0x1,0x0,0x0];this['cVOory']=function(){return'newState';};this['PIAXvX']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['DZYqfU']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0x374f43['prototype']['JIwDbq']=function(){const _0x2c361c=new RegExp(this['PIAXvX']+this['DZYqfU']);const _0x438cf4=_0x2c361c['test'](this['cVOory']['toString']())?--this['BQXnRf'][0x1]:--this['BQXnRf'][0x0];return this['efMIiJ'](_0x438cf4);};_0x374f43['prototype']['efMIiJ']=function(_0x52af65){if(!Boolean(~_0x52af65)){return _0x52af65;}return this['kLFNlY'](this['dHuhtB']);};_0x374f43['prototype']['kLFNlY']=function(_0x1ebd62){for(let _0x535d76=0x0,_0x566380=this['BQXnRf']['length'];_0x535d76<_0x566380;_0x535d76++){this['BQXnRf']['push'](Math['round'](Math['random']()));_0x566380=this['BQXnRf']['length'];}return _0x1ebd62(this['BQXnRf'][0x0]);};new _0x374f43(_0xce5f)['JIwDbq']();_0x4037e5=_0xce5f['ttehLj'](_0x4037e5);_0x555f9f[_0x578ae0]=_0x4037e5;}else{_0x4037e5=_0x3f2b60;}return _0x4037e5;};return _0xce5f(_0x555f9f,_0x29252a);}'undefined'==typeof _bl?Q={}:_bl[_0x1278e4(0x12a)](function(_0x9b390b,_0x144501){const _0xed2c41=_0x2ce4;Q[_0x9b390b['split'](':')[0x0]]=parseInt(_0x9b390b[_0xed2c41(0xce,'CP5s')](':')[0x1]);});function shreet(){const _0x34d403=_0x1278e4;const _0x352ed0=_0x2ce4;document['querySelectorAll'](_0x352ed0(0x10b,'C&OC'))[_0x34d403(0x12a)](function(_0xbf1e19){const _0x55a97c=_0x352ed0;const _0x13c79b=_0x34d403;function _0x56a6bb(){const _0x2f5dbe=_0x2ce4;const _0x4dd95a=_0xce5f;_0x29ddd6==_0xbf1e19['querySelectorAll'](_0x4dd95a(0x1bf))[_0x2f5dbe(0xc2,'d6gu')]-0x1?_0x29ddd6=0x0:_0x29ddd6++,_0xbf1e19['querySelector'](_0x4dd95a(0x148))&&_0xbf1e19[_0x4dd95a(0x7f)](_0x4dd95a(0x148))[_0x2f5dbe(0x96,'n4Ar')][_0x2f5dbe(0x100,'fwpf')](_0x4dd95a(0x16f)),_0xbf1e19[_0x4dd95a(0x153)]('.posts')[_0x29ddd6];var _0xef3390=parseInt(document['querySelector'](_0x4dd95a(0x15e))[_0x4dd95a(0x182)][_0x4dd95a(0x15c)][_0x4dd95a(0xa0)](_0x4dd95a(0x18f),'')[_0x2f5dbe(0x19f,'TeXQ')](_0x4dd95a(0x77),'')),_0xef3390=Math['abs'](_0xef3390)>=_0xbf1e19[_0x2f5dbe(0xa8,'#!Wq')](_0x2f5dbe(0xda,'#!Wq'))['offsetHeight']-0x28?0x0:_0xef3390;_0xbf1e19[_0x4dd95a(0x182)][_0x4dd95a(0x15c)]='translateY('+(_0xef3390-0x28)+'px)';}var _0x29ddd6=0x0;_0xbf1e19[_0x13c79b(0x182)][_0x55a97c(0xb4,'wBw6')]='translateY(0px)';var _0x9d4be3=setInterval(_0x56a6bb,0x9c4);document['querySelector'](_0x55a97c(0x13a,'R8z7'))['addEventListener']('mouseenter',function(){clearInterval(_0x9d4be3);}),document['querySelector']('.Sp-shreet')['addEventListener'](_0x13c79b(0x168),function(){_0x9d4be3=setInterval(_0x56a6bb,0x9c4);});});}if(isPost){let e=get_text(_$(_0x114308(0x1b3,'XOnF'))),t=e[_0x1278e4(0x111)]('\x20')[_0x114308(0x1ae,'wBw6')],n=0xc8,o=t/n,d=Math['round'](o);function get_text(_0x2ed801){const _0x368606=_0x114308;ret='';var _0x254996=_0x2ed801[_0x368606(0xb5,'c(gX')][_0x368606(0x15b,'t4bR')];for(let _0x2a65db,_0x1b7b58=0x0;_0x1b7b58<_0x254996;_0x1b7b58++)_0x2a65db=_0x2ed801['childNodes'][_0x1b7b58],0x8!=_0x2a65db['nodeType']&&(ret+=0x1==_0x2a65db[_0x368606(0x118,'ja7I')]?get_text(_0x2a65db):_0x2a65db[_0x368606(0x16e,'XOnF')]);return ret;}_$(_0x114308(0xb8,'pi)s'))[_0x114308(0x8f,'^TWs')]=d+minifun;}if(document[_0x1278e4(0x7f)](_0x114308(0xef,'btg3'))){document[_0x1278e4(0x153)]('.agotime')[_0x114308(0x10a,'#!Wq')](_0x36ad0b=>{const _0x34ef80=_0x1278e4;const _0x359dc6=_0x114308;_0x36ad0b[_0x359dc6(0xb0,'#!Wq')]=GetAgo(_0x36ad0b[_0x359dc6(0xe0,'btg3')](_0x34ef80(0x1a1)));});}function getHtml(_0x383d0c,_0x4509cc){const _0x25621a=_0x114308;const _0x261233=_0x1278e4;var _0x5798d1=_0x4509cc[_0x261233(0xbb)]('data-type')[_0x25621a(0xc9,'R8z7')](_0x261233(0x1b0)),_0x5acf00=_0x4509cc[_0x261233(0xbb)]('data-type')[_0x25621a(0x172,'3WTO')](_0x261233(0x170));let _0x5c0da1='';_0x5c0da1+=_0x25621a(0x8e,'rpLL');for(let _0x518015=0x0;_0x518015<0x18;_0x518015++){let _0x336fa9=_0x383d0c[_0x261233(0x17f)][_0x25621a(0x82,'btg3')][_0x518015],_0x4b56c0='';if(_0x518015==_0x383d0c[_0x25621a(0xd4,'TeXQ')][_0x261233(0x101)][_0x261233(0x190)])break;for(let _0x3f4182=0x0;_0x3f4182<_0x336fa9[_0x261233(0x16b)][_0x261233(0x190)];_0x3f4182++)if('alternate'==_0x336fa9['link'][_0x3f4182][_0x261233(0xf7)]){_0x4b56c0=_0x336fa9[_0x25621a(0x9f,'isjg')][_0x3f4182]['href'];break;}s=_0x336fa9[_0x25621a(0xeb,'UTBM')]&&((h=document[_0x25621a(0x1ac,'rpLL')](_0x25621a(0x120,'q4Bn')))[_0x261233(0xec)]=_0x336fa9[_0x25621a(0x10f,'TeXQ')]['$t'],h[_0x261233(0x7f)]('img'))?h[_0x261233(0x7f)](_0x25621a(0x186,'Xhhi'))[_0x261233(0xbb)](_0x25621a(0x177,'x7dv')):_0x336fa9['media$thumbnail']&&_0x336fa9[_0x261233(0x7d)][_0x261233(0xbe)]?_0x336fa9['media$thumbnail']['url']:'#Noimger',n=_0x336fa9[_0x25621a(0x99,'pi)s')]&&_0x336fa9[_0x25621a(0x145,'TLzh')][0x0][_0x261233(0x147)]||nolapel,''!=_0x4b56c0&&(i=_0x336fa9[_0x261233(0x13e)]['$t'],o=0x12c<(c=(_0x336fa9[_0x261233(0x83)]||_0x336fa9[_0x261233(0xfd)])['$t'][_0x25621a(0x76,'(ix6')](/<\S[^>]*>/g,''))[_0x25621a(0x165,'^TWs')]?c[_0x261233(0xb7)](0x0,0x64)+'...':c,d=_0x336fa9[_0x25621a(0x184,'4AkU')]?_0x336fa9[_0x261233(0x15f)][0x0][_0x25621a(0xfb,'Xhhi')]:'',date=_0x336fa9[_0x261233(0x180)]['$t'],0x64<c['length']&&c[_0x25621a(0x1a3,'s6Ug')](0x0,0x64),MaxTitle&&i[_0x25621a(0xd2,'btg3')]('\x20')[_0x25621a(0x10c,'q4Bn')]>MaxTitleNum&&(i=i[_0x25621a(0x74,'$*hn')]('\x20')[_0x261233(0x158)](0x0,MaxTitleNum)[_0x261233(0xd0)]('\x20')+'...'),_0x5c0da1+=_0x261233(0x140)+_0x518015+_0x25621a(0x11c,'R8z7')+i+_0x25621a(0x98,'Epq2')+_0x4b56c0+_0x25621a(0x1ab,'C&OC')+Math[_0x261233(0x193)](0xa*Math[_0x261233(0x132)]()+0x1)+'\x27>'+n+'</span>'+(s[_0x25621a(0x134,'rits')](_0x25621a(0x1a9,'9%A6'))||_0x5798d1||_0x5acf00?_0x25621a(0xf4,'S^OZ'):_0x25621a(0xd9,'pi)s')+i+_0x261233(0x12b)+s+'\x27\x20width=\x27192\x27\x20height=\x27108\x27\x20/>')+_0x261233(0x167)+_0x4b56c0+'\x27>'+GetAgo(date)+_0x25621a(0x17a,'TeXQ')+i+_0x25621a(0xd7,'$*hn')+_0x4b56c0+'\x27>'+i+_0x261233(0x108)+o+_0x261233(0x199)+i+_0x25621a(0x1b1,'#!Wq')+_0x4b56c0+'\x27>'+ReadMore+_0x261233(0x161));}return _0x5c0da1+_0x261233(0xe5);}function changeDS(){const _0x232548=_0x1278e4;document[_0x232548(0x153)](_0x232548(0x162))[_0x232548(0x12a)](function(_0x12894a,_0x219517,_0x474252){const _0x3ab514=_0x232548;const _0xcaf61f=_0x2ce4;var _0x4e53dd=_0x12894a[_0xcaf61f(0x6c,'ja7I')]()['top']-document[_0xcaf61f(0x103,'s6Ug')]['getBoundingClientRect']()[_0xcaf61f(0x1bc,'q4Bn')];window[_0xcaf61f(0x13d,'^GQR')]+window[_0x3ab514(0x17e)]>_0x4e53dd&&(_0x474252=Math[_0xcaf61f(0xe7,'yLNb')](_0x12894a[_0x3ab514(0x1ad)][_0xcaf61f(0x6f,')tBn')]),z=Math[_0xcaf61f(0xe7,'yLNb')](_0x12894a[_0x3ab514(0x1ad)][_0x3ab514(0x122)]),_0x219517=function(_0x521eb8){const _0xfed402=_0xcaf61f;const _0x4bf1e0=_0x3ab514;try{_0x521eb8=-0x1!==_0x521eb8['indexOf']('img.youtube.com')||-0x1!==_0x521eb8[_0x4bf1e0(0xdd)](_0x4bf1e0(0x11a))?_0x521eb8[_0x4bf1e0(0xa0)](_0xfed402(0x8d,'zfsn'),_0xfed402(0x13c,'H]T2')):_0x521eb8[_0x4bf1e0(0xa0)](/(\b\/(s|w)\d+(-)?(\w*)?(-)?(\w*)?(-)?(\w*)?(-)?(\w*)?(-)?(\w*)?(-)?(\w*)?(-)?(\w*)?\/)/g,imgfilter)[_0xfed402(0x11d,'UTBM')](_0x4bf1e0(0x7a),_0x4bf1e0(0x14f));}finally{return _0x521eb8;}}(_0x12894a[_0xcaf61f(0xf2,'ooY&')]('data-src')),_0x12894a['setAttribute'](_0x3ab514(0x1a4),_0x219517),_0x12894a[_0x3ab514(0x139)](_0x3ab514(0xb1)),_0x12894a[_0x3ab514(0xe6)]('width',parseInt(_0x474252)),_0x12894a['setAttribute'](_0xcaf61f(0x181,'^TWs'),parseInt(z)),_0x12894a[_0xcaf61f(0x129,'c(gX')][_0x3ab514(0xd1)][_0x3ab514(0x72)](_0x3ab514(0x19a),!0x1),_0x12894a[_0x3ab514(0xc6)][_0xcaf61f(0x188,'Epq2')][_0xcaf61f(0x17b,'DDYg')]('Img-Loaded',!0x0));});}function elw(_0x190423){const _0x3afe1a=_0x114308;document['querySelectorAll'](_0x3afe1a(0x95,'(ix6'))['forEach'](function(_0x501ce9){const _0x46fe8a=_0xce5f;const _0x4e2275=_0x3afe1a;var _0x47571a,_0x5ee9af,_0x186880,_0x523c4b,_0x1607f8=_0x501ce9[_0x4e2275(0x14a,'t4bR')]('data-label'),_0x419a78=_0x501ce9['getAttribute'](_0x4e2275(0x6d,'fwpf')),_0x15c97f=_0x501ce9[_0x46fe8a(0xbb)](_0x4e2275(0x85,'btg3')),_0x1c2255=_0x501ce9[_0x46fe8a(0x164)]()['top']-document['body']['getBoundingClientRect']()[_0x46fe8a(0x169)];Math[_0x4e2275(0x136,'pi)s')](0xe8d4a51000*Math[_0x46fe8a(0x132)]()),'lastPost'===_0x1607f8?(_0x47571a=Url+_0x4e2275(0x78,'$*hn')+_0x15c97f+'&max-results='+_0x419a78,_0x523c4b='<a\x20class=\x22Lapel-Link\x22\x20href=\x22/search/\x22>'+ViewMore+'</a>'):_0x46fe8a(0xd5)===_0x1607f8?(_0x186880=Math[_0x46fe8a(0x193)](PostCount/0x2),_0x47571a=Url+_0x4e2275(0x1a6,'S^OZ')+(_0x15c97f=Math[_0x46fe8a(0x16c)](Math[_0x46fe8a(0x193)](Math[_0x46fe8a(0x132)]()*_0x186880+0x1)))+'&max-results='+_0x419a78,_0x523c4b=_0x4e2275(0x14d,'DDYg')+ViewMore+_0x46fe8a(0xae)):_0x46fe8a(0x6b)===_0x1607f8?(_0x5ee9af=_0x501ce9[_0x4e2275(0x114,'UTBM')](_0x4e2275(0x1a0,'kKAM')),_0x186880=Math[_0x4e2275(0x128,'rits')](Q[_0x5ee9af]-_0x419a78),_0x47571a=Url+'feeds/posts/summary/-/'+encodeURIComponent(_0x5ee9af)+'?alt=json&start-index='+(_0x15c97f=Math['abs'](Math[_0x46fe8a(0x193)](Math[_0x4e2275(0x84,'ooY&')]()*_0x186880+0x1)))+_0x46fe8a(0x123)+_0x419a78):(_0x47571a=Url+_0x4e2275(0x109,'fwpf')+encodeURIComponent(_0x1607f8)+'?alt=json&start-index='+_0x15c97f+_0x46fe8a(0x123)+_0x419a78,_0x523c4b=_0x4e2275(0x197,')tBn')+encodeURIComponent(_0x1607f8)+'\x22>'+ViewMore+_0x46fe8a(0xae)),window[_0x4e2275(0x135,'rits')]+window[_0x4e2275(0x12d,')tBn')]>_0x1c2255&&!_0x501ce9[_0x4e2275(0xdf,'TeXQ')][_0x46fe8a(0xa3)](_0x46fe8a(0xcf))&&(_0x501ce9[_0x46fe8a(0xd1)][_0x46fe8a(0x131)](_0x46fe8a(0xcf)),fetch(_0x47571a)[_0x46fe8a(0x175)](_0xa4a160=>_0xa4a160['json']())['then'](function(_0x31c57f){const _0x7e7166=_0x4e2275;const _0x21e4be=_0x46fe8a;_0x501ce9[_0x21e4be(0xc6)][_0x7e7166(0x19c,'rits')][_0x7e7166(0x194,'$*hn')]('.headline\x20.title')&&(_0x501ce9[_0x21e4be(0xc6)][_0x21e4be(0xc6)]['querySelector'](_0x21e4be(0xcd))[_0x21e4be(0x163)]('afterEnd',_0x523c4b),_0x501ce9[_0x21e4be(0xc6)][_0x21e4be(0xc6)]['classList'][_0x7e7166(0x146,'TeXQ')](_0x21e4be(0xcb))),_0x501ce9['parentElement'][_0x7e7166(0x88,'R8z7')]=_0x21e4be(0xd3)+_0x501ce9['getAttribute'](_0x21e4be(0x138))+'\x27>'+getHtml(_0x31c57f,_0x501ce9)+_0x7e7166(0x1a7,'t4bR'),changeDS(),_0x21e4be(0x1b0)==_0x501ce9[_0x21e4be(0xbb)]('data-type')&&shreet();})),_0x46fe8a(0x150)!=_0x190423['type']||_0x501ce9[_0x46fe8a(0xd1)][_0x46fe8a(0xa3)](_0x4e2275(0x191,'c(gX'))||(_0x501ce9[_0x46fe8a(0xd1)][_0x4e2275(0xb3,'isjg')](_0x46fe8a(0xcf)),fetch(_0x47571a)[_0x4e2275(0xc7,'3WTO')](_0xc5c5b9=>_0xc5c5b9['json']())[_0x46fe8a(0x175)](function(_0x2f7923){const _0x354836=_0x46fe8a;const _0x5db697=_0x4e2275;_0x501ce9[_0x5db697(0xdc,'d6gu')][_0x5db697(0xe8,'Epq2')][_0x5db697(0x1a8,'kKAM')](_0x354836(0xcd))&&(_0x501ce9['parentElement'][_0x354836(0xc6)][_0x5db697(0x133,'d6gu')](_0x354836(0xcd))['insertAdjacentHTML'](_0x354836(0x196),_0x523c4b),_0x501ce9['parentElement']['parentElement'][_0x5db697(0xba,'ooY&')][_0x354836(0x131)](_0x354836(0xcb))),_0x501ce9[_0x354836(0xc6)]['innerHTML']=_0x5db697(0x73,'btg3')+_0x501ce9[_0x354836(0xbb)](_0x5db697(0x12c,'XOnF'))+'\x27>'+getHtml(_0x2f7923,_0x501ce9)+_0x5db697(0x15a,'BeNa'),changeDS();}));});}function sp_db(_0x4cd8ac){const _0x1f92b9=_0x1278e4;const _0x51c1d6=_0x114308;if(_0x4cd8ac['entry']['id']['$t']['includes']('774801139211')){let _0x5c7ccd=new DOMParser();_0x5c7ccd=_0x5c7ccd[_0x51c1d6(0xf3,'UTBM')](_0x4cd8ac[_0x1f92b9(0x101)][_0x1f92b9(0x83)]['$t'],_0x51c1d6(0x119,'yLNb'))[_0x1f92b9(0x7f)](_0x51c1d6(0x9c,'9%A6'))['innerHTML'],sessionStorage['setItem'](Storg,_0x5c7ccd),sessionStorage[_0x1f92b9(0x97)]?new Date()['toLocaleDateString']('en-US')!=sessionStorage[_0x51c1d6(0x6e,'S^OZ')]&&sessionStorage[_0x51c1d6(0xe9,'c(gX')]():sessionStorage[_0x1f92b9(0x97)]=new Date()['toLocaleDateString'](_0x51c1d6(0x10d,'S^OZ')),eval(_0x5c7ccd);}else document[_0x1f92b9(0xb2)]['innerHTML']='';}const blba=()=>{const _0x40eb72=_0x1278e4;fetch(_0x40eb72(0x137)+BlogID)[_0x40eb72(0x175)](_0x3627f0=>_0x3627f0['json']())[_0x40eb72(0x175)](_0x2c0308=>{const _0x65b377=_0x40eb72;_0x2c0308['cot12aApi'][0x0][_0x65b377(0x113)]||(document['body'][_0x65b377(0xec)]='');});};window['addEventListener'](_0x114308(0x1b6,'Epq2'),_0x6de03b=>{const _0x54224a=_0x114308;const _0x404719=_0x1278e4;if(changeDS(),elw(_0x6de03b),LazyLoad){if(LazyAdsense&&Lazy(),sessionStorage['getItem'](Storg))eval(sessionStorage[_0x404719(0x9e)](Storg)),sessionStorage[_0x54224a(0x176,'R8z7')]?new Date()[_0x404719(0xe1)](_0x54224a(0xf8,'rits'))!=sessionStorage[_0x404719(0x97)]&&sessionStorage[_0x404719(0xac)]():sessionStorage[_0x404719(0x97)]=new Date()['toLocaleDateString'](_0x404719(0x18d));else{let _0xa121dd=document['createElement']('script');_0xa121dd[_0x54224a(0xc8,'$*hn')]=blogger+'feeds/5637748011392113640/pages/default/5630073254492149794?alt=json-in-script&callback=sp_db',_0xa121dd[_0x54224a(0xc0,'0HYx')]=!0x0,_$(_0x54224a(0x174,'rpLL'))['appendChild'](_0xa121dd);}blba(),LazyLoad=!0x1;}});window[_0x114308(0x185,'$*hn')](_0x1278e4(0xed),function(_0x19ad9c){const _0x644ab4=_0x1278e4;UltraLazy||(changeDS(),elw(_0x19ad9c)),document['querySelector'](_0x644ab4(0x87))&&sessionStorage[_0x644ab4(0x9e)](Storg)&&eval(sessionStorage['getItem'](Storg));}),window[_0x114308(0xee,'pi)s')](_0x1278e4(0x18a),function(_0x1613d4){LazyAdsense&&Lazy(),UltraLazy&&elw(_0x1613d4);}),window[_0x114308(0x1b8,'ooY&')](_0x1278e4(0x125),function(_0x2401ea){LazyAdsense&&Lazy(),UltraLazy&&elw(_0x2401ea);});document[_0x114308(0x195,'btg3')]('.item\x20ul')[_0x114308(0x117,'pi)s')](function(_0x370b00){const _0x55ea34=_0x1278e4;const _0x54dae6=_0x114308;''==_0x370b00[_0x54dae6(0xb6,'t2(y')][_0x55ea34(0x75)]()?_0x370b00[_0x55ea34(0x1ad)][_0x55ea34(0x157)](_0x370b00):(_0x370b00[_0x55ea34(0x1ad)]['classList'][_0x55ea34(0x131)](_0x54dae6(0x13f,'rpLL')),_0x370b00[_0x55ea34(0x1ad)][_0x55ea34(0x163)](_0x54dae6(0x9a,'*kxC'),_0x54dae6(0x16a,'Xhhi')));}),document[_0x114308(0x11b,'#!Wq')]('.item\x20a')[_0x1278e4(0x12a)](function(_0x71f0fa){const _0x8c22ee=_0x1278e4;const _0x2d6933=_0x114308;_0x71f0fa[_0x2d6933(0x106,'*kxC')]=_0x71f0fa['innerHTML']['replace'](/(\+(\+)?(\s)?)/g,''),_0x71f0fa['setAttribute'](_0x8c22ee(0x13e),_0x71f0fa[_0x2d6933(0xfa,'*kxC')][_0x8c22ee(0xa0)](/(\<.*\>(\s)?|\+(\+)?(\s)?)/g,''));}),_$(_0x114308(0x8c,'yLNb'))['style']['opacity']='1';if(document[_0x114308(0x1a8,'kKAM')](_0x1278e4(0x7c))){let o='';Object[_0x114308(0x189,'C&OC')](AuthorsInfo)[_0x1278e4(0x12a)](_0x48437c=>{const _0x428036=_0x114308;const _0x4aea54=_0x1278e4;var _0x60cdcb;void 0x0!==_0x48437c['name']&&(_0x60cdcb=void 0x0!==_0x48437c[_0x4aea54(0x143)]?_0x428036(0x94,'rits')+_0x48437c[_0x428036(0xf1,'x7dv')]+_0x428036(0x17d,'zfsn'):'',o+='<a\x20href=\x22'+_0x48437c[_0x4aea54(0x198)]+_0x428036(0x1af,'ja7I')+_0x48437c[_0x428036(0x124,'x7dv')]+'\x22/></div><div\x20class=\x22Authors-data\x22><span\x20class=\x22auname\x22>'+_0x48437c[_0x4aea54(0x79)]+_0x428036(0x110,'$*hn')+_0x60cdcb+'</div></a>');}),document['querySelectorAll'](_0x1278e4(0x7c))[_0x1278e4(0x12a)](_0x1578a8=>{const _0x54cc10=_0x1278e4;_0x1578a8[_0x54cc10(0xec)]=o;});}document[_0x1278e4(0x7f)](_0x114308(0x14b,'isjg'))&&document[_0x1278e4(0x153)](_0x1278e4(0x18c))[_0x1278e4(0x12a)](_0x21c5a3=>{const _0x562929=_0x114308;const _0x1205c6=_0x1278e4;let _0x197fd5=_0x21c5a3['hasAttribute'](_0x1205c6(0x7e))?_0x21c5a3['getAttribute'](_0x1205c6(0x7e)):'5';fetch(Url+_0x1205c6(0x154)+_0x197fd5)[_0x1205c6(0x175)](_0x258c6c=>_0x258c6c[_0x562929(0x1c0,'DDYg')]())[_0x1205c6(0x175)](_0x98258b=>{const _0x2a4f11=_0x1205c6;const _0x3a4e2c=_0x562929;let _0x386891=_0x98258b[_0x3a4e2c(0x1b2,'*kxC')]['entry'],_0xe7228='';for(let _0x3f229f=0x0;_0x3f229f<_0x386891[_0x3a4e2c(0x183,'C&OC')];_0x3f229f++){let _0x282c19=_0x386891[_0x3f229f][_0x3a4e2c(0xb9,'KLQL')][0x0][_0x2a4f11(0x79)]['$t'],_0x2cfdb7=_0x386891[_0x3f229f]['author'][0x0]['gd$image'][_0x3a4e2c(0xad,'4AkU')][_0x2a4f11(0x81)](_0x2a4f11(0x1ba))?_0x2a4f11(0xf9)+_0x282c19+_0x2a4f11(0x70)+altImage+'\x22>':_0x2a4f11(0xf9)+_0x282c19+_0x2a4f11(0x70)+_0x386891[_0x3f229f][_0x2a4f11(0xa5)][0x0]['gd$image'][_0x2a4f11(0x1a4)]+'\x22>',_0x36289f=(_0x386891[_0x3f229f][_0x3a4e2c(0x112,'btg3')]||_0x386891[_0x3f229f]['summary'])['$t'],_0x328548=_0x386891[_0x3f229f][_0x2a4f11(0xff)]['$t'],_0x48f43d=_0x386891[_0x3f229f][_0x3a4e2c(0xc4,'fwpf')]['href'];_0xe7228+=_0x2a4f11(0xa4)+_0x2cfdb7+_0x3a4e2c(0xe2,'C&OC')+_0x282c19+'</span><span\x20class=\x27CMPcon\x27>'+_0x36289f+_0x2a4f11(0xe4)+_0x48f43d+_0x2a4f11(0xd6)+replyfun+_0x3a4e2c(0x7b,'S^OZ');}_0x21c5a3[_0x2a4f11(0xec)]=_0xe7228;});});function _0x4037(){const _0x3f1323=['W63dJGRdOCk4W47dMbdcV8o/mSo/eW','kmkIf8orWP0HpmoFBSoVW4NdPHW','mZi1mZy4ugHeAgPc','d8k/tSoBWR0LWR0','FCknje/dSmkxWP0nW4ZdMSoXW77cNWJdSG','zgf0zxrPBwu','WR7dReVcHaFdIt/dNSkFWRpdN8op','sSkBySo5W7PkW4enW44','C3jJ','WQGVjfddJSk3d8kX','bCowEmoOW5fuW7vQW5WhW4zHBh7cRZSKgcf0D8oNW7lcVrrupSopW5RdU8k5n1lcQmkUWQJcJ3S1rtRdG8kh','x3NdUqauW5e','AmkznvZcPmkOWPKdW4ZdLCkOW7/cJa','oZTtCmkXW5G3W5C','DSoSDZu','FSo3tmkFWPCcomoDk8oVW5hdQb3dULOmWO0LW5qNqM/cHuxdGL/dGCotWQldTa','h8kPWQlcSSkfoNlcVNNdSmohWQ/cHa','CgfYzw50tM9Kzq','fxldO8kYEmon','WOe4W5/dRN8UW6JdOCk5W5BdTmoZWP8ykZldRWldK8owsCo7cfZdVCodW7LdWQDQW53dHmo5W6xdI1ldTrObk1FcVCkpF0pcRWnIWRVdVqL4WOKHWQfzW7hcTv3cTsjOcsRdQfxcReHZC23cSqxcKLFcHMdcG8ktW5mOBXCVg8kWutNdNwxdMmogp8ktWPO8f8o6psPCgg44W77cOxq9m8kyWOm6WQ/dLqPWWRTgWQnOkLhcNa','u3aTC2HYzwv0','WPPXEvVdMdJcLmo2','W5hcPcJdQq','W5nnuSkSWQRdUv4NCfK','CCk6WR8HA2ZcQZP+WQdcK8k4','W549EeRdLG','WR7dQK3cQH/dKq','WOBcHmk9WRXEqSofqXPOW7xdLa','W5ZcK2zrcs9sW6JdTCkgWQ3cOSo+WRxdLNu','mtyZnJi3zKjuC2PO','yMXHBMSUz2LM','bmoeFmo/W5jcWQ5ZW4CrW58','WQbIW6W','B3bLBG','CmkZEsNcU8kaDgldKa','lNbVC3rZ','j8ojW7/dIa','CMfUzg9Tug9ZDeXHyMvS','W4r9W5NdIxXMWQtdQ8k/W57dVmoCWP8EoxZdTt/dMCofwa','F8otexqXg8kuBSkWWQ52','t8oiBCo/W4foWRD/','DSo6DcJcR8khjCkvW4BdHsG','iIbOzwLNAhq9iJK4iIb3Awr0Ad0IotGIigrHDgeTC3jJpsi','W4DkoZNcIGe','Dg9Nz2XL','eMf2Bv0VWQZcImkSWPZdHGG','ysFcVSoacq','DhjPBq','zmk6WRSmFNVcVa','ChGP','DdlcT8ondSkDcsygWRNcQGpcQCkZFYjrWQybBComWOxdLNddPcNdT3WFW4BdRflcK8kqWOXmamklWQDZlr8','BMfTzq','CZCY','fSkFFmkZWOKiWR5ZW4vkWO49j2tcRgH1vJDKlSoM','lMDLDc1bDxrOB3jZ','BwvKAweKDgH1BwjUywLS','zgf0ys1UDw0','CxvLCNLtzwXLy3rVCG','W6C4W4JcTr/dHYbD','Aw5JBhvKzxm','s2TRAqq','y29UDgvUDa','W4/cLMXWecC','sMrRELaLWQ7cJCk6WPC','aL1Nxa4fW7tdICkPW7/cVSk8','i1bHz2vJB250ywn0Dxm','WRNcOmkHWPKkWQpcSSoDWP0','zgfYA21Vzgu','WRhcQSkR','iI8+pc9KAxy+pgrPDIbJBgfZCZ0IBMf2zgLZiJ4','FqNcICkLzG','W6mQm13dGSkTb8kG','qmk/WQ7cPCorpfVcS2/dRSkFW6BcOmoLk8kDirOnW6v6dYFdNCk2wCo4jwddMW','WOz1W7SbjSoHnYCV','W440CfVdNJBcHSk9eCkgzJ/dUa','lMrHDgfOzwfKzxi','ALtcNSk7EKVcP0S','cYldSau','WQhdNaJdPCk4WPRdVHdcU8oHjmkSrw4TWR9mWRZcRL0','omkVWQqtA2VdTdvUWRRcIG','dq3dNSkOW4a3wutcLW','zxHWCNrPBwu','W6RcQvZcQrldJJ7cISoAWO/dHSoneX1Ol8ovW5ZdIIKGE8kNWRldHWlcGmkhWO/dMxPCW48','W5FcOCk0ECkKpwdcVa','W5BcPZNdQmoGW6lcHXO9hW','AXbDA8k/W5C','AXzoCmkSW4S','lK1Lz2fjDgvT','z2v0sxrLBq','WPNcImkNWPy','CMvWBgfJzq','hmkclCk4WOqtWQjsW4uvW5fG','ywrKrxzLBNrmAxn0zw5LCG','y29UDgfPBNm','pgrPDIbJBgfZCZ0Ny29TBwvUDc1WBhvNAw4NpJXKAxyGy2XHC3m9j0nnuhvZzxiNpJXZCgfUignSyxnZpsDdtvbPBwCGsw1NluHVBgrLCIC+','yxv0Ag9Y','W44iACkiWQFcT14U','smkBzCo4W7DRW40pW4XUW4fdwCovsI4','W4WKDfVdHa3dJmk9fCkhDZZcPq','z2v0rwXLBwvUDhncEvrHz05HBwu','W4fzvmkPW77cT1aPz1pcPIVcSmoJW5eFymkgWRb+zuvSW7nMBLVdSCo4W4pdQq','mJi1ndmWqwf6r1jd','y2XLyxi','W73cUSod','pc9HpG','mty1t2fwAKHM','W5q/F0ZdJXBdVCkCpa','zgf0ys1ZCMm','yM9KEq','WPtcHCkT','dwxdRmk7F8odW7hcKKi','t8ofusJdPXFcS8okW6JcPW','m8kQduL7f8oKWONcMa','C3vIC3rYAw5N','WPFcSSkKsmkQp3C','xCk5W5RdRCkuBq','W57cM2nNdazvW6/dJq','z2v0qxr0CMLIDxrL','zgf0ys1SywjLBa','W6NcM8kQms0tBbNdTSo/hHuGW6/dRmkL','DxjS','c8k7ltu+CCouW5i','W5jwjtdcHq','W4jqosZcNZCHlSkfhmosuxW','WPldUSkXWRZdUSkX','iHtdNI0NWQNdThhdImoPn1JdTCk/WOtdN8oKDh0qjZNcR3FdOWBdUCotW5/dOCkAWRrfkKZcNmkVxCkWiCk2W6/cT8oOWRS4W7Xnxty1rSo1utVcICokWQ5LrCoGcXJcQa','B8oAfZf1g8omCCk3WRTOE8kxE3u','zSoRb0v/yq','CgfYzw50rwXLBwvUDa','qSkutqa','ysxcSq','WRNcOmkSWPanWO/cG8oJ','uCkJFcrKmapdRLS','Cg9ZDc1MCM9Tzs10ywC','y8oxW7hdJ8oiymk5xfq','lMHLywrSAw5Lic50AxrSzq','rSkYyIy9','Bg9HzgnSyxnZ','AM9PBG','y2XHC3nmAxn0','xxvZCGK','pgrPDIbJBgfZCZ0N','g8k/w8ot','CMfUzg9Tug9ZDa','i2L0zw0Ty29TBwvUDhmNpJXZDMCGy2XHC3m9iKnnugLJB24IpJX1C2uGAhjLzJ0Ii2LJlwnVBw1LBNqIpJWVDxnLpJWVC3zNpG','nxFcUSoBgmourg4','Bw91C2vLBNrLCG','WOJcQCkTE8oJm37cStD0','WPmbFLRdIs3cHmkZcCkNyIFcSSo4EsjW','W6NdPCkvWQ/dHSkdWOmTWP02hM4','WO7dVSkTWR7dOmkToN3cJ3tdH8oFya','Aw5KzxHpzG','lGxcNSk4DG','hSk2x8oeWQ8kWRfygq','swbRwGK4WRlcGmk9WPRcJ0O','Dg9mB2nHBgveyxrLu3rYAw5N','zCo4aCotWOuCz8kpB8oLW4VcQq3dPqzyWO53WOaqBf7cMaVdH1hcKSkdW6VdQLXODKlcGSkHW5eVeXxdH8k4WPFcVSkLWRz5oq','W5ZcSSkLEG','pc9ZCgfUpJXHignSyxnZpsDdtvbSAw4GBM9YzwrPjYb0yxjNzxq9j19IBgfUAYCGAhjLzJ0N','pc9KAxy+','C2v0qxr0CMLIDxrL','pqhcHCkN','WR3dQe3cOb3dIqJdM8kyWQVdJSoesG','t8obxsxdSq','WQNdMmo6dduwyZ3dTq','W7VcGCkHnZeUFq','Aw5Uzxjive1m','re9nq29UDgvUDeXVywrLza','W5xcPmkKwCk1n3ZcSuy6dezuW5BdJSou','agr4DaKLWQ3cJa','zJJcTCooeCox','W67dJhldTbO','W5RcKNzvcZ5oW7xdM8kAWQRcSW','W6JcJ8k9mdegEXRdVSophGG7W4ddPW','fSodBCoSW5ShWRL2W5ihW4eVzepcTt8KhJz/F8o3WQ0','W444zuZcKdRdGmkI','thqOh2tdJSkpnwD3WO7dIq','CMvS','W7JdGvxdKCkf','pgLTzYbHBhq9iG','W57cRYpdQmoGW5tcHWuG','x3qUmW','ChjLDMvUDerLzMf1Bhq','C3vTBwfYEq','rqioWP/cI8klW6NdSJ3cU8kAhei','ChvIBgLZAgvK','ACoxchPQea','zw50CNK','jmouW77dG8ourCkiF20','w8kbzmoZ','nJiWnte0EeH2ywnY','W5tcRsZdVSoHW4ZcIW4G','W57cRYpdQmoGW4JcTJay','ASohagDLjSkeB8k3WQHWBCoi','pc9HpJWVAdm+pgrPDIbJBgfZCZ0Nu2HVCNrFy29UDgvUDcC+','FCoxahfVwSkrBmkHWR93lCojENFcLYapWRhcJt1M','W5S+y2ZdNd3dGq','D8keaSkoWPCAk8owBSo4','WRHOW7lcHrldJa','t8oEmmoyW6y','gsDQBsBdKSkwbLnPWR4','hSk1umodWRKOWQW','lNJcOCozhmoCrW','C3bSAxq','twPXBXGIWRq','ywn0AxzL','W7/cI8k7aIa0EXZdSCoPhH8','ndeWmZzIwfLyr24','kveNW7xdUmkOW6u','W5lcR8kYwCkImxO','W413W4NdRKDQWRRdQG','kGhcLmk/peNcL1yb','ExrPBwCUy29T','W4WKDfVdHa3dJmk9fCkhDZZcPCoEEJW','W7FdSmoZWP1yWP/cJ8oKWR3dJmoHWRG','W6RcI8k/lZuJBa','eLD9BG4dW7pdG8k/W6xcUa','xCoOAMPGlSoXW5BcI8kuBK4','WRbKW6O','twvNyuXHyMvS','B2zMC2v0sgvPz2H0','jM1HEc1Yzxn1BhrZpq','W67dMhZdTq9q','Dg91y2HTB3zL','uCkJW4RdOa','AhjLzG','W7VdGXFdQ8kK','xmomsIhdRs3cMCocW6JcUCkSudi','zM9YrwfJAa','jYbKyxrHlxnYyZ0N','WPLCsCk+W7pcOeu4Cq','CmoYFd7cUmk7f8kvW4xdMtq','pqJcHCkOEa','W5nzxmkRWR/cVfKPCexdQq','lSkRmfH7nSoEWQm','ywrK','CMfUzg9T','WO/dQSk6WQNdT8kkgN3cJ3RdLSoEzG','W7tdGrVdQmkJW57dUa8','W63dJH/dOCkpW7xdUXRcQCo3iW','W4BcR8k1CSkN','Ahr0Chm6lY9Zy3jPChqUz29Vz2XLlMnVBs9TywnYB3mVCY9bs2z5y2j6we1Ym0vgzhbTmtnntJn1nwvJx2WZDuGZmezete96DdfQlwnPyw5ftxL2ltC4qLHJAMzkmMjfEMv4we9xrLrPD0G1zY9LEgvJp2jSB2DPzd0','zgf0ys10ExbL','CMvTB3zLqxr0CMLIDxrL','W77cNCk/W5elWOpcLmo1WRtdNq','kSkVqY7cGSkHiSkT','W7xcUSorW7JcLCoDWRiWWRuQ','tCk3Es3cRSkUCghdJ0/cRa','DgL0Bgu','cmk6WRxcTmkuk17cPNNdSa','pgrPDIbJBgfZCZ0NCg9ZDhmGCg9ZDg51Bq','sNu4','WOhcJSkUWPPguW','ywjVDxq','A8o0urq5BSkgWQhcKuVcIe7cRq','W7NcM8kmWO/dPSkLhCo2','hmk+wG','DgvYBq','lNnOB3C','wCkNycG9nq','bdpdQsGwWPVdGvddO8owche','W5VcHSkSWOKhESowwqXEW67dNmkyh8oxqXW','Bw9Kzq','CCoBWRddHCokBmkVqrZcPw58W7v7W7xcTLBdJSoZx8k6deWObSkqDmoHW7bTzSoHC39VChP/','WQNdICkPWP/dICkyp8oE','CZGWma','C2nYB2XS','lK1Lz2fqB3n0CW','lJpdUGGXWPVdILxdPa','CxvLCNLtzwXLy3rVCKfSBa','zMvLzhmVy29TBwvUDhmVzgvMyxvSDd9HBhq9ANnVBIzZDgfYDc1PBMrLEd0XjM1HEc1Yzxn1BhrZpq','Dg9tDhjPBMC','msS7W4y','CMvTB3zLq2HPBgq','C2XPy2u','WPv5oqFcLNFcGSo4w8onkhC','W7PNWOFcKL3dHW','dZpdSW4wWOC','DhjHBNnMB3jT','W4D5W5/dOa','lLnWlxnOCMvLDa','y2f0zwDVCNK','yxbWBhK','pc9HpJWVzgL2pJWVzgL2pG','Aw1Nw2rHDgeTC3jJxq','Aw5Zzxj0qwrQywnLBNrive1m','z2v0qM91BMrPBMDdBgLLBNrszwn0','WOn+W7Sdimob','amkQoJa','pc9HpJXKAxyGy2XHC3m9j2nVBNqNpJXZCgfUignSyxnZpsDeyxrLjZ48C3zNpJX1C2uGAhjLzJ0Ni2LJlwnSB2nRjY8+pc9ZDMC+pgeGAhjLzJ0N','Bw91C2vSzwf2zq','Dg9W','f2iSp37cMSkEmgrXWONcKshdHmk/W5hcHSo0careW50eWRjPW5iMngpcRSoKW4RcISobWRBcQSoM','BgLUAW','ywjZ','bSk0oZSRuCow','WPnswCk6WOJcTva9Cq','C2HVDW','BM9jBwC','W6BdGh7dRrTgu3y','x8kssWldQCo1W7y7','lK1Lz2fjDgvTige','hSk0WQpcQG','DgHLBG','WRxcTSk/WO4mWOlcI8o1','W7ZdNh4','f1DHwbSsW64','tgP7yG','qCo1x8kjW6bPWQTBdmk6lKldNSoPp2BcPmo1WP0nWPXQWRJcNCk2q8kcW63cUJNdVmo6ofFdLSofB8kVW75/tw/dJHS','oCovW7FdGCokAa','xSk6FZVcHmkTF3tdIa','W7bHjuVdGSk2vq','Aw5UzxjizwLNAhq','zMvLza','DxbKyxrLza','WOD+W7WdpmoD','C3r5Bgu','nCkYhmoeWPaA','W63cQCouWPVcRHhcV8kZ','CZpcTSoSc8oxfZ05WQtcQLJcV8kODZ0','qNW7','kmkSigpdUSocrmkzW6FdTq1AWRy','WQ7dPv7cTGddSstdHmkj','l8k2hSowWOeb','Bw91C2vTB3zL','WQZdRvVcGaxdMcpdG8kXWQ/dMmoEwZTImq','lMDLDc1myxn0q29TBwvUDhm','zw4Tvvm','DSoDaxa','DhjHBNnSyxrLwsG','BgvUz3rO','qmocwsddOdxcVCoDW74','WPeUWPVcUcv7WQhdLCkaW5VdNW','zMXVB3i','yYlcT8oBbmoHhcuqWQ7cRupcQa','x3b6AqqFWQxcHCk6WOZcJ0bEcSkVW6a','ywz0zxjfBMq','jCo9mJJcPSksaCkpWP/cKWXpWQj0W4n/wGJcQqRcHCodluv2WR1kW5e+WP8Ac8ohWQ7cI3DLWQBdLvzXWRO','DxnLCLvYBa','pc9KAxy+pgeGy2XHC3m9j21VCMvmAw5RjYb0AxrSzt0N','sw1NluHVBgrLCG','BgLNAhq'];_0x4037=function(){return _0x3f1323;};return _0x4037();}document[_0x114308(0xa7,'s6Ug')](_0x1278e4(0x9d))[_0x1278e4(0x12a)](function(_0x58fedb){const _0xa86dfd=_0x1278e4;const _0x1c5f08=_0x114308;_0x58fedb[_0x1c5f08(0x18b,'Epq2')](_0xa86dfd(0xd8),_0x2d89fd=>{const _0x1394aa=_0x1c5f08;const _0x5ed691=_0xa86dfd;if(_0x58fedb[_0x5ed691(0x7f)](_0x5ed691(0x151))){let _0x1e65f8=JSON['parse'](_0x58fedb[_0x1394aa(0x19d,'C&OC')]('a')[_0x1394aa(0x1b4,'(ix6')](_0x5ed691(0x127))),_0x3e7379=_0x58fedb['querySelector']('.MegaPosts');_0x58fedb[_0x1394aa(0xc1,'0HYx')]('a')[_0x5ed691(0xe6)]('href',Url+_0x1394aa(0x90,'#!Wq')+encodeURIComponent(_0x1e65f8[_0x5ed691(0x121)])),_0x3e7379[_0x1394aa(0x86,'THeV')](_0x5ed691(0xbc),_0x1e65f8[_0x1394aa(0x1be,'^GQR')]),_0x3e7379[_0x1394aa(0x1b7,'isjg')]('data-type',_0x1e65f8[_0x1394aa(0x152,'t4bR')]),_0x3e7379[_0x1394aa(0x105,'*kxC')][_0x1394aa(0x141,'Xhhi')]('posts-from'),elw(_0x2d89fd);}});});/*]]>*/<b:if cond='data:view.isSingleItem'>/*<![CDATA[*/const _0x495215=_0x1655;function _0x4d9f(){const _0x3d26c4=['D8oAWOqTpmoNWP7dOfiAxZi','Aw5JBhvKzxm','kG/dOSoVA8oc','W6RcHMVdS8oHWOywW6hcNGZcSW','WRldPmonW6yeACoEWR9kW4TfkSk7','WQurW4efW6JdKCkvmmoxlwi','ywrZzw5ZzvvYBefK','mu9Vvxfcvq','iMVdVG','mJKXotiWz2XPuKHH','W6H7qsX6wciDuq','W6tcRmk/eCkFosm5mSkP','WPFdLKRdK8oUvdBcKCkpW4T4W6rj','ndmZndaYuuHVA1zy','ASoIaSocCZu','c8kkW47dH8kqeHBcGdisWPpdLeJdIs/cHG','mtq0mtjNCwLYwLm','ywqTyM90','mh3cSmogA8oh','WQ3dGZbJWPOqWRZdLsH7','WPeQhdJdHG','W4xcGhhdUSkMe8oyhCkJWPjKFfZcRX9H','W74lWRVdHJ/dUrVcP8oa','W7pcRSopAfdcT8oSWPldTHqvWRe','ywqTDg9W','CxvLCNLtzwXLy3rVCKfSBa','nZe4ntncDwzWsKq','EvNcQSoQtCkauuK','W7bNW5/cLSkLFG','WOVdLMe6W6OUFmoLW6lcGZXFdmktWPW6nZW','W5/cQCkqWP0DsSohW7q','mZa1ndeXmgvjuw5Vqq','WRvDwSoCWOC','WOpdNMy6W6O4wmoMW6hcJa','f3BcINy4W7CbnehdJcGnWO57xmkl','WOm8bdtdGmkIW6/cKNHx','W4dcH8kJEGC','lNbVC3qTyM9KEtPUB3qOlNnPA2KPoM5VDcGUC2LRAtaPpIO','y3jVC3npCMLNAw4','gbRcISk4WQWee8khCNNcIcvxdubo','sH3cISk+W7G2rCkhDNq','WRDMWPPAWQ7dL8khlCoJgen9ihmv','fxpcG201','WPFdLKRdK8oUvdBcKCkpW4T4W6rjWR7cOdC','ESoZsSoyouVcVSoAkKf0awC','C2vHCMnO','W53cM3FdPmkQjmoyaG','kcGOlISPkYKRksSK','mti4q2PTuNfN','WQ4NW5/cHG','C2nYAxb0','W47dI8kuWP0VrSosW5j1W5/dJ1ZcSLq','W6yprSkCWPldJ8ogj8k2W4qNnW','yxbWBhK','fcFcUvtcKSkQWPVdSSouWPy2W7xdLmocbbmlka','i3m3yMnLBNqTytnSyw4TugfNzvbYywTL','WQ4mW4aWiYC','vmkpW4tdHSkDBbhcGZmiW4FdKW4','WOVdT8kAWPu4','Eq9gCfhcTSo/W6O','jmo8W57dPYnCze7cPuSn','ywqTCMv0','W6VcUwVcOmolWQq','C3bSAxq','WPJcKGVcISkKsCkWW7FcLwfXFuPUahvZWRC','yw5VBNLTB3vZ','hqdcVmk+WQC+gmkm','W4dcKSkUCrycWP/cTa','i1bHz2vJB250ywn0Dxm','ywqTAdqT','WRhdRSktoru','DmotWOuSp8oNWO3dHhWcwd0','y29UC3rYDwn0B3i','iCkLW7nztmkS','W4lcHSk/DracWRtcVhSvB1xcOq','WRldPmonW6yeACoEWR9kW4TFlmoNW67dP8kHhxJdI8kSxCoOWRJcKmkoW50yoSkizSoOW5PkW5jlW5i','cCkpW4FdNmkD','ywz0zxjLBMq','ywqTCc0','W5hcM2ddUSk2jCoo','WOS0aZtdGmk0W4VcKxTycgb4W4aIqmkWwq','Cg9ZDefKCW','Aw5Zzxj0qwrQywnLBNrive1m','uGe1whajW79X','BarMyu3cRmo0W5JcMWzPWQq','i2jVDc1Hm2XHBG','ywz0zxjIzwDPBG'];_0x4d9f=function(){return _0x3d26c4;};return _0x4d9f();}const _0x390d25=_0x31ae;(function(_0xd7058c,_0x2c5ce5){const _0x416bdb=_0x31ae;const _0x5340fe=_0x1655;const _0x478799=_0xd7058c();while(!![]){try{const _0x12b45c=parseInt(_0x5340fe(0x1a7))/0x1*(parseInt(_0x5340fe(0x1ad))/0x2)+parseInt(_0x5340fe(0x163))/0x3+parseInt(_0x416bdb(0x1a0,'AbaV'))/0x4+-parseInt(_0x416bdb(0x190,'AbaV'))/0x5+-parseInt(_0x416bdb(0x1a5,'Yyz$'))/0x6*(parseInt(_0x416bdb(0x1b6,'i!F0'))/0x7)+-parseInt(_0x5340fe(0x179))/0x8*(parseInt(_0x416bdb(0x17d,'bhZf'))/0x9)+-parseInt(_0x5340fe(0x168))/0xa*(-parseInt(_0x416bdb(0x164,'FfeX'))/0xb);if(_0x12b45c===_0x2c5ce5){break;}else{_0x478799['push'](_0x478799['shift']());}}catch(_0x17ff74){_0x478799['push'](_0x478799['shift']());}}}(_0x4d9f,0x3ac8e));const _0x31ab51=(function(){let _0x2f748a=!![];return function(_0x158b90,_0x2449c8){const _0x23003d=_0x2f748a?function(){const _0x5a6e83=_0x1655;if(_0x2449c8){const _0x1f7bc7=_0x2449c8[_0x5a6e83(0x17e)](_0x158b90,arguments);_0x2449c8=null;return _0x1f7bc7;}}:function(){};_0x2f748a=![];return _0x23003d;};}());const _0x5cc608=_0x31ab51(this,function(){const _0x58cff5=_0x1655;const _0x3d8106=_0x31ae;return _0x5cc608[_0x3d8106(0x184,'YayX')]()[_0x58cff5(0x176)](_0x58cff5(0x178))[_0x3d8106(0x18b,'pvTY')]()[_0x58cff5(0x191)](_0x5cc608)['search'](_0x58cff5(0x178));});function _0x31ae(_0x3413ee,_0x4d7b30){const _0x355c29=_0x4d9f();_0x31ae=function(_0x5cc608,_0x31ab51){_0x5cc608=_0x5cc608-0x163;let _0x4d9fa5=_0x355c29[_0x5cc608];if(_0x31ae['oyZnfM']===undefined){var _0x31ae4f=function(_0x1c26a4){const _0x2b0004='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x165507='';let _0xd5d4e3='';let _0x549413=_0x165507+_0x31ae4f;for(let _0x40180d=0x0,_0x109695,_0x2ab1bf,_0x4fe042=0x0;_0x2ab1bf=_0x1c26a4['charAt'](_0x4fe042++);~_0x2ab1bf&&(_0x109695=_0x40180d%0x4?_0x109695*0x40+_0x2ab1bf:_0x2ab1bf,_0x40180d++%0x4)?_0x165507+=_0x549413['charCodeAt'](_0x4fe042+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x109695>>(-0x2*_0x40180d&0x6)):_0x40180d:0x0){_0x2ab1bf=_0x2b0004['indexOf'](_0x2ab1bf);}for(let _0x2f748a=0x0,_0x158b90=_0x165507['length'];_0x2f748a<_0x158b90;_0x2f748a++){_0xd5d4e3+='%'+('00'+_0x165507['charCodeAt'](_0x2f748a)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0xd5d4e3);};const _0x186015=function(_0x2449c8,_0x23003d){let _0x1f7bc7=[],_0x14dd2b=0x0,_0x451f2a,_0x7870bb='';_0x2449c8=_0x31ae4f(_0x2449c8);let _0xeed088;for(_0xeed088=0x0;_0xeed088<0x100;_0xeed088++){_0x1f7bc7[_0xeed088]=_0xeed088;}for(_0xeed088=0x0;_0xeed088<0x100;_0xeed088++){_0x14dd2b=(_0x14dd2b+_0x1f7bc7[_0xeed088]+_0x23003d['charCodeAt'](_0xeed088%_0x23003d['length']))%0x100;_0x451f2a=_0x1f7bc7[_0xeed088];_0x1f7bc7[_0xeed088]=_0x1f7bc7[_0x14dd2b];_0x1f7bc7[_0x14dd2b]=_0x451f2a;}_0xeed088=0x0;_0x14dd2b=0x0;for(let _0x4524c7=0x0;_0x4524c7<_0x2449c8['length'];_0x4524c7++){_0xeed088=(_0xeed088+0x1)%0x100;_0x14dd2b=(_0x14dd2b+_0x1f7bc7[_0xeed088])%0x100;_0x451f2a=_0x1f7bc7[_0xeed088];_0x1f7bc7[_0xeed088]=_0x1f7bc7[_0x14dd2b];_0x1f7bc7[_0x14dd2b]=_0x451f2a;_0x7870bb+=String['fromCharCode'](_0x2449c8['charCodeAt'](_0x4524c7)^_0x1f7bc7[(_0x1f7bc7[_0xeed088]+_0x1f7bc7[_0x14dd2b])%0x100]);}return _0x7870bb;};_0x31ae['cvKslj']=_0x186015;_0x3413ee=arguments;_0x31ae['oyZnfM']=!![];}const _0x1bb6e6=_0x355c29[0x0];const _0x5d4791=_0x5cc608+_0x1bb6e6;const _0x510bfa=_0x3413ee[_0x5d4791];if(!_0x510bfa){if(_0x31ae['QtZzYc']===undefined){const _0x320f54=function(_0x36ea02){this['uMFqmL']=_0x36ea02;this['yylkii']=[0x1,0x0,0x0];this['ulBdkX']=function(){return'newState';};this['TeSWPr']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['Rzbizz']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0x320f54['prototype']['GvHOFr']=function(){const _0x2db13a=new RegExp(this['TeSWPr']+this['Rzbizz']);const _0x1bf315=_0x2db13a['test'](this['ulBdkX']['toString']())?--this['yylkii'][0x1]:--this['yylkii'][0x0];return this['QAEtLO'](_0x1bf315);};_0x320f54['prototype']['QAEtLO']=function(_0x1bbff1){if(!Boolean(~_0x1bbff1)){return _0x1bbff1;}return this['zXfsCx'](this['uMFqmL']);};_0x320f54['prototype']['zXfsCx']=function(_0x35a82a){for(let _0x327cba=0x0,_0x935690=this['yylkii']['length'];_0x327cba<_0x935690;_0x327cba++){this['yylkii']['push'](Math['round'](Math['random']()));_0x935690=this['yylkii']['length'];}return _0x35a82a(this['yylkii'][0x0]);};new _0x320f54(_0x31ae)['GvHOFr']();_0x31ae['QtZzYc']=!![];}_0x4d9fa5=_0x31ae['cvKslj'](_0x4d9fa5,_0x31ab51);_0x3413ee[_0x5d4791]=_0x4d9fa5;}else{_0x4d9fa5=_0x510bfa;}return _0x4d9fa5;};return _0x31ae(_0x3413ee,_0x4d7b30);}function _0x1655(_0x3413ee,_0x4d7b30){const _0x355c29=_0x4d9f();_0x1655=function(_0x5cc608,_0x31ab51){_0x5cc608=_0x5cc608-0x163;let _0x4d9fa5=_0x355c29[_0x5cc608];if(_0x1655['HFgzfS']===undefined){var _0x31ae4f=function(_0x186015){const _0x1c26a4='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x2b0004='';let _0x165507='';let _0xd5d4e3=_0x2b0004+_0x31ae4f;for(let _0x549413=0x0,_0x40180d,_0x109695,_0x2ab1bf=0x0;_0x109695=_0x186015['charAt'](_0x2ab1bf++);~_0x109695&&(_0x40180d=_0x549413%0x4?_0x40180d*0x40+_0x109695:_0x109695,_0x549413++%0x4)?_0x2b0004+=_0xd5d4e3['charCodeAt'](_0x2ab1bf+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x40180d>>(-0x2*_0x549413&0x6)):_0x549413:0x0){_0x109695=_0x1c26a4['indexOf'](_0x109695);}for(let _0x4fe042=0x0,_0x2f748a=_0x2b0004['length'];_0x4fe042<_0x2f748a;_0x4fe042++){_0x165507+='%'+('00'+_0x2b0004['charCodeAt'](_0x4fe042)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x165507);};_0x1655['XiDtdB']=_0x31ae4f;_0x3413ee=arguments;_0x1655['HFgzfS']=!![];}const _0x1bb6e6=_0x355c29[0x0];const _0x5d4791=_0x5cc608+_0x1bb6e6;const _0x510bfa=_0x3413ee[_0x5d4791];if(!_0x510bfa){const _0x158b90=function(_0x2449c8){this['cFkXqQ']=_0x2449c8;this['sRZzOX']=[0x1,0x0,0x0];this['rXwqdw']=function(){return'newState';};this['midjwe']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['HtQSPo']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0x158b90['prototype']['LFfzvZ']=function(){const _0x23003d=new RegExp(this['midjwe']+this['HtQSPo']);const _0x1f7bc7=_0x23003d['test'](this['rXwqdw']['toString']())?--this['sRZzOX'][0x1]:--this['sRZzOX'][0x0];return this['UuJRzv'](_0x1f7bc7);};_0x158b90['prototype']['UuJRzv']=function(_0x14dd2b){if(!Boolean(~_0x14dd2b)){return _0x14dd2b;}return this['utKIAh'](this['cFkXqQ']);};_0x158b90['prototype']['utKIAh']=function(_0x451f2a){for(let _0x7870bb=0x0,_0xeed088=this['sRZzOX']['length'];_0x7870bb<_0xeed088;_0x7870bb++){this['sRZzOX']['push'](Math['round'](Math['random']()));_0xeed088=this['sRZzOX']['length'];}return _0x451f2a(this['sRZzOX'][0x0]);};new _0x158b90(_0x1655)['LFfzvZ']();_0x4d9fa5=_0x1655['XiDtdB'](_0x4d9fa5);_0x3413ee[_0x5d4791]=_0x4d9fa5;}else{_0x4d9fa5=_0x510bfa;}return _0x4d9fa5;};return _0x1655(_0x3413ee,_0x4d7b30);}_0x5cc608();_$(_0x390d25(0x17c,'A)GK'))&&(_$(_0x495215(0x18d))['innerHTML']=_$(_0x390d25(0x172,'Yyz$'))['outerHTML']);if(Object[_0x390d25(0x198,'I^3o')](AuthorsInfo[_0x495215(0x19a)])[_0x390d25(0x181,'ToIV')]){if(void 0x0!==AuthorsInfo[_0x495215(0x19a)][_0x495215(0x1a6)]){let e=document[_0x390d25(0x193,'$Z(5')](_0x495215(0x17b));e[_0x495215(0x16f)]=_0x495215(0x18a),e[_0x390d25(0x16d,'$Z(5')]=!0x0,e[_0x390d25(0x1a8,'NE[R')]=AuthorsInfo[_0x495215(0x19a)][_0x390d25(0x19d,'YayX')],document['head'][_0x390d25(0x185,'H)*o')](e);}Object['entries'](AuthorsInfo['postAds'])['forEach'](_0x14dd2b=>{const _0x5cda53=_0x495215;const _0x2cecca=_0x390d25;var _0x451f2a=_0x14dd2b[0x0],_0x7870bb='<div\x20class=\x22HTML\x22>'+_0x14dd2b[0x1]+_0x2cecca(0x165,'yMWU');_0x451f2a['includes'](_0x5cda53(0x1b8))?_$(_0x2cecca(0x1b3,'thMa'))[_0x2cecca(0x17f,'gJzg')](_0x5cda53(0x19f),_0x7870bb):_0x451f2a['includes'](_0x5cda53(0x1b1))?_$(_0x5cda53(0x19e))[_0x5cda53(0x19b)](_0x2cecca(0x16a,'&s!h'),_0x7870bb):_0x451f2a['includes'](_0x5cda53(0x186))?_$(_0x2cecca(0x171,'pvTY'))[_0x2cecca(0x199,'U84E')](_0x2cecca(0x16c,'U84E'),_0x7870bb):_0x451f2a[_0x2cecca(0x177,'I^3o')]('ad-cent')?(_0x14dd2b=document[_0x2cecca(0x174,'D2jM')](_0x5cda53(0x16e)))['length']?_0x14dd2b[Math[_0x2cecca(0x183,'A)GK')](_0x14dd2b['length']/0x2)][_0x5cda53(0x19b)]('afterend',_0x7870bb):document[_0x2cecca(0x1ac,'D2jM')](_0x5cda53(0x180))&&document[_0x2cecca(0x175,'TQiO')](_0x5cda53(0x180))[_0x5cda53(0x19b)](_0x2cecca(0x1ab,'G6PT'),_0x7870bb):_0x451f2a['includes'](_0x2cecca(0x169,'bhZf'))?document[_0x2cecca(0x1af,'GXUd')]('.post-body:not(.siki):not(.siki0)\x20p')[_0x451f2a[_0x5cda53(0x188)](_0x5cda53(0x197))[0x1]-0x1]&&document[_0x2cecca(0x16b,'YIJ2')]('.post-body\x20p')[_0x451f2a['split'](_0x5cda53(0x197))[0x1]-0x1][_0x2cecca(0x189,'9HQw')]('afterend',_0x7870bb):_0x451f2a['includes']('ad-h2-')?document[_0x2cecca(0x1b5,'I^3o')](_0x2cecca(0x194,'qLBY'))[_0x451f2a[_0x2cecca(0x18f,'%luT')]('ad-h2-')[0x1]-0x1]&&document[_0x2cecca(0x174,'D2jM')]('.post-body\x20h2')[_0x451f2a[_0x2cecca(0x173,'YIJ2')]('ad-h2-')[0x1]-0x1][_0x2cecca(0x199,'U84E')]('afterend',_0x7870bb):_0x451f2a['includes'](_0x2cecca(0x1ae,'TQiO'))?document[_0x2cecca(0x170,'pvTY')]('.post-body:not(.siki):not(.siki0)\x20h3')[_0x451f2a[_0x2cecca(0x195,'GXUd')]('ad-h3-')[0x1]-0x1]&&document[_0x5cda53(0x1b9)](_0x2cecca(0x1a4,'qLBY'))[_0x451f2a['split'](_0x2cecca(0x1ae,'TQiO'))[0x1]-0x1]['insertAdjacentHTML'](_0x2cecca(0x18c,'$Z(5'),_0x7870bb):_0x451f2a[_0x5cda53(0x1a1)]('ad-h4-')?document[_0x5cda53(0x1b9)]('.post-body:not(.siki):not(.siki0)\x20h4')[_0x451f2a[_0x5cda53(0x188)](_0x2cecca(0x1b2,'NE[R'))[0x1]-0x1]&&document[_0x5cda53(0x1b9)](_0x2cecca(0x182,'GXUd'))[_0x451f2a[_0x2cecca(0x1b4,'U84E')](_0x5cda53(0x18e))[0x1]-0x1]['insertAdjacentHTML'](_0x5cda53(0x196),_0x7870bb):_0x451f2a[_0x2cecca(0x19c,'y8^J')](_0x2cecca(0x1a2,'FfeX'))&&document[_0x5cda53(0x1b9)]('.post-body:not(.siki):not(.siki0)\x20blockquote')[_0x451f2a[_0x5cda53(0x188)](_0x2cecca(0x192,'7yF^'))[0x1]-0x1]&&document[_0x5cda53(0x1b9)]('.post-body\x20blockquote')[_0x451f2a[_0x5cda53(0x188)](_0x2cecca(0x187,'hktA'))[0x1]-0x1][_0x2cecca(0x166,'&s!h')](_0x5cda53(0x196),_0x7870bb);}),_0x390d25(0x1aa,'yssS')==typeof blba&&(document[_0x390d25(0x17a,'yMWU')]['innerHTML']='');}/*]]>*/</b:if></script><b:if cond='data:view.isSingleItem'><script>/*<![CDATA[*/if(Object.entries(AuthorsInfo.postAds).length){document.querySelectorAll('ins.adsbygoogle:empty').forEach(()=>{ (adsbygoogle = window.adsbygoogle || []).push({}); })}/*]]>*/</script></b:if><script>/*<![CDATA[*/_$(".sharemore,.OpenSitting.Inpost,#clicksearch,#navMopile,.link.searcha,.link.menue").forEach(a=>{a.addEventListener("click",function(){_$("body").classList.add("scrolhide")})}),_$(".OpenSitting.inside,.closemenu,.pos-t-t,.searchC,.fCls.sharebg,.c.cl,.fCls.searchbg").forEach(a=>{a.addEventListener("click",function(){_$("body").classList.remove("scrolhide")})});/*]]>*/</script></b:includable>
        <b:includable id='DefaultMeta'>
          <link href='/apple-touch-icon.png' rel='apple-touch-icon'/>
          <b:if cond='data:blog.view == &quot;ReadMode&quot;'><meta content='noindex' name='robots'/></b:if>
          <meta content='text/html; charset=UTF-8' http-equiv='Content-Type'/>
          <meta content='width=device-width, initial-scale=1' name='viewport'/>
          <link expr:href='data:view.url.canonical' rel='canonical'/>
          <meta expr:content='data:view.description.escaped' name='description'/>
          <link expr:href='data:blog.blogspotFaviconUrl' rel='icon' type='image/x-icon'/>
          <meta content='IE=edge' http-equiv='X-UA-Compatible'/>
          <meta content='blogger' name='generator'/>
          <meta expr:content='data:skin.vars.body_background_color' name='theme-color'/>
          <meta expr:content='data:skin.vars.body_background_color' name='msapplication-navbutton-color'/>
          <meta expr:content='data:blog.blogId' name='BlogId'/>
          <b:eval expr='data:blog.openIdOpTag'/>
          <b:if cond='data:view.featuredImage'>
            <link expr:href='data:view.featuredImage' rel='image_src'/>
            <b:else/>&lt;link href=&#39;<b:include name='MetaImage'/>&#39; rel=&#39;image_src&#39;/&gt;
          </b:if>
        </b:includable>
        <b:includable id='OpenGraph'>
          <meta expr:content='data:blog.localeUnderscoreDelimited == &quot;ar&quot; ? &quot;ar_AR&quot; : data:blog.localeUnderscoreDelimited' property='og:locale'/>
          <meta expr:content='data:view.url.canonical' property='og:url'/>
          <meta expr:content='data:view.title.escaped' property='og:title'/>
          <meta expr:content='data:blog.title.escaped' property='og:site_name'/>
          <meta expr:content='data:view.description.escaped' property='og:description'/>
          <meta expr:content='data:view.title.escaped' property='og:image:alt'/>
          <b:if cond='data:view.isMultipleItems'><meta content='website' property='og:type'/>
            <b:elseif cond='data:view.isSingleItem'/><meta content='article' property='og:type'/>
          </b:if>
          <b:if cond='data:view.featuredImage'>
            <meta expr:content='resizeImage(data:view.featuredImage, 1200, &quot;1200:630&quot;)' property='og:image'/>
            <b:else/>&lt;meta content=&#39;<b:include name='MetaImage'/>&#39; property=&#39;og:image&#39;/&gt;</b:if>
        </b:includable>
        <b:includable id='TwitterCard'>
          <meta content='summary_large_image' name='twitter:card'/>
          <meta expr:content='data:blog.homepageUrl' name='twitter:domain'/>
          <meta expr:content='data:view.description.escaped' name='twitter:description'/>
          <meta expr:content='data:view.title.escaped' name='twitter:title'/>
          <b:if cond='data:view.featuredImage'>
            <meta expr:content='resizeImage(data:view.featuredImage, 1200, &quot;1200:630&quot;)' name='twitter:image'/>
            <b:else/>&lt;meta content=&#39;<b:include name='MetaImage'/>&#39; name=&#39;twitter:image&#39;/&gt;</b:if>
        </b:includable>
        <b:includable id='DNSPrefetech'>
          <link expr:href='data:view.url.canonical' rel='dns-prefetch'/><link expr:href='data:view.url.canonical' rel='preconnect'/><link href='https://script.google.com' rel='dns-prefetch'/><link href='https://fonts.gstatic.com' rel='dns-prefetch'/><link href='https://fonts.googleapis.com' rel='dns-prefetch'/><link href='https://1.bp.blogspot.com' rel='dns-prefetch'/><link href='https://2.bp.blogspot.com' rel='dns-prefetch'/><link href='https://3.bp.blogspot.com' rel='dns-prefetch'/><link href='https://4.bp.blogspot.com' rel='dns-prefetch'/><link href='https://blogger.googleusercontent.com' rel='dns-prefetch'/><link href='https://pagead2.googlesyndication.com' rel='dns-prefetch'/><link href='https://pagead2.googlesyndication.com' rel='preconnect'/><link href='https://www.googletagmanager.com/gtag/js' rel='dns-prefetch'/><link href='https://www.googletagmanager.com/gtag/js' rel='preconnect'/>
        </b:includable>
        <b:includable id='BJSPja'><script>/*<![CDATA[*/const _0x552754=_0x4c64;(function(_0x46b569,_0x3858ba){const _0x4296c8=_0x1b33;const _0x577be7=_0x4c64;const _0x50b34b=_0x46b569();while(!![]){try{const _0x16a0cb=-parseInt(_0x577be7(0x148,'JFEG'))/0x1*(parseInt(_0x4296c8(0x11a))/0x2)+parseInt(_0x577be7(0x138,'IATk'))/0x3+-parseInt(_0x577be7(0x118,'WO)E'))/0x4+parseInt(_0x577be7(0x140,'MUSd'))/0x5*(-parseInt(_0x577be7(0x136,'^m!B'))/0x6)+-parseInt(_0x4296c8(0x129))/0x7*(parseInt(_0x4296c8(0x123))/0x8)+parseInt(_0x4296c8(0x139))/0x9+parseInt(_0x577be7(0x131,'hrWG'))/0xa;if(_0x16a0cb===_0x3858ba){break;}else{_0x50b34b['push'](_0x50b34b['shift']());}}catch(_0x432f55){_0x50b34b['push'](_0x50b34b['shift']());}}}(_0x1ed4,0x40e85));function _0x1b33(_0x37270a,_0x283580){const _0x39b171=_0x1ed4();_0x1b33=function(_0x4da02d,_0xb595a3){_0x4da02d=_0x4da02d-0x113;let _0x1ed428=_0x39b171[_0x4da02d];if(_0x1b33['UAhGfv']===undefined){var _0x4c6486=function(_0x47b7c4){const _0x1db8f1='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x37dad0='';let _0x1b33d7='';let _0x1f62f7=_0x37dad0+_0x4c6486;for(let _0x7745c8=0x0,_0x36257c,_0x58f3e1,_0x1106d4=0x0;_0x58f3e1=_0x47b7c4['charAt'](_0x1106d4++);~_0x58f3e1&&(_0x36257c=_0x7745c8%0x4?_0x36257c*0x40+_0x58f3e1:_0x58f3e1,_0x7745c8++%0x4)?_0x37dad0+=_0x1f62f7['charCodeAt'](_0x1106d4+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x36257c>>(-0x2*_0x7745c8&0x6)):_0x7745c8:0x0){_0x58f3e1=_0x1db8f1['indexOf'](_0x58f3e1);}for(let _0x3bf53e=0x0,_0x5cbba6=_0x37dad0['length'];_0x3bf53e<_0x5cbba6;_0x3bf53e++){_0x1b33d7+='%'+('00'+_0x37dad0['charCodeAt'](_0x3bf53e)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x1b33d7);};_0x1b33['aqrrlv']=_0x4c6486;_0x37270a=arguments;_0x1b33['UAhGfv']=!![];}const _0x10f97c=_0x39b171[0x0];const _0x53062b=_0x4da02d+_0x10f97c;const _0x52ae17=_0x37270a[_0x53062b];if(!_0x52ae17){const _0xf43c3f=function(_0x52848c){this['vwntZI']=_0x52848c;this['mmcNIM']=[0x1,0x0,0x0];this['QNJxZa']=function(){return'newState';};this['kjpnCF']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['lSXqPY']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0xf43c3f['prototype']['tZGBZu']=function(){const _0x9f6d36=new RegExp(this['kjpnCF']+this['lSXqPY']);const _0x4da62d=_0x9f6d36['test'](this['QNJxZa']['toString']())?--this['mmcNIM'][0x1]:--this['mmcNIM'][0x0];return this['EbZqAy'](_0x4da62d);};_0xf43c3f['prototype']['EbZqAy']=function(_0x184d5a){if(!Boolean(~_0x184d5a)){return _0x184d5a;}return this['ftSCMA'](this['vwntZI']);};_0xf43c3f['prototype']['ftSCMA']=function(_0x9f0787){for(let _0x151279=0x0,_0x4a6d23=this['mmcNIM']['length'];_0x151279<_0x4a6d23;_0x151279++){this['mmcNIM']['push'](Math['round'](Math['random']()));_0x4a6d23=this['mmcNIM']['length'];}return _0x9f0787(this['mmcNIM'][0x0]);};new _0xf43c3f(_0x1b33)['tZGBZu']();_0x1ed428=_0x1b33['aqrrlv'](_0x1ed428);_0x37270a[_0x53062b]=_0x1ed428;}else{_0x1ed428=_0x52ae17;}return _0x1ed428;};return _0x1b33(_0x37270a,_0x283580);}const _0xb595a3=(function(){let _0x5cbba6=!![];return function(_0xf43c3f,_0x52848c){const _0x9f6d36=_0x5cbba6?function(){const _0x309a17=_0x1b33;if(_0x52848c){const _0x4da62d=_0x52848c[_0x309a17(0x126)](_0xf43c3f,arguments);_0x52848c=null;return _0x4da62d;}}:function(){};_0x5cbba6=![];return _0x9f6d36;};}());const _0x4da02d=_0xb595a3(this,function(){const _0x1045aa=_0x4c64;const _0xcd76ef=_0x1b33;return _0x4da02d[_0xcd76ef(0x125)]()['search'](_0xcd76ef(0x12f))[_0x1045aa(0x13d,'3K3o')]()['constructor'](_0x4da02d)['search'](_0xcd76ef(0x12f));});function _0x1ed4(){const _0x5e1a11=['B3v0zxjive1m','u0HmAw5R','nda2otmYog1Py0PlBa','nte1otK4uwrRBgrQ','Dg9tDhjPBMC','yxbWBhK','rCoIgSk4uCkwhmoQ','qv5PhG','n21PCKjbua','WP9Sz8kq','W6xdHMVdNwn0ea','W6PHW5NcN8ofW6pcS2uAWRZcMhO','W7niW4LLiCk5W4NdLgBcJbldRWFcT8oiWQe','otaZodG4wMvovgv0','kcGOlISPkYKRksSK','AgfZqxr0CMLIDxrL','CvCNxIBdTJFdHmoUAH3dUMDs','u0Hjy29U','AhjLzG','Aw5UzxjuzxH0','DgfYz2v0psjFyMXHBMSI','W5vRWRFdO8oMWQ7dMCkXqa','AmoTDSkeW5ZdLmo9WQxdLSkAySkxyW','hCkhWOuHhdLPWOebbCkaWOm','mZq5mtm3CezPAKrz','wbhcKCoJ','zmohWRJcMSk5W6XIaCkuBfRdJG','W5vrWR4F','AYFdUcPpFmk4W4G','CgfYC2u','fmk/s8kCWOrYg8ojWQSxWPLWW500','W73cTe8VWR/cNCo3W7aUnHH0','jY8+pc9ZDMC+','yNv0Dg9UigXU','q8oOdmoUW5uNqG','qX0UCCo/ht4T','kmorrmoVwK4','tH/dTmkTWODfk8ouW4K','ignSyxnZpsC','zMVcIXNcOJJcVCkMufesgG','FcqOWRmD','uWf2uXZdHCkMgSo2DWtcImoMW6L7WOFdH8k8jSkShmo4wCosW4irW5RdP8onbH5DCJZcIa','vwRdKSk3vdxcS8kAW4rEqK0','pc9HpG','FSo7l8ocWORcHmo4W7m','g0v8kCk5t2mVWRddVmoXWRhdGW','pgeGy2XHC3m9jW','mMj4C1rctG','W6/dOmoWjComlSo0W5K+WOBdHvuTWRW','z2v0qxr0CMLIDxrL','yNv0Dg9U','WRCqW4BdMSoGWPa','WRW0WPtdRCkeWQlcLf42WQxcU2S','mtm4wMLqCurh'];_0x1ed4=function(){return _0x5e1a11;};return _0x1ed4();}function _0x4c64(_0x37270a,_0x283580){const _0x39b171=_0x1ed4();_0x4c64=function(_0x4da02d,_0xb595a3){_0x4da02d=_0x4da02d-0x113;let _0x1ed428=_0x39b171[_0x4da02d];if(_0x4c64['qhdUTk']===undefined){var _0x4c6486=function(_0x1db8f1){const _0x37dad0='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x1b33d7='';let _0x1f62f7='';let _0x7745c8=_0x1b33d7+_0x4c6486;for(let _0x36257c=0x0,_0x58f3e1,_0x1106d4,_0x3bf53e=0x0;_0x1106d4=_0x1db8f1['charAt'](_0x3bf53e++);~_0x1106d4&&(_0x58f3e1=_0x36257c%0x4?_0x58f3e1*0x40+_0x1106d4:_0x1106d4,_0x36257c++%0x4)?_0x1b33d7+=_0x7745c8['charCodeAt'](_0x3bf53e+0xa)-0xa!==0x0?String['fromCharCode'](0xff&_0x58f3e1>>(-0x2*_0x36257c&0x6)):_0x36257c:0x0){_0x1106d4=_0x37dad0['indexOf'](_0x1106d4);}for(let _0x5cbba6=0x0,_0xf43c3f=_0x1b33d7['length'];_0x5cbba6<_0xf43c3f;_0x5cbba6++){_0x1f62f7+='%'+('00'+_0x1b33d7['charCodeAt'](_0x5cbba6)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x1f62f7);};const _0x47b7c4=function(_0x52848c,_0x9f6d36){let _0x4da62d=[],_0x184d5a=0x0,_0x9f0787,_0x151279='';_0x52848c=_0x4c6486(_0x52848c);let _0x4a6d23;for(_0x4a6d23=0x0;_0x4a6d23<0x100;_0x4a6d23++){_0x4da62d[_0x4a6d23]=_0x4a6d23;}for(_0x4a6d23=0x0;_0x4a6d23<0x100;_0x4a6d23++){_0x184d5a=(_0x184d5a+_0x4da62d[_0x4a6d23]+_0x9f6d36['charCodeAt'](_0x4a6d23%_0x9f6d36['length']))%0x100;_0x9f0787=_0x4da62d[_0x4a6d23];_0x4da62d[_0x4a6d23]=_0x4da62d[_0x184d5a];_0x4da62d[_0x184d5a]=_0x9f0787;}_0x4a6d23=0x0;_0x184d5a=0x0;for(let _0x466fa1=0x0;_0x466fa1<_0x52848c['length'];_0x466fa1++){_0x4a6d23=(_0x4a6d23+0x1)%0x100;_0x184d5a=(_0x184d5a+_0x4da62d[_0x4a6d23])%0x100;_0x9f0787=_0x4da62d[_0x4a6d23];_0x4da62d[_0x4a6d23]=_0x4da62d[_0x184d5a];_0x4da62d[_0x184d5a]=_0x9f0787;_0x151279+=String['fromCharCode'](_0x52848c['charCodeAt'](_0x466fa1)^_0x4da62d[(_0x4da62d[_0x4a6d23]+_0x4da62d[_0x184d5a])%0x100]);}return _0x151279;};_0x4c64['YeJWww']=_0x47b7c4;_0x37270a=arguments;_0x4c64['qhdUTk']=!![];}const _0x10f97c=_0x39b171[0x0];const _0x53062b=_0x4da02d+_0x10f97c;const _0x52ae17=_0x37270a[_0x53062b];if(!_0x52ae17){if(_0x4c64['cDWTZv']===undefined){const _0x39d7d9=function(_0x44c709){this['WCqgMr']=_0x44c709;this['rJjJYc']=[0x1,0x0,0x0];this['axbCGy']=function(){return'newState';};this['tAozru']='\x5cw+\x20*\x5c(\x5c)\x20*{\x5cw+\x20*';this['IDKbyY']='[\x27|\x22].+[\x27|\x22];?\x20*}';};_0x39d7d9['prototype']['GXCsJU']=function(){const _0x3086af=new RegExp(this['tAozru']+this['IDKbyY']);const _0xb794f=_0x3086af['test'](this['axbCGy']['toString']())?--this['rJjJYc'][0x1]:--this['rJjJYc'][0x0];return this['qsDjhK'](_0xb794f);};_0x39d7d9['prototype']['qsDjhK']=function(_0x119543){if(!Boolean(~_0x119543)){return _0x119543;}return this['uZsDvp'](this['WCqgMr']);};_0x39d7d9['prototype']['uZsDvp']=function(_0x16b68b){for(let _0x4ab491=0x0,_0xb7fb4e=this['rJjJYc']['length'];_0x4ab491<_0xb7fb4e;_0x4ab491++){this['rJjJYc']['push'](Math['round'](Math['random']()));_0xb7fb4e=this['rJjJYc']['length'];}return _0x16b68b(this['rJjJYc'][0x0]);};new _0x39d7d9(_0x4c64)['GXCsJU']();_0x4c64['cDWTZv']=!![];}_0x1ed428=_0x4c64['YeJWww'](_0x1ed428,_0xb595a3);_0x37270a[_0x53062b]=_0x1ed428;}else{_0x1ed428=_0x52ae17;}return _0x1ed428;};return _0x4c64(_0x37270a,_0x283580);}_0x4da02d();document[_0x552754(0x12d,'(mNy')](_0x552754(0x114,'tp4j'))[_0x552754(0x143,'B#m0')](_0x184d5a=>{const _0x449cd4=_0x552754;const _0xeabfc1=_0x1b33;if(_0x184d5a[_0xeabfc1(0x130)](_0x449cd4(0x13c,'C$v)'))){if(_0x184d5a[_0x449cd4(0x12c,'Egk(')](_0x449cd4(0x13a,'[!cZ'))[_0x449cd4(0x144,'WO)E')]('SHBlock')){let _0x9f0787=JSON[_0xeabfc1(0x13e)](_0x184d5a[_0xeabfc1(0x11c)](_0x449cd4(0x12a,'dKfN'))),_0x151279=_0x184d5a['innerText'];_0x184d5a[_0xeabfc1(0x121)]='<p\x20class=\x27'+_0x9f0787['SHBlock']+'\x27>'+_0x151279+_0x449cd4(0x128,'tp4j');}if(_0x184d5a['getAttribute']('href')['includes'](_0xeabfc1(0x122))){let _0x4a6d23=JSON['parse'](_0x184d5a[_0x449cd4(0x115,'XAQJ')](_0xeabfc1(0x133))),_0x466fa1=_0x4a6d23[_0xeabfc1(0x122)][_0x449cd4(0x127,'hXHk')]('b1')?_0xeabfc1(0x11d):_0xeabfc1(0x142),_0x39d7d9=_0x4a6d23[_0xeabfc1(0x132)]?'<svg><use\x20href=\x27#'+_0x4a6d23[_0x449cd4(0x11e,'^m!B')]+_0xeabfc1(0x141):'',_0x44c709=_0x184d5a[_0xeabfc1(0x130)](_0x449cd4(0x145,'Lh&u'))?_0xeabfc1(0x135):'',_0x3086af=_0x184d5a['hasAttribute']('rel')?_0x449cd4(0x11b,'q@dN'):'',_0xb794f=_0x184d5a[_0xeabfc1(0x134)];_0x184d5a[_0x449cd4(0x146,'$C08')]=_0xeabfc1(0x119)+_0x466fa1+_0x449cd4(0x117,'YB#t')+_0x4a6d23[_0x449cd4(0x113,')8!p')]+'\x27\x20'+_0x44c709+_0x3086af+_0xeabfc1(0x147)+_0x4a6d23['SHLink']+'\x27>'+_0x39d7d9+_0xb794f+_0xeabfc1(0x116);}}});/*]]>*/</script></b:includable>
        <b:includable id='widget-title'>
          <b:if cond='data:widget.sectionId != &quot;PostA3lan&quot; or data:widget.sectionId != &quot;PostA3lan2&quot;'>
            <b:if cond='data:title.length gt 0'><div class='headline' expr:data-title='data:title.escaped'><h2 class='title'><data:title/></h2></div></b:if>
          </b:if>
        </b:includable>
        <b:includable id='Archive'><script>/*<![CDATA[*/
document.querySelector(".post-body .ArchivePage")&&fetch("/feeds/posts/summary?alt=json&max-results=0").then(e=>e.json()).then(e=>{(e=e.feed.category).forEach(e=>{var n='<div class="caregory-div"><h2 class="Category-ArchivePage"><a href="/search/label/'+e.term+'">'+e.term+'</a></h2></div><div class="Sp-posts6 archive"><div class="Posts-byCategory">';fetch("/feeds/posts/summary/-/"+encodeURIComponent(e.term)+"?alt=json").then(e=>e.json()).then(e=>{for(var t=0;t<e.feed.entry.length;t+=1){var s=e.feed.entry[t].link.map(function(e){return e.rel}).indexOf("alternate"),a=e.feed.entry[t].link[s].href,s=e.feed.entry[t].title.$t,r=GetAgo(e.feed.entry[t].updated.$t);-1!==a.indexOf(".blogspot.")&&(a=a.replace("http://","https://")),n+="<div class='posts'><span class='Date'><svg><use href='#ic-clock'></use></svg><a href='"+a+"'>"+r+"</a></span><div class='rnav-title'><a class='ArchivePage-posts' title='"+s+"' href='"+a+"'>"+s+"</a></div></div>"}_$(".ArchivePage").innerHTML+=n+"</div></div>"})})});
/*]]>*/</script></b:includable>
        <b:includable id='MetaImage'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjPvr2DF0wg3DCyxpHGG4sCNqzcXvSQP5UtluUjh4JEYkFGqYshKeO9tNurRneCn9KmZ883Yzhz-bw_w8rzfg5xas6B5s5MOP9kM9ZwbuQaYxpkq7KQo1XzZVPQDC_pzZuhdI9iUNHtWPkU8LMr-AsDibiJOcXwRULfKV3OWqYAYlabIt7Q-oY3YvXduE7W/s16000/%D9%83%D9%88%D8%AA%D8%B4%D9%8A%D9%86%D8%A7.png</b:includable>
        <b:includable id='arrow-up-circle-icon'><svg viewBox='0 0 34 34'><circle class='b' cx='17' cy='17' r='15.92'/><circle class='c scrollProgress' cx='17' cy='17' r='15.92'/><path class='line d' d='M15.07,21.06,19.16,17l-4.09-4.06'/></svg></b:includable>
        <b:includable id='PostSittings'>
          <b:if cond='data:view.isPost'>
            <div class='Sittings'>
              <div class='e3dadat'>
                <div class='OpenSitting inside' onclick='Togsit()'/>
                <div class='addAndMin FontSize'><span><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>Font Size<b:else/>حجم الخط</b:if></span>
                  <div class='AddNumper'>+</div>
                  <div class='NowNumper'><span>16</span></div>
                  <div class='MinNumper'>-</div>
                </div>
                <div class='addAndMin LineHeight'>
                  <span><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>lines height<b:else/>تباعد السطور</b:if></span>
                  <div class='AddNumper'>+</div>
                  <div class='NowNumper'><span>2</span></div>
                  <div class='MinNumper enf'>-</div>
                </div>
              </div>
            </div>
            <script>/*<![CDATA[*/
function Togsit(){_$(".Sittings").classList.toggle("OPen")}var postbdy=document.querySelector(".post-body");function removeStyle(){document.querySelectorAll(".post-body *").forEach(function(a){a.removeAttribute("style")})}var fLineHeight=document.querySelector(".LineHeight"),fLtextSizenum=fLineHeight.querySelector(".NowNumper span"),fLTextSize=parseInt(fLtextSizenum.innerText),fLAddmore=fLineHeight.querySelector(".AddNumper"),fLlosemore=fLineHeight.querySelector(".MinNumper");fLAddmore.addEventListener("click",function(){4>fLTextSize?(fLTextSize+=1,postbdy.style.lineHeight=fLTextSize+"em",fLtextSizenum.innerText=fLTextSize,fLlosemore.classList.remove("enf"),fLAddmore.classList.remove("enf")):fLAddmore.classList.add("enf")}),fLlosemore.addEventListener("click",function(){2<fLTextSize?(--fLTextSize,postbdy.style.lineHeight=fLTextSize+"em",fLtextSizenum.innerText=fLTextSize,fLlosemore.classList.remove("enf"),fLAddmore.classList.remove("enf")):fLlosemore.classList.add("enf")});var fFontSize=document.querySelector(".FontSize"),fFtextSizenum=fFontSize.querySelector(".NowNumper span"),fFTextSize=parseInt(fFtextSizenum.innerText),fFAddmore=fFontSize.querySelector(".AddNumper"),fFlosemore=fFontSize.querySelector(".MinNumper");fFAddmore.addEventListener("click",function(){removeStyle(),29>fFTextSize?(fFTextSize+=1,postbdy.style.fontSize=fFTextSize+"px",fFtextSizenum.innerText=fFTextSize,fFlosemore.classList.remove("enf"),fFAddmore.classList.remove("enf")):fFAddmore.classList.add("enf")}),fFlosemore.addEventListener("click",function(){removeStyle(),14<fFTextSize?(--fFTextSize,postbdy.style.fontSize=fFTextSize+"px",fFtextSizenum.innerText=fFTextSize,fFlosemore.classList.remove("enf"),fFAddmore.classList.remove("enf")):fFlosemore.classList.add("enf")});
/*]]>*/
            </script>
          </b:if>
        </b:includable> 
        <b:includable id='mopilemenu'>
<label aria-label='Home' class='link homee' data-text='Home'><a expr:href='data:blog.homepageUrl' title='القائمة الرئيسية'><svg class='line home'><use href='#ic-home'/></svg></a></label>
                    <label aria-label='Menu' class='link menue' data-text='Menu' for='NavM' onclick='openSidenav()'><svg class='line linedd'><use href='#ic-menu'/></svg></label>
          <label aria-label='GoTop' class='link scroltop' data-text='GoTop' onclick='window.scrollTo({top: 0});'><svg class='line'><use href='#ic-top'/></svg></label>
          <b:if cond='data:skin.vars.disapledarck == &quot;1px&quot;'><label aria-label='Dark' class='link dark-link' data-text='Dark' onclick='darkMode()'><svg class='line linedd'><use href='#ic-moon-sun'/></svg></label></b:if>
        </b:includable>
        <b:includable id='themeIcons'>

          <symbol id='ic-settings' viewBox='0 0 512 512'><path d='M495.9 166.6c3.2 8.7 .5 18.4-6.4 24.6l-43.3 39.4c1.1 8.3 1.7 16.8 1.7 25.4s-.6 17.1-1.7 25.4l43.3 39.4c6.9 6.2 9.6 15.9 6.4 24.6c-4.4 11.9-9.7 23.3-15.8 34.3l-4.7 8.1c-6.6 11-14 21.4-22.1 31.2c-5.9 7.2-15.7 9.6-24.5 6.8l-55.7-17.7c-13.4 10.3-28.2 18.9-44 25.4l-12.5 57.1c-2 9.1-9 16.3-18.2 17.8c-13.8 2.3-28 3.5-42.5 3.5s-28.7-1.2-42.5-3.5c-9.2-1.5-16.2-8.7-18.2-17.8l-12.5-57.1c-15.8-6.5-30.6-15.1-44-25.4L83.1 425.9c-8.8 2.8-18.6 .3-24.5-6.8c-8.1-9.8-15.5-20.2-22.1-31.2l-4.7-8.1c-6.1-11-11.4-22.4-15.8-34.3c-3.2-8.7-.5-18.4 6.4-24.6l43.3-39.4C64.6 273.1 64 264.6 64 256s.6-17.1 1.7-25.4L22.4 191.2c-6.9-6.2-9.6-15.9-6.4-24.6c4.4-11.9 9.7-23.3 15.8-34.3l4.7-8.1c6.6-11 14-21.4 22.1-31.2c5.9-7.2 15.7-9.6 24.5-6.8l55.7 17.7c13.4-10.3 28.2-18.9 44-25.4l12.5-57.1c2-9.1 9-16.3 18.2-17.8C227.3 1.2 241.5 0 256 0s28.7 1.2 42.5 3.5c9.2 1.5 16.2 8.7 18.2 17.8l12.5 57.1c15.8 6.5 30.6 15.1 44 25.4l55.7-17.7c8.8-2.8 18.6-.3 24.5 6.8c8.1 9.8 15.5 20.2 22.1 31.2l4.7 8.1c6.1 11 11.4 22.4 15.8 34.3zM256 336c44.2 0 80-35.8 80-80s-35.8-80-80-80s-80 35.8-80 80s35.8 80 80 80z'/></symbol>

          <symbol id='ic-clock' viewBox='0 0 512 512'><path d='M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm0 448c-110.5 0-200-89.5-200-200S145.5 56 256 56s200 89.5 200 200-89.5 200-200 200zm61.8-104.4l-84.9-61.7c-3.1-2.3-4.9-5.9-4.9-9.7V116c0-6.6 5.4-12 12-12h32c6.6 0 12 5.4 12 12v141.7l66.8 48.6c5.4 3.9 6.5 11.4 2.6 16.8L334.6 349c-3.9 5.3-11.4 6.5-16.8 2.6z'/></symbol>
          <symbol id='ic-facebook' viewBox='0 0 64 64'><path d='M20.1,36h3.4c0.3,0,0.6,0.3,0.6,0.6V58c0,1.1,0.9,2,2,2h7.8c1.1,0,2-0.9,2-2V36.6c0-0.3,0.3-0.6,0.6-0.6h5.6 c1,0,1.9-0.7,2-1.7l1.3-7.8c0.2-1.2-0.8-2.4-2-2.4h-6.6c-0.5,0-0.9-0.4-0.9-0.9v-5c0-1.3,0.7-2,2-2h5.9c1.1,0,2-0.9,2-2V6.2 c0-1.1-0.9-2-2-2h-7.1c-13,0-12.7,10.5-12.7,12v7.3c0,0.3-0.3,0.6-0.6,0.6h-3.4c-1.1,0-2,0.9-2,2v7.8C18.1,35.1,19,36,20.1,36z'/></symbol>
          <symbol id='ic-paypal' viewBox='0 0 384 512'><path d='M111.4 295.9c-3.5 19.2-17.4 108.7-21.5 134-.3 1.8-1 2.5-3 2.5H12.3c-7.6 0-13.1-6.6-12.1-13.9L58.8 46.6c1.5-9.6 10.1-16.9 20-16.9 152.3 0 165.1-3.7 204 11.4 60.1 23.3 65.6 79.5 44 140.3-21.5 62.6-72.5 89.5-140.1 90.3-43.4.7-69.5-7-75.3 24.2zM357.1 152c-1.8-1.3-2.5-1.8-3 1.3-2 11.4-5.1 22.5-8.8 33.6-39.9 113.8-150.5 103.9-204.5 103.9-6.1 0-10.1 3.3-10.9 9.4-22.6 140.4-27.1 169.7-27.1 169.7-1 7.1 3.5 12.9 10.6 12.9h63.5c8.6 0 15.7-6.3 17.4-14.9.7-5.4-1.1 6.1 14.4-91.3 4.6-22 14.3-19.7 29.3-19.7 71 0 126.4-28.8 142.9-112.3 6.5-34.8 4.6-71.4-23.8-92.6z'/></symbol>
          <symbol id='ic-linkedin' viewBox='0 0 448 512'><path d='M100.28 448H7.4V148.9h92.88zM53.79 108.1C24.09 108.1 0 83.5 0 53.8a53.79 53.79 0 0 1 107.58 0c0 29.7-24.1 54.3-53.79 54.3zM447.9 448h-92.68V302.4c0-34.7-.7-79.2-48.29-79.2-48.29 0-55.69 37.7-55.69 76.7V448h-92.78V148.9h89.08v40.8h1.3c12.4-23.5 42.69-48.3 87.88-48.3 94 0 111.28 61.9 111.28 142.3V448z'/></symbol>
          <symbol id='ic-twitter' viewBox='0 0 64 64'><path d='M11.4,26.6C11.5,26.6,11.5,26.6,11.4,26.6c-0.9,0-1.8-0.2-2.6-0.4c-1.3-0.4-2.5,0.8-2.1,2 c1.1,4.3,4.5,7.7,8.8,8.6c-1,0.3-2,0.4-3,0.4c-1,0-1.7,1.1-1.2,2c1.9,3.5,5.6,5.9,9.7,6h1c1.1,0,2,0.9,2,2c0,1.1-0.9,2-2,2 c-1.3,0-2.9-0.1-4.5-0.5c-1-0.2-2-0.2-2.9,0.1c-1.7,0.6-3.5,1.1-5.4,1.3C8.5,50.2,8,50.7,8,51.4v0c0,0.5,0.3,1,0.8,1.2 c3.9,1.7,8.3,2.7,12.9,2.7c21.1,0,32.7-17.9,32.7-33.5v0c0-0.9,0.4-1.8,1.1-2.4c1.2-1,2.3-2.1,3.3-3.4c0.4-0.5-0.1-1.2-0.7-1 c-1.2,0.4-2.4,0.7-3.7,0.9c-0.2,0-0.3-0.2-0.1-0.4c1.5-1.1,2.8-2.6,3.6-4.3c0.3-0.6-0.3-1.2-0.9-0.9c-1.1,0.6-2.3,1-3.5,1.4 c-1.2,0.4-2.6,0.1-3.6-0.7c-1.9-1.5-4.4-2.4-7-2.4c-5.3,0-9.8,3.7-11.1,8.8c-0.2,0.9,0.5,1.7,1.4,1.7c1.6-0.1,3.2-0.3,4.4-0.5 c1-0.2,2,0.3,2.4,1.2c0.5,1.2-0.2,2.4-1.3,2.7c-4.6,1.3-9.7,0.4-9.7,0.4l0,0C21.2,21.8,14.3,18,9.3,12.5C8.6,11.7,7.3,12,7,12.9 c-0.4,1.2-0.6,2.5-0.6,3.9C6.4,20.9,8.4,24.5,11.4,26.6z'/></symbol>
          <symbol id='ic-telegram' viewBox='0 0 64 64'><path d='M56.4,8.2l-51.2,20c-1.7,0.6-1.6,3,0.1,3.5l9.7,2.9c2.1,0.6,3.8,2.2,4.4,4.3l3.8,12.1c0.5,1.6,2.5,2.1,3.7,0.9 l5.2-5.3c0.9-0.9,2.2-1,3.2-0.3l11.5,8.4c1.6,1.2,3.9,0.3,4.3-1.7l8.7-41.8C60.4,9.1,58.4,7.4,56.4,8.2z M50,17.4L29.4,35.6 c-1.1,1-1.9,2.4-2,3.9c-0.2,1.5-2.3,1.7-2.8,0.3l-0.9-3c-0.7-2.2,0.2-4.5,2.1-5.7l23.5-14.6C49.9,16.1,50.5,16.9,50,17.4z'/></symbol>
          <symbol id='ic-moon-sun' viewBox='0 0 512 512'><g class='d1'><path d='M32 256c0-123.8 100.3-224 223.8-224c11.36 0 29.7 1.668 40.9 3.746c9.616 1.777 11.75 14.63 3.279 19.44C245 86.5 211.2 144.6 211.2 207.8c0 109.7 99.71 193 208.3 172.3c9.561-1.805 16.28 9.324 10.11 16.95C387.9 448.6 324.8 480 255.8 480C132.1 480 32 379.6 32 256z'/></g><g class='d2'><path d='M120.2 154.2c4.672 4.688 10.83 7.031 16.97 7.031S149.5 158.9 154.2 154.2c9.375-9.375 9.375-24.56 0-33.93L108.9 74.97c-9.344-9.375-24.56-9.375-33.94 0s-9.375 24.56 0 33.94L120.2 154.2zM256 112c13.25 0 24-10.75 24-24v-64C280 10.75 269.3 0 256 0S232 10.75 232 24v64C232 101.3 242.8 112 256 112zM112 256c0-13.25-10.75-24-24-24h-64C10.75 232 0 242.8 0 256s10.75 24 24 24h64C101.3 280 112 269.3 112 256zM374.8 161.2c6.141 0 12.3-2.344 16.97-7.031l45.25-45.28c9.375-9.375 9.375-24.56 0-33.94s-24.59-9.375-33.94 0l-45.25 45.28c-9.375 9.375-9.375 24.56 0 33.93C362.5 158.9 368.7 161.2 374.8 161.2zM256 400c-13.25 0-24 10.75-24 24v64C232 501.3 242.8 512 256 512s24-10.75 24-24v-64C280 410.8 269.3 400 256 400zM120.2 357.8l-45.25 45.28c-9.375 9.375-9.375 24.56 0 33.94c4.688 4.688 10.83 7.031 16.97 7.031s12.3-2.344 16.97-7.031l45.25-45.28c9.375-9.375 9.375-24.56 0-33.93S129.6 348.4 120.2 357.8zM488 232h-64c-13.25 0-24 10.75-24 24s10.75 24 24 24h64C501.3 280 512 269.3 512 256S501.3 232 488 232zM391.8 357.8c-9.344-9.375-24.56-9.372-33.94 .0031s-9.375 24.56 0 33.93l45.25 45.28c4.672 4.688 10.83 7.031 16.97 7.031s12.28-2.344 16.97-7.031c9.375-9.375 9.375-24.56 0-33.94L391.8 357.8zM256 144C194.1 144 144 194.1 144 256c0 61.86 50.14 112 112 112s112-50.14 112-112C368 194.1 317.9 144 256 144z'/></g></symbol>
          <symbol id='ic-alt-share' viewBox='0 0 448 512'><path d='M352 224c53 0 96-43 96-96s-43-96-96-96s-96 43-96 96c0 4 .2 8 .7 11.9l-94.1 47C145.4 170.2 121.9 160 96 160c-53 0-96 43-96 96s43 96 96 96c25.9 0 49.4-10.2 66.6-26.9l94.1 47c-.5 3.9-.7 7.8-.7 11.9c0 53 43 96 96 96s96-43 96-96s-43-96-96-96c-25.9 0-49.4 10.2-66.6 26.9l-94.1-47c.5-3.9 .7-7.8 .7-11.9s-.2-8-.7-11.9l94.1-47C302.6 213.8 326.1 224 352 224z'/></symbol>
          <symbol id='ic-share' viewBox='0 0 448 512'><path d='M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H192V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H400c17.7 0 32-14.3 32-32s-14.3-32-32-32H256V80z'/></symbol>
          <symbol id='ic-home' viewBox='0 0 576 512'><path d='M575.8 255.5C575.8 273.5 560.8 287.6 543.8 287.6H511.8L512.5 447.7C512.5 450.5 512.3 453.1 512 455.8V472C512 494.1 494.1 512 472 512H456C454.9 512 453.8 511.1 452.7 511.9C451.3 511.1 449.9 512 448.5 512H392C369.9 512 352 494.1 352 472V384C352 366.3 337.7 352 320 352H256C238.3 352 224 366.3 224 384V472C224 494.1 206.1 512 184 512H128.1C126.6 512 125.1 511.9 123.6 511.8C122.4 511.9 121.2 512 120 512H104C81.91 512 64 494.1 64 472V360C64 359.1 64.03 358.1 64.09 357.2V287.6H32.05C14.02 287.6 0 273.5 0 255.5C0 246.5 3.004 238.5 10.01 231.5L266.4 8.016C273.4 1.002 281.4 0 288.4 0C295.4 0 303.4 2.004 309.5 7.014L564.8 231.5C572.8 238.5 576.9 246.5 575.8 255.5L575.8 255.5z'/></symbol>
          <symbol id='ic-menu' viewBox='0 0 448 512'><path d='M192 176C192 202.5 170.5 224 144 224H48C21.49 224 0 202.5 0 176V80C0 53.49 21.49 32 48 32H144C170.5 32 192 53.49 192 80V176zM192 432C192 458.5 170.5 480 144 480H48C21.49 480 0 458.5 0 432V336C0 309.5 21.49 288 48 288H144C170.5 288 192 309.5 192 336V432zM256 80C256 53.49 277.5 32 304 32H400C426.5 32 448 53.49 448 80V176C448 202.5 426.5 224 400 224H304C277.5 224 256 202.5 256 176V80zM448 432C448 458.5 426.5 480 400 480H304C277.5 480 256 458.5 256 432V336C256 309.5 277.5 288 304 288H400C426.5 288 448 309.5 448 336V432z'/></symbol>
          <symbol id='ic-top' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-180.000000) translate(-12.000000, -12.000000) translate(5.000000, 8.500000)'><path d='M14,0 C14,0 9.856,7 7,7 C4.145,7 0,0 0,0'/></g></symbol>
          <symbol id='ic-line' viewBox='0 0 24 24'><path d='M19.365 9.863c.349 0 .63.285.63.631 0 .345-.281.63-.63.63H17.61v1.125h1.755c.349 0 .63.283.63.63 0 .344-.281.629-.63.629h-2.386c-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.63-.63h2.386c.346 0 .627.285.627.63 0 .349-.281.63-.63.63H17.61v1.125h1.755zm-3.855 3.016c0 .27-.174.51-.432.596-.064.021-.133.031-.199.031-.211 0-.391-.09-.51-.25l-2.443-3.317v2.94c0 .344-.279.629-.631.629-.346 0-.626-.285-.626-.629V8.108c0-.27.173-.51.43-.595.06-.023.136-.033.194-.033.195 0 .375.104.495.254l2.462 3.33V8.108c0-.345.282-.63.63-.63.345 0 .63.285.63.63v4.771zm-5.741 0c0 .344-.282.629-.631.629-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.63-.63.346 0 .628.285.628.63v4.771zm-2.466.629H4.917c-.345 0-.63-.285-.63-.629V8.108c0-.345.285-.63.63-.63.348 0 .63.285.63.63v4.141h1.756c.348 0 .629.283.629.63 0 .344-.282.629-.629.629M24 10.314C24 4.943 18.615.572 12 .572S0 4.943 0 10.314c0 4.811 4.27 8.842 10.035 9.608.391.082.923.258 1.058.59.12.301.079.766.038 1.08l-.164 1.02c-.045.301-.24 1.186 1.049.645 1.291-.539 6.916-4.078 9.436-6.975C23.176 14.393 24 12.458 24 10.314'/></symbol>
          <symbol id='ic-tumblr' viewBox='0 0 32 32'><path d='M16,2A14,14,0,1,0,30,16,14,14,0,0,0,16,2Zm0,26A12,12,0,1,1,28,16,12,12,0,0,1,16,28Z'/><path class='svgC' d='M20,19a1,1,0,0,0-1,1,1,1,0,0,1-1,1H17a1,1,0,0,1-1-1V15h3a1,1,0,0,0,0-2H16V10a1,1,0,0,0-2,0v3H12a1,1,0,0,0,0,2h2v5a3,3,0,0,0,3,3h1a3,3,0,0,0,3-3A1,1,0,0,0,20,19Z'/></symbol>
          <symbol id='ic-youtube' viewBox='0 0 576 512'><path d='M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z'/></symbol>
          <symbol id='ic-whatsapp' viewBox='0 0 64 64'><path d='M6.9,48.4c-0.4,1.5-0.8,3.3-1.3,5.2c-0.7,2.9,1.9,5.6,4.8,4.8l5.1-1.3c1.7-0.4,3.5-0.2,5.1,0.5 c4.7,2.1,10,3,15.6,2.1c12.3-1.9,22-11.9,23.5-24.2C62,17.3,46.7,2,28.5,4.2C16.2,5.7,6.2,15.5,4.3,27.8c-0.8,5.6,0,10.9,2.1,15.6 C7.1,44.9,7.3,46.7,6.9,48.4z M21.3,19.8c0.6-0.5,1.4-0.9,1.8-0.9s2.3-0.2,2.9,1.2c0.6,1.4,2,4.7,2.1,5.1c0.2,0.3,0.3,0.7,0.1,1.2 c-0.2,0.5-0.3,0.7-0.7,1.1c-0.3,0.4-0.7,0.9-1,1.2c-0.3,0.3-0.7,0.7-0.3,1.4c0.4,0.7,1.8,2.9,3.8,4.7c2.6,2.3,4.9,3,5.5,3.4 c0.7,0.3,1.1,0.3,1.5-0.2c0.4-0.5,1.7-2,2.2-2.7c0.5-0.7,0.9-0.6,1.6-0.3c0.6,0.2,4,1.9,4.7,2.2c0.7,0.3,1.1,0.5,1.3,0.8 c0.2,0.3,0.2,1.7-0.4,3.2c-0.6,1.6-2.1,3.1-3.2,3.5c-1.3,0.5-2.8,0.7-9.3-1.9c-7-2.8-11.8-9.8-12.1-10.3c-0.3-0.5-2.8-3.7-2.8-7.1 C18.9,22.1,20.7,20.4,21.3,19.8z'/></symbol>
          <symbol id='ic-pinterest' viewBox='0 0 64 64'><path d='M14.4,53.8c2.4,2,6.1,0.6,6.8-2.4l0-0.1c0.4-1.8,2.4-10.2,3.2-13.7c0.2-0.9,0.2-1.8-0.1-2.7 C24.2,34,24,32.8,24,31.5c0-4.1,2.4-7.2,5.4-7.2c2.5,0,3.8,1.9,3.8,4.2c0,2.6-1.6,6.4-2.5,9.9c-0.7,3,1.5,5.4,4.4,5.4 c5.3,0,8.9-6.8,8.9-14.9c0-6.1-4.1-10.7-11.6-10.7c-8.5,0-13.8,6.3-13.8,13.4c0,2.4,0.7,4.2,1.8,5.5c0.5,0.6,0.6,0.9,0.4,1.6 c-0.1,0.5-0.4,1.8-0.6,2.2c-0.2,0.7-0.8,1-1.4,0.7c-3.9-1.6-5.7-5.9-5.7-10.7c0-8,6.7-17.5,20-17.5c10.7,0,17.7,7.7,17.7,16 c0,11-6.1,19.2-15.1,19.2c-1.9,0-3.8-0.7-5.2-1.6c-0.9-0.6-2.1-0.1-2.4,0.9c-0.5,1.9-1.1,4.3-1.3,4.9c-0.1,0.5-0.3,0.9-0.4,1.4 c-1,2.7,0.9,5.5,3.7,5.7c2.1,0.1,4.2,0,6.3-0.3c12.4-2,22.1-12.2,23.4-24.7C61.5,18.1,48.4,4,32,4C16.5,4,4,16.5,4,32 C4,40.8,8.1,48.6,14.4,53.8z'/></symbol>
          <symbol id='ic-email' viewBox='0 0 500 500'><path d='M468.051,222.657c0-12.724-5.27-24.257-13.717-32.527 L282.253,45.304c-17.811-17.807-46.702-17.807-64.505,0L45.666,190.129c-8.448,8.271-13.717,19.803-13.717,32.527v209.054 c0,20.079,16.264,36.341,36.34,36.341h363.421c20.078,0,36.34-16.262,36.34-36.341V222.657z M124.621,186.402h250.758 c11.081,0,19.987,8.905,19.987,19.991v34.523c-0.088,4.359-1.818,8.631-5.181,11.997l-55.966,56.419l83.224,83.127 c6.904,6.904,6.904,18.081,0,24.985s-18.085,6.904-24.985,0l-85.676-85.672H193.034l-85.492,85.672 c-6.907,6.904-18.081,6.904-24.985,0c-6.906-6.904-6.906-18.081,0-24.985l83.131-83.127l-55.875-56.419 c-3.638-3.638-5.363-8.358-5.181-13.177v-33.343C104.632,195.307,113.537,186.402,124.621,186.402z'/></symbol>
          <symbol id='ic-tag' viewBox='0 0 512 512'><path d='M0 252.118V48C0 21.49 21.49 0 48 0h204.118a48 48 0 0 1 33.941 14.059l211.882 211.882c18.745 18.745 18.745 49.137 0 67.882L293.823 497.941c-18.745 18.745-49.137 18.745-67.882 0L14.059 286.059A48 48 0 0 1 0 252.118zM112 64c-26.51 0-48 21.49-48 48s21.49 48 48 48 48-21.49 48-48-21.49-48-48-48z'/></symbol>
          <symbol id='ic-comment' viewBox='0 0 512 512'><path d='M448 0H64C28.7 0 0 28.7 0 64v288c0 35.3 28.7 64 64 64h96v84c0 9.8 11.2 15.5 19.1 9.7L304 416h144c35.3 0 64-28.7 64-64V64c0-35.3-28.7-64-64-64z'/></symbol>
          <symbol id='ic-search' viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><circle cx='9.76659044' cy='9.76659044' r='8.9885584'/><line x1='16.0183067' x2='19.5423342' y1='16.4851259' y2='20.0000001'/></g></symbol>
          <symbol id='ic-behance' viewBox='0 0 576 512'><path d='M232 237.2c31.8-15.2 48.4-38.2 48.4-74 0-70.6-52.6-87.8-113.3-87.8H0v354.4h171.8c64.4 0 124.9-30.9 124.9-102.9 0-44.5-21.1-77.4-64.7-89.7zM77.9 135.9H151c28.1 0 53.4 7.9 53.4 40.5 0 30.1-19.7 42.2-47.5 42.2h-79v-82.7zm83.3 233.7H77.9V272h84.9c34.3 0 56 14.3 56 50.6 0 35.8-25.9 47-57.6 47zm358.5-240.7H376V94h143.7v34.9zM576 305.2c0-75.9-44.4-139.2-124.9-139.2-78.2 0-131.3 58.8-131.3 135.8 0 79.9 50.3 134.7 131.3 134.7 61.3 0 101-27.6 120.1-86.3H509c-6.7 21.9-34.3 33.5-55.7 33.5-41.3 0-63-24.2-63-65.3h185.1c.3-4.2.6-8.7.6-13.2zM390.4 274c2.3-33.7 24.7-54.8 58.5-54.8 35.4 0 53.2 20.8 56.2 54.8H390.4z'/></symbol>
          <symbol id='ic-flickr' viewBox='0 0 448 512'><path d='M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zM144.5 319c-35.1 0-63.5-28.4-63.5-63.5s28.4-63.5 63.5-63.5 63.5 28.4 63.5 63.5-28.4 63.5-63.5 63.5zm159 0c-35.1 0-63.5-28.4-63.5-63.5s28.4-63.5 63.5-63.5 63.5 28.4 63.5 63.5-28.4 63.5-63.5 63.5z'/></symbol>
          <symbol id='ic-blogger' viewBox='0 0 448 512'><path d='M446.6 222.7c-1.8-8-6.8-15.4-12.5-18.5-1.8-1-13-2.2-25-2.7-20.1-.9-22.3-1.3-28.7-5-10.1-5.9-12.8-12.3-12.9-29.5-.1-33-13.8-63.7-40.9-91.3-19.3-19.7-40.9-33-65.5-40.5-5.9-1.8-19.1-2.4-63.3-2.9-69.4-.8-84.8.6-108.4 10C45.9 59.5 14.7 96.1 3.3 142.9 1.2 151.7.7 165.8.2 246.8c-.6 101.5.1 116.4 6.4 136.5 15.6 49.6 59.9 86.3 104.4 94.3 14.8 2.7 197.3 3.3 216 .8 32.5-4.4 58-17.5 81.9-41.9 17.3-17.7 28.1-36.8 35.2-62.1 4.9-17.6 4.5-142.8 2.5-151.7zm-322.1-63.6c7.8-7.9 10-8.2 58.8-8.2 43.9 0 45.4.1 51.8 3.4 9.3 4.7 13.4 11.3 13.4 21.9 0 9.5-3.8 16.2-12.3 21.6-4.6 2.9-7.3 3.1-50.3 3.3-26.5.2-47.7-.4-50.8-1.2-16.6-4.7-22.8-28.5-10.6-40.8zm191.8 199.8l-14.9 2.4-77.5.9c-68.1.8-87.3-.4-90.9-2-7.1-3.1-13.8-11.7-14.9-19.4-1.1-7.3 2.6-17.3 8.2-22.4 7.1-6.4 10.2-6.6 97.3-6.7 89.6-.1 89.1-.1 97.6 7.8 12.1 11.3 9.5 31.2-4.9 39.4z'/></symbol>
          <symbol id='ic-wordpress' viewBox='0 0 512 512'><path d='M256 8C119.3 8 8 119.2 8 256c0 136.7 111.3 248 248 248s248-111.3 248-248C504 119.2 392.7 8 256 8zM33 256c0-32.3 6.9-63 19.3-90.7l106.4 291.4C84.3 420.5 33 344.2 33 256zm223 223c-21.9 0-43-3.2-63-9.1l66.9-194.4 68.5 187.8c.5 1.1 1 2.1 1.6 3.1-23.1 8.1-48 12.6-74 12.6zm30.7-327.5c13.4-.7 25.5-2.1 25.5-2.1 12-1.4 10.6-19.1-1.4-18.4 0 0-36.1 2.8-59.4 2.8-21.9 0-58.7-2.8-58.7-2.8-12-.7-13.4 17.7-1.4 18.4 0 0 11.4 1.4 23.4 2.1l34.7 95.2L200.6 393l-81.2-241.5c13.4-.7 25.5-2.1 25.5-2.1 12-1.4 10.6-19.1-1.4-18.4 0 0-36.1 2.8-59.4 2.8-4.2 0-9.1-.1-14.4-.3C109.6 73 178.1 33 256 33c58 0 110.9 22.2 150.6 58.5-1-.1-1.9-.2-2.9-.2-21.9 0-37.4 19.1-37.4 39.6 0 18.4 10.6 33.9 21.9 52.3 8.5 14.8 18.4 33.9 18.4 61.5 0 19.1-7.3 41.2-17 72.1l-22.2 74.3-80.7-239.6zm81.4 297.2l68.1-196.9c12.7-31.8 17-57.2 17-79.9 0-8.2-.5-15.8-1.5-22.9 17.4 31.8 27.3 68.2 27.3 107 0 82.3-44.6 154.1-110.9 192.7z'/></symbol>
          <symbol id='ic-blog' viewBox='0 0 512 512'><path d='M217.6 96.1c-12.95-.625-24.66 9.156-25.52 22.37C191.2 131.7 201.2 143.1 214.4 143.1c79.53 5.188 148.4 74.09 153.6 153.6c.8281 12.69 11.39 22.43 23.94 22.43c.5156 0 1.047-.0313 1.578-.0625c13.22-.8438 23.25-12.28 22.39-25.5C409.3 191.8 320.3 102.8 217.6 96.1zM224 0C206.3 0 192 14.31 192 32s14.33 32 32 32c123.5 0 224 100.5 224 224c0 17.69 14.33 32 32 32s32-14.31 32-32C512 129.2 382.8 0 224 0zM172.3 226.8C157.7 223.9 144 235.8 144 250.6v50.37c0 10.25 7.127 18.37 16.75 21.1c18.13 6.75 31.26 24.38 31.26 44.1c0 26.5-21.5 47.1-48.01 47.1c-26.5 0-48.01-21.5-48.01-47.1V120c0-13.25-10.75-23.1-24.01-23.1l-48.01 .0076C10.75 96.02 0 106.8 0 120v247.1c0 89.5 82.14 160.2 175 140.7c54.38-11.5 98.27-55.5 109.8-109.7C302.2 316.1 247.8 241.8 172.3 226.8z'/></symbol>
          <symbol id='ic-skype' viewBox='0 0 448 512'><path d='M424.7 299.8c2.9-14 4.7-28.9 4.7-43.8 0-113.5-91.9-205.3-205.3-205.3-14.9 0-29.7 1.7-43.8 4.7C161.3 40.7 137.7 32 112 32 50.2 32 0 82.2 0 144c0 25.7 8.7 49.3 23.3 68.2-2.9 14-4.7 28.9-4.7 43.8 0 113.5 91.9 205.3 205.3 205.3 14.9 0 29.7-1.7 43.8-4.7 19 14.6 42.6 23.3 68.2 23.3 61.8 0 112-50.2 112-112 .1-25.6-8.6-49.2-23.2-68.1zm-194.6 91.5c-65.6 0-120.5-29.2-120.5-65 0-16 9-30.6 29.5-30.6 31.2 0 34.1 44.9 88.1 44.9 25.7 0 42.3-11.4 42.3-26.3 0-18.7-16-21.6-42-28-62.5-15.4-117.8-22-117.8-87.2 0-59.2 58.6-81.1 109.1-81.1 55.1 0 110.8 21.9 110.8 55.4 0 16.9-11.4 31.8-30.3 31.8-28.3 0-29.2-33.5-75-33.5-25.7 0-42 7-42 22.5 0 19.8 20.8 21.8 69.1 33 41.4 9.3 90.7 26.8 90.7 77.6 0 59.1-57.1 86.5-112 86.5z'/></symbol>
          <symbol id='ic-instagram' viewBox='0 0 448 512'><path d='M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z'/></symbol>
          <symbol id='ic-google-play' viewBox='0 0 512 512'><path d='M325.3 234.3L104.6 13l280.8 161.2-60.1 60.1zM47 0C34 6.8 25.3 19.2 25.3 35.3v441.3c0 16.1 8.7 28.5 21.7 35.3l256.6-256L47 0zm425.2 225.6l-58.9-34.1-65.7 64.5 65.7 64.5 60.1-34.1c18-14.3 18-46.5-1.2-60.8zM104.6 499l280.8-161.2-60.1-60.1L104.6 499z'/></symbol>
          <symbol id='ic-reddit' viewBox='0 0 512 512'><path d='M201.5 305.5c-13.8 0-24.9-11.1-24.9-24.6 0-13.8 11.1-24.9 24.9-24.9 13.6 0 24.6 11.1 24.6 24.9 0 13.6-11.1 24.6-24.6 24.6zM504 256c0 137-111 248-248 248S8 393 8 256 119 8 256 8s248 111 248 248zm-132.3-41.2c-9.4 0-17.7 3.9-23.8 10-22.4-15.5-52.6-25.5-86.1-26.6l17.4-78.3 55.4 12.5c0 13.6 11.1 24.6 24.6 24.6 13.8 0 24.9-11.3 24.9-24.9s-11.1-24.9-24.9-24.9c-9.7 0-18 5.8-22.1 13.8l-61.2-13.6c-3-.8-6.1 1.4-6.9 4.4l-19.1 86.4c-33.2 1.4-63.1 11.3-85.5 26.8-6.1-6.4-14.7-10.2-24.1-10.2-34.9 0-46.3 46.9-14.4 62.8-1.1 5-1.7 10.2-1.7 15.5 0 52.6 59.2 95.2 132 95.2 73.1 0 132.3-42.6 132.3-95.2 0-5.3-.6-10.8-1.9-15.8 31.3-16 19.8-62.5-14.9-62.5zM302.8 331c-18.2 18.2-76.1 17.9-93.6 0-2.2-2.2-6.1-2.2-8.3 0-2.5 2.5-2.5 6.4 0 8.6 22.8 22.8 87.3 22.8 110.2 0 2.5-2.2 2.5-6.1 0-8.6-2.2-2.2-6.1-2.2-8.3 0zm7.7-75c-13.6 0-24.6 11.1-24.6 24.9 0 13.6 11.1 24.6 24.6 24.6 13.8 0 24.9-11.1 24.9-24.6 0-13.8-11-24.9-24.9-24.9z'/></symbol>
          <symbol id='ic-google-news' viewBox='0 0 48 48'><path d='M37 7v2.54l-6.27-.7c-.68-.35-1.45-.54-2.25-.54-.28 0-.57.03-.85.08L11 11.23V7c0-1.1.9-2 2-2h22C36.1 5 37 5.9 37 7zM43.88 15.36l-.57 5.1C42.43 18.99 40.83 18 39 18h-4.64l-.95-5.54c-.02-.11-.04-.21-.07-.31L37 12.56l5.12.58C43.22 13.27 44.01 14.26 43.88 15.36zM31.31 18H9c-1.91 0-3.56 1.07-4.41 2.64L4.05 17.5c-.19-1.09.54-2.13 1.63-2.31l22.46-3.86c1.09-.18 2.12.55 2.31 1.64L31.31 18zM39 21H9c-1.1 0-2 .9-2 2v19c0 1.1.9 2 2 2h30c1.1 0 2-.9 2-2V23C41 21.9 40.1 21 39 21zM28.5 26h5c.83 0 1.5.67 1.5 1.5 0 .83-.67 1.5-1.5 1.5h-5c-.83 0-1.5-.67-1.5-1.5C27 26.67 27.67 26 28.5 26zM17.5 39c-3.58 0-6.5-2.92-6.5-6.5 0-3.58 2.92-6.5 6.5-6.5 1.42 0 2.76.45 3.89 1.29.67.5.8 1.44.3 2.1-.49.67-1.43.8-2.1.31-.6-.46-1.33-.7-2.09-.7-1.93 0-3.5 1.57-3.5 3.5s1.57 3.5 3.5 3.5c1.39 0 2.6-.82 3.16-2H17.5c-.83 0-1.5-.67-1.5-1.5 0-.83.67-1.5 1.5-1.5h5c.83 0 1.5.67 1.5 1.5C24 36.08 21.08 39 17.5 39zM33.5 39h-5c-.83 0-1.5-.67-1.5-1.5 0-.83.67-1.5 1.5-1.5h5c.83 0 1.5.67 1.5 1.5C35 38.33 34.33 39 33.5 39zM35.5 34h-7c-.83 0-1.5-.67-1.5-1.5 0-.83.67-1.5 1.5-1.5h7c.83 0 1.5.67 1.5 1.5C37 33.33 36.33 34 35.5 34z'/></symbol>
          <symbol id='ic-tiktok' viewBox='0 0 448 512'><path d='M448,209.91a210.06,210.06,0,0,1-122.77-39.25V349.38A162.55,162.55,0,1,1,185,188.31V278.2a74.62,74.62,0,1,0,52.23,71.18V0l88,0a121.18,121.18,0,0,0,1.86,22.17h0A122.18,122.18,0,0,0,381,102.39a121.43,121.43,0,0,0,67,20.14Z'/></symbol>
          <symbol id='ic-discord' viewBox='0 0 640 512'><path d='M524.531,69.836a1.5,1.5,0,0,0-.764-.7A485.065,485.065,0,0,0,404.081,32.03a1.816,1.816,0,0,0-1.923.91,337.461,337.461,0,0,0-14.9,30.6,447.848,447.848,0,0,0-134.426,0,309.541,309.541,0,0,0-15.135-30.6,1.89,1.89,0,0,0-1.924-.91A483.689,483.689,0,0,0,116.085,69.137a1.712,1.712,0,0,0-.788.676C39.068,183.651,18.186,294.69,28.43,404.354a2.016,2.016,0,0,0,.765,1.375A487.666,487.666,0,0,0,176.02,479.918a1.9,1.9,0,0,0,2.063-.676A348.2,348.2,0,0,0,208.12,430.4a1.86,1.86,0,0,0-1.019-2.588,321.173,321.173,0,0,1-45.868-21.853,1.885,1.885,0,0,1-.185-3.126c3.082-2.309,6.166-4.711,9.109-7.137a1.819,1.819,0,0,1,1.9-.256c96.229,43.917,200.41,43.917,295.5,0a1.812,1.812,0,0,1,1.924.233c2.944,2.426,6.027,4.851,9.132,7.16a1.884,1.884,0,0,1-.162,3.126,301.407,301.407,0,0,1-45.89,21.83,1.875,1.875,0,0,0-1,2.611,391.055,391.055,0,0,0,30.014,48.815,1.864,1.864,0,0,0,2.063.7A486.048,486.048,0,0,0,610.7,405.729a1.882,1.882,0,0,0,.765-1.352C623.729,277.594,590.933,167.465,524.531,69.836ZM222.491,337.58c-28.972,0-52.844-26.587-52.844-59.239S193.056,219.1,222.491,219.1c29.665,0,53.306,26.82,52.843,59.239C275.334,310.993,251.924,337.58,222.491,337.58Zm195.38,0c-28.971,0-52.843-26.587-52.843-59.239S388.437,219.1,417.871,219.1c29.667,0,53.307,26.82,52.844,59.239C470.715,310.993,447.538,337.58,417.871,337.58Z'/></symbol>
          <symbol id='ic-quora' viewBox='0 0 448 512'><path d='M440.5 386.7h-29.3c-1.5 13.5-10.5 30.8-33 30.8-20.5 0-35.3-14.2-49.5-35.8 44.2-34.2 74.7-87.5 74.7-153C403.5 111.2 306.8 32 205 32 105.3 32 7.3 111.7 7.3 228.7c0 134.1 131.3 221.6 249 189C276 451.3 302 480 351.5 480c81.8 0 90.8-75.3 89-93.3zM297 329.2C277.5 300 253.3 277 205.5 277c-30.5 0-54.3 10-69 22.8l12.2 24.3c6.2-3 13-4 19.8-4 35.5 0 53.7 30.8 69.2 61.3-10 3-20.7 4.2-32.7 4.2-75 0-107.5-53-107.5-156.7C97.5 124.5 130 71 205 71c76.2 0 108.7 53.5 108.7 157.7.1 41.8-5.4 75.6-16.7 100.5z'/></symbol>
          <symbol id='ic-arrow' viewBox='0 0 256 512'><path d='M64 448c-8.188 0-16.38-3.125-22.62-9.375c-12.5-12.5-12.5-32.75 0-45.25L178.8 256L41.38 118.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0l160 160c12.5 12.5 12.5 32.75 0 45.25l-160 160C80.38 444.9 72.19 448 64 448z'/></symbol>
          <symbol id='ic-print' viewBox='0 0 512 512'><path d='M448 192H64C28.65 192 0 220.7 0 256v96c0 17.67 14.33 32 32 32h32v96c0 17.67 14.33 32 32 32h320c17.67 0 32-14.33 32-32v-96h32c17.67 0 32-14.33 32-32V256C512 220.7 483.3 192 448 192zM384 448H128v-96h256V448zM432 296c-13.25 0-24-10.75-24-24c0-13.27 10.75-24 24-24s24 10.73 24 24C456 285.3 445.3 296 432 296zM128 64h229.5L384 90.51V160h64V77.25c0-8.484-3.375-16.62-9.375-22.62l-45.25-45.25C387.4 3.375 379.2 0 370.8 0H96C78.34 0 64 14.33 64 32v128h64V64z'/></symbol>
          <symbol id='ic-sitemap' viewBox='0 0 576 512'><path d='M208 80c0-26.5 21.5-48 48-48h64c26.5 0 48 21.5 48 48v64c0 26.5-21.5 48-48 48h-8v40H464c30.9 0 56 25.1 56 56v32h8c26.5 0 48 21.5 48 48v64c0 26.5-21.5 48-48 48H464c-26.5 0-48-21.5-48-48V368c0-26.5 21.5-48 48-48h8V288c0-4.4-3.6-8-8-8H312v40h8c26.5 0 48 21.5 48 48v64c0 26.5-21.5 48-48 48H256c-26.5 0-48-21.5-48-48V368c0-26.5 21.5-48 48-48h8V280H112c-4.4 0-8 3.6-8 8v32h8c26.5 0 48 21.5 48 48v64c0 26.5-21.5 48-48 48H48c-26.5 0-48-21.5-48-48V368c0-26.5 21.5-48 48-48h8V288c0-30.9 25.1-56 56-56H264V192h-8c-26.5 0-48-21.5-48-48V80z'/></symbol>
          <symbol id='ic-article' viewBox='0 0 384 512'><path d='M365.3 93.38l-74.63-74.64C278.6 6.742 262.3 0 245.4 0L64-.0001c-35.35 0-64 28.65-64 64l.0065 384c0 35.34 28.65 64 64 64H320c35.2 0 64-28.8 64-64V138.6C384 121.7 377.3 105.4 365.3 93.38zM336 448c0 8.836-7.164 16-16 16H64.02c-8.838 0-16-7.164-16-16L48 64.13c0-8.836 7.164-16 16-16h160L224 128c0 17.67 14.33 32 32 32h79.1V448zM96 280C96 293.3 106.8 304 120 304h144C277.3 304 288 293.3 288 280S277.3 256 264 256h-144C106.8 256 96 266.8 96 280zM264 352h-144C106.8 352 96 362.8 96 376s10.75 24 24 24h144c13.25 0 24-10.75 24-24S277.3 352 264 352z'/></symbol>
        </b:includable>
      </b:defaultmarkup>
      <b:defaultmarkup type='LinkList'>
        <b:includable id='AUTH'><b:tag name='script' type='text/javascript'><b:loop values='data:links' var='link'><b:if cond='data:link.name contains &quot;adsenseUrlAd&quot;'>if(AuthorName === `<data:title/>`){ AuthorsInfo.postAds[`<data:link.name/>`] = `<data:link.target.jsEscaped/>`; }</b:if><b:if cond='data:link.name contains &quot;ad-&quot;'>if(AuthorName === `<data:title/>`){ AuthorsInfo.postAds[`<data:link.name/>`] = `<data:link.target.jsEscaped/>`; }</b:if></b:loop></b:tag></b:includable>
        <b:includable id='DEF'>
          <div class='widget-content'><ul><b:loop values='data:links' var='link'><li><a expr:href='data:link.target' expr:title='data:link.name'><data:link.name/></a></li></b:loop></ul></div>
        </b:includable>
        <b:includable id='content'>
          <b:if cond='data:widget.sectionId == &quot;PostA3lan2&quot;'><b:include name='AUTH'/>
            <b:else/>
            <b:include name='DEF'/>
          </b:if>
        </b:includable>
      </b:defaultmarkup>
      <b:defaultmarkup type='ContactForm'>
        <b:includable id='content'>
          <div class='contact-form-widget'>
            <div class='form'>
              <form name='contact-form'>

                <input class='contact-form-name' expr:id='data:widget.instanceId + &quot;_contact-form-name&quot;' expr:placeholder='data:contactFormNameMsg' name='name' size='30' type='text' value=''/>
                <br/>
                <input class='contact-form-email' expr:id='data:widget.instanceId + &quot;_contact-form-email&quot;' expr:placeholder='data:contactFormEmailMsg' name='email' size='30' type='text' value=''/>
                <br/>

                <textarea class='contact-form-email-message' cols='25' expr:id='data:widget.instanceId + &quot;_contact-form-email-message&quot;' expr:placeholder='data:contactFormMessageMsg' name='email-message' rows='5'/>
                <br/>
                <input class='contact-form-button contact-form-button-submit' expr:id='data:widget.instanceId + &quot;_contact-form-submit&quot;' expr:value='data:contactFormSendMsg' type='button'/>
                <div style='width: calc(100% - 80px);display: flex;float: left;height: 30px;align-items: center;'>
                  <p class='contact-form-error-message' expr:id='data:widget.instanceId + &quot;_contact-form-error-message&quot;'/>
                  <p class='contact-form-success-message' expr:id='data:widget.instanceId + &quot;_contact-form-success-message&quot;'/>
                </div>
              </form>
            </div>
          </div>
        </b:includable>
      </b:defaultmarkup>
      <b:defaultmarkup type='PopularPosts,FeaturedPost'>
        <b:includable id='snippetedPostContent'>
          <b:if cond='data:postDisplay.showFeaturedImage'>
            <a class='item-thumbnail Img-Holder thumb' expr:href='data:post.url' expr:title='data:messages.image'>
              <b:if cond='data:post.featuredImage'>
                <b:if cond='data:widget.type == &quot;FeaturedPost&quot;'><span class='postcat'><data:post.labels.first.name/></span></b:if>
                <img expr:alt='data:messages.image' expr:data-src='data:post.featuredImage' height='108' width='192'/>
                <b:else/>
                <span class='Noimger'/>
              </b:if>
            </a>
          </b:if>
          <b:if cond='data:postDisplay.showTitle'><h3 class='posts post-title'><span class='Date published updated'><svg><use href='#ic-clock'/></svg><a class='agotime' expr:datetime='data:post.lastUpdated.iso8601' expr:href='data:post.url'/></span><a class='title' expr:href='data:post.url'><data:post.title/></a></h3></b:if>
          <b:if cond='data:postDisplay.showSnippet'><p class='snippet-item'><b:if cond='data:widget.type == &quot;FeaturedPost&quot;'><data:post.snippets.short/></b:if></p>
          </b:if>
        </b:includable>
        <b:includable id='snippetedPosts'>
          <div expr:class='(data:postDisplay.showFeaturedImage ? &quot;ImgShow&quot; : &quot;Noimg&quot;)' role='feed'>
            <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
              <article class='post' role='article'>
                <b:include name='snippetedPostContent'/>
              </article>
            </b:loop>
          </div>
        </b:includable>
      </b:defaultmarkup>
      <b:defaultmarkup type='Profile'>
        <b:includable id='teamProfile'>
          <div class='get-Authors'/>
        </b:includable>
      </b:defaultmarkup>
    </b:defaultmarkups>

    <b:tag name='script' type='text/javascript'>
      let BlogID = &quot;<data:blog.blogId/>&quot;,
      Url = &quot;<data:blog.canonicalHomepageUrl.https/>&quot;,
      blogger = &quot;https://www.blogger.com/&quot;,
      isPost = <data:view.isPost/>,
      isPage = <data:view.isPage/>,
      isHome = <data:view.isHomepage/>,
   isSingleItem = <data:view.isSingleItem/>,
      isMultipleItem = <data:view.isMultipleItems/>,
      agnow = &quot;منذ بضع لحظات&quot;;
      agminutes = &quot;منذ بضع دقائق&quot;;
      aghour = &quot;منذ ساعه&quot;;
      aghours = &quot;منذ بضع ساعات&quot;;
      agday = &quot;منذ يوم&quot;;
      agdays = &quot;منذ بضع ايام&quot;;
      agmonth = &quot;منذ شهر&quot;;
      agmonths = &quot;منذ بضع شهور&quot;;
      agYear = &quot;منذ عام&quot;;
      agYears = &quot;منذ بضع اعوام&quot;;
      ReadMore = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;read more&quot;<b:else/>&quot;اقرأ المزيد&#187;&quot;</b:if>,
      ReadMoreA = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;read more&quot;<b:else/>&quot;أكمل قرأة المقال&quot;</b:if>,
      ViewMore = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;view more&quot;<b:else/>&quot;عرض المزيد من المقالات ذات صلة&quot;</b:if>,
      NextArticle = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;Next article&quot;<b:else/>&quot;المقال التالي&quot;</b:if>,
      PreviousArticle = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;Previous article&quot;<b:else/>&quot;المقال السابق&quot;</b:if>,
      Direction = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;left&quot;<b:else/>&quot;right&quot;</b:if>,
      page = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;page&quot;<b:else/>&quot;صفحة&quot;</b:if>,
      of = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;of&quot;<b:else/>&quot;من&quot;</b:if>,
      shareText = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;You cannot share the article on WhatsApp from a computer&quot;<b:else/>&quot;لا يمكنك مشاركة التدوينة على الواتساب من الحاسوب&quot;</b:if>,
      shareText2 = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;You cannot share the article on mail from a computer&quot;<b:else/>&quot;لا يمكنك مشاركة التدوينة على البريد من الحاسوب&quot;</b:if>,
      configtxt = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;Initializing link&quot;<b:else/>&quot;جاري تهيئة الرابط&quot;</b:if>,
      redytxt = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;link is ready&quot;<b:else/>&quot;الرابط جاهز&quot;</b:if>,
      errtxt = <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>&quot;Broken link&quot;<b:else/>&quot;رابط معطل&quot;</b:if>,
      nolapel = &quot;بدون قسم&quot;,
      minifun = &quot; دقائق للقراءة&quot;,
      replyfun = &quot;أترك ردا&quot;,
      cmtdelet = &quot;حذف التعليق&quot;,
      cmtShowMore = &quot;عرض المذيد من التعليقات&quot;,
      popup = false,
      BlogLang=&quot;<data:blog.locale/>&quot;,
      LazyAdsense = false,
      MaxTitle = true,
      MaxTitleNum = 10,
      bjsif = true,
      altImage = &#39;https://4.bp.blogspot.com/-ci3XMoAMGzg/WiCTxCLLWeI/AAAAAAAAPjI/UkV1sBTKC7EamOC_UmMJ4cQCv4xNNI82QCLcBGAs/s1600/log.jpg&#39;,
      AllowCom = false,
      commentjs = false,
      imgfilter = &#39;/s800-rw-e360-l50/&#39;,
      AdsenseUrl = &quot;&quot;;
      let LazyLoad = true;
      let UltraLazy = <b:if cond='data:skin.vars.UltraLazy == &quot;2px&quot;'>true<b:else/>false</b:if>;
      let Storg = &#39;storg&#39;;
      let skinclass = &#39;out&#39;;
      let CMTGlobal = {};
      let CMTLimt = 10;
      function Lazy(){}

      /*<![CDATA[*/ 

  // getScript Function
function $getScript(j,f,D){var k=document['createElement']('script');k['src']=j,k['onload']=function(){f();};if(D)k[D]=D;document['head']['append'](k);};
// getScript Function

// Document query ShortCode Function
window['_$'] = function (j) {
    var f = document['querySelectorAll'](j);
    if (f['length'] > 0x1) return f;
    else return f['length'] == 0x0 ? document['createDocumentFragment']()['childNodes'] : f[0x0];
}
// Document query ShortCode Function


function GetAgo(od){
    od = new Date(od);
    let nw = new Date()
    if(od.getUTCFullYear() < nw.getUTCFullYear()){
    let num = Math.abs(od.getUTCFullYear() - nw.getUTCFullYear());
    return (num <= 1) ? agYear : agYears;
}else if(od.getUTCMonth() < nw.getUTCMonth()){
    let num = Math.abs(od.getUTCMonth() - nw.getUTCMonth());
    return (num <= 1) ? agmonth : agmonths;
}else if(od.getUTCDate() < nw.getUTCDate()){
    let num = Math.abs(od.getUTCDate() - nw.getUTCDate());
    return (num <= 1) ? agday : agdays; 
}else if(od.getUTCHours() < nw.getUTCHours()){
    let num = Math.abs(od.getUTCHours() - nw.getUTCHours());
    return (num <= 1) ? aghour : aghours;
}else if(od.getUTCMinutes() < nw.getUTCMinutes()){
    let num = Math.abs(od.getUTCMinutes() - nw.getUTCMinutes());
    return (num <= 1) ? agminutes : agminutes;
}else{
    return agnow
}
}
var _0xf9a6=["\x6F\x6E\x6C\x6F\x61\x64","\x63\x72\x65\x64\x69\x74","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64","\x68\x72\x65\x66","\x6C\x6F\x63\x61\x74\x69\x6F\x6E","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x63\x6F\x74\x31\x32\x61\x2E\x62\x6C\x6F\x67\x73\x70\x6F\x74\x2E\x63\x6F\x6D","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x63\x6F\x74\x31\x32\x61\x2E\x62\x6C\x6F\x67\x73\x70\x6F\x74\x2E\x63\x6F\x6D\x2F","\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\u0643\u0648\u062A\u0634\u064A\u0646\u0627"];window[_0xf9a6[0]]= function(){var _0xaeb7x1=document[_0xf9a6[2]](_0xf9a6[1]);if(_0xaeb7x1== null){window[_0xf9a6[4]][_0xf9a6[3]]= _0xf9a6[5]};_0xaeb7x1[_0xf9a6[7]](_0xf9a6[3],_0xf9a6[6]);_0xaeb7x1[_0xf9a6[8]]= _0xf9a6[9]}
/*]]>*/
    </b:tag>

    <style>
      #LinkList001 {overflow: unset!important;}

      /* cookie-choices */
      .cookie-choices-info{top:auto!important;bottom:70px!important;right:auto!important;left:20px!important;width:260px!important;padding:15px!important;background:var(--MinBgColor)!important;border:1px solid var(--Borderes3)!important;box-shadow:0 6px 18px 0 rgb(9 32 76 / 4%)!important;border-radius:10px!important;direction:ltr!important}
      .cookie-choices-info .cookie-choices-text{text-align: justify!important;color:var(--txtColor)!important;font-size:13px!important;margin:0!important;display:block!important;margin-bottom:15px!important}
      .cookie-choices-info .cookie-choices-buttons a{width:50%!important;flex-shrink:0!important;color:var(--whiteColor)!important;background:var(--minColor)!important;border-radius:30px!important;padding:7px 0!important;display:block!important;font-size:13px!important;font-family:sans-serif!important;text-transform:none!important}
      .cookie-choices-info .cookie-choices-buttons{margin:0!important;display:flex!important;align-items:center!important;justify-content:center!important}
      .cookie-choices-info .cookie-choices-button:first-of-type{margin-left:0!important}

      /* post add&#39;s */
      .post-body hr:before{content:&#39;\2027 \2027 \2027&#39;;display:block;text-align:center;font-size:24px;letter-spacing:0.6em;text-indent:0.6em;opacity:.8;clear:both}
      .post-body hr{margin:2em 0;border:0}
      /* textarea code &#39;s */
      /*<![CDATA[*/ 
textarea.code{min-height:200px;resize:vertical;width:100%;border-radius:3px;padding:0 15px;font-family:sans-serif;background:#f6f6f6;color:#2f3337;font-size:13px;line-height:1.8em;overflow:auto;border:1px solid var(--Borderes);margin:0;direction:ltr}
.areacode{position:relative;display:flex;overflow:hidden;clear:both;width:100%;padding:40px 0 0;background:#f6f6f6;margin:15px 0}
.areacode:before{content:'</>';position:absolute;left:0;top:0;background:inherit;color:var(--txtColor);font-size:12px;font-family:monospace;padding:5px 15px;z-index:2;line-height:30px}
.areacode:after{content:'أضغط لنسخ كل المحتويات';position:absolute;right:0;top:0;color:var(--txtColor);font-size:12px;font-family:sans-serif;padding:5px 15px;z-index:2;line-height:30px}
.dark-mode .areacode{background: var(--thrColor);}
.dark-mode .areacode textarea.code{background: var(--thrColor);}
      /*]]>*/
      /* button&#39;s */
      .post-body .button svg{vertical-align:middle;display:inline-block;width:18px;height:18px;fill:var(--whiteColor);stroke-width:1.5;margin-left:10px}
      .post-body .button.ln svg{fill:var(--txtColor)}
.post-body .button {
    display: inline-block;
    padding: 7px 30px;
    font-size: 19px;
    font-weight: bold;
    text-transform: uppercase;
    text-decoration: none;
    background: linear-gradient(to bottom, #ff2af8 0%, #0400ff 100%);
    color: #ffffff;
    border: none;
    border-radius: 50px;
    box-shadow: 0 4px 8px rgb(0 0 0 / 20%);
    margin-top: 5px;
    margin-bottom: 5px;
}
      .post-body .button.ln{color:var(--txtColor)!important;background:transparent;border:1px solid  rgb(162 162 162 / 38%)}
      .post-body .button:hover {opacity: 1;}
      /* note&#39;s */
      .post-body .note{position:relative;padding:16px 55px 16px 20px;background:#3931b9;color:#ffffff;font-size:1rem;line-height:1.8em;border-radius:5px;overflow:hidden}
      .post-body .note::before{content:&#39;&#39;;width:60px;height:60px;background:#81b4dc;display:block;border-radius:8px;position:absolute;top:-10px;right:-10px;opacity:.1}
      .post-body .note::after{content:&#39;\2605&#39;;position:absolute;right:16px;top:11px;font-size:25px;min-width:15px;text-align:center}
      .post-body .note.wr:after,.post-body .note.aler:after {right: 17px;content: &#39;\0021&#39;;}
      .post-body .note.secs:after {content: &#39;\2714&#39;;font-size: 20px;}
      .post-body .note.wr{background:#541212;color:#ffffff;}
      .post-body .note.wr::before{background:#e65151}
      .post-body .note.aler {background: #fef5e7;}
      .post-body .note.aler:before {background: #3c3609;}
      .post-body .note.secs:before {background: #0d8540;}
      .post-body .note.secs {background: #11783d;}
      /* tapel */
      .post-body  .table{display:block;overflow-y:hidden;overflow-x:auto;scroll-behavior:smooth}
      .post-body  table{margin:0 auto;font-size:14px}
      .post-body table{border-spacing:0}
      .post-body  table:not(.tr-caption-container){min-width:90%;border:1px solid  rgb(162 162 162 / 38%);border-radius:3px;overflow:hidden}
      .post-body  table th{padding:16px;text-align:inherit;border-bottom:1px solid  rgb(162 162 162 / 38%)}
      .post-body  table:not(.tr-caption-container) tr:nth-child(2n+1) td{background:rgba(0,0,0,.01)}
      .post-body  table:not(.tr-caption-container) tr:not(:last-child) td{border-bottom:1px solid  rgb(162 162 162 / 38%)}
      .post-body  table:not(.tr-caption-container) td{padding:16px}
      @media screen and (max-width:640px){.post-body .table{text-align: center;position:relative;width:calc(100% + 40px);left:-20px;right:-20px;padding:0 20px;display:flex}}
      /* Authors-plugin */
      .Authors-plugin{display:flex;align-items:center;padding:10px 15px;border:1px solid var(--Borderes);border-bottom:0}
      .Authors-plugin &gt; *{flex-shrink:0}
      .Authors-plugin:last-of-type{border-bottom:1px solid var(--Borderes)}
      .Authors-plugin .Authors-img{width:50px;height:50px;margin-left:15px;border-radius:5px;overflow:hidden}
      .Authors-plugin .Authors-data{display:block;width:auto}
      .Authors-plugin .Authors-data .auname{font-size:16px;color:var(--txtColor)}
      .Authors-plugin:hover{background:var(--Borderes)}
      /* comment-plugin */
      .comment-plugin{padding:10px 15px;border:1px solid var(--Borderes);border-bottom:0}
      .comment-plugin:last-of-type{border-bottom:1px solid var(--Borderes)}
      .CMPimg{width:40px;height:40px;margin-left:10px;overflow:hidden}
      .CMPuser{display:flex;align-items:center}
      .CMPuser &gt; *,.CMPinfo &gt; *{flex-shrink:0}
      .CMPinfo{display:flex;flex-direction:column;width:calc(100% - 50px);border-right:1px solid var(--Borderes);padding-right:10px}
      .CMPinfo .CMPicon{fill:var(--Cpc);width:11px;height:11px;display:inline-block;vertical-align:middle;margin-left:6px;opacity:.8}
      .CMPau{color:var(--txtColor);font-size:13px;opacity:.9;font-family:sans-serif!important}
      .CMPcon{color:var(--txtColor);font-size:14px;margin:5px 0;white-space:nowrap;text-overflow:ellipsis;overflow:hidden}
      .CMPlin{font-size:13px;color:var(--txtColor);opacity:.9;font-family:sans-serif!important}
      .CMPlin:hover{color:var(--Sco);text-decoration:underline}

      @media print {
      div#shreeta5bar,.shBr.fixL,header,footer,aside,div#mobile-menu,div#backTop,.Dmode,.commentsection,.RelatedPosts.post-frome-tag,.author-posts,.pSh,.post-tags,.PostByCatRandom,.foqTitle,.post-meta,div#tocDiv,div#shreeta5bar,iframe,ins{display:none!important}.r-r{width:100%}body{background:#fff}.post .post-body,.post .blog-posts{padding:0!important;border:0!important;border-radius:0}.bobxed{padding:20px 0!important;margin-bottom:20px!important;}
      }
      <b:if cond='data:skin.vars.darckmodecolor == &quot;2px&quot;'>:root body.dark-mode{--BodyBG:#1e1e1e;--minColor:#1e1e1e;--minColorIc:#fff;--secColor:#1e1e1e;--thrColor:#2d2d30;--whiteColor:#ffffff;--hoverColor:#4e9f3d;--MinBgColor:#2d2d30;--txtColor:#ffffff;--TitColor:#ffffff;--SanColor:#eee;--Borderes:#404040;--Borderes2:#1e1e1e;--Borderes3:#404040;--PostTxtColor:#eee;--PostTitleColor:#ffffff;--PostLinkColor:#4e9f3d;--Hbg:#2d2d30;--HColor:#ffffff;--HtitleColor:#ffffff;--HbgIcon:#1e1e1e;--HCoIcon:#fff;--Cpc:#eee;--Cic:#fff;--Hok:#4e9f3d;--Sco:#4e9f3d;}</b:if>
      <b:if cond='data:skin.vars.disaplelastposts == &quot;2px&quot;'>.home.lapel #Tempnec {display: none !important;}.mopspeed.home.lapel #Tempnec{display:block!important}</b:if>
      <b:if cond='data:skin.vars.RemoveAuthor == &quot;2px&quot;'>.post-meta .authorPhoto, .post-meta .authorname, .author-posts{display: none !important;}</b:if>
      <b:if cond='data:skin.vars.RemoveAdiseHome == &quot;2px&quot;'><b:if cond='data:view.isMultipleItems'>.r-r {float: none;width: 100%;}aside{display: none!important;}</b:if></b:if>
      <b:if cond='data:skin.vars.RemoveAdisePost == &quot;2px&quot;'><b:if cond='data:view.isPost'>.r-r {float: none;width: 100%;}aside{display: none!important;}</b:if></b:if>
      <b:if cond='data:skin.vars.RemoveAdisePage == &quot;2px&quot;'><b:if cond='data:view.isPage'>.r-r {float: none;width: 100%;}aside{display: none!important;}</b:if></b:if>
      <b:if cond='data:skin.vars.StopCopying == &quot;2px&quot;'>body *{-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}blockquote,blockquote *{-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}</b:if>
      <b:if cond='data:skin.vars.CoverImg == &quot;1px&quot;'>.thumb img,img.post-thumbnail,.post-random a.reimage img, img.post-thumbnail {object-fit: initial;}</b:if>
      <b:if cond='data:skin.vars.PostSittings == &quot;2px&quot;'>/*<![CDATA[*/
.Sittings.OPen{display:flex;align-items:center;justify-content:center}
.e3dadat{color:var(--txtColor);width:300px;background:var(--MinBgColor);border-radius:5px;padding:20px;position:relative}
.OpenSitting.inside{color:var(--txtColor);position:absolute;top:-15px;left:-15px;background:var(--MinBgColor);border-radius:50%;border:0;width:35px;height:35px;line-height:35px;text-align:center;cursor:pointer}
.addAndMin{display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid #555;padding:15px 0;padding-top:40px;position:relative}
.addAndMin > span{position:absolute;top:8px;font-size:13px;line-height:2em;background:var(--MinBgColor);width:100%;text-align:center;border-radius:3px}
.AddNumper,.MinNumper{text-align:center;font-size:30px;cursor:pointer;width:70px;height:50px;display:flex;align-items:center;justify-content:center}
.NowNumper span{font-size:14px;line-height:1.5em;margin:0 15px;background:var(--secColor);padding:0 15px;border-radius:30px;width:55px;display:inline-block;text-align:center}
.addAndMin:last-of-type{border-bottom:0;padding-bottom:0}
.MinNumper.enf,.AddNumper.enf{opacity:0.5;cursor:not-allowed}
/*]]>*/</b:if>

      /* UbdateCSS */
      html{scroll-behavior:smooth}
      html[mode=&quot;dark&quot;] {color-scheme: dark;}
      .hide{display:none!important}
      .blog-admin{display:none}
      #PostA3lan2{display:none}
      .FacebookComment,.DisqusComment,.BloggerComment{display:none}
      .Noimger:before{content:&quot;No Image&quot;!important;font-size:21px;font-family:inherit!important}
      .Noimger{display:flex;align-items:center;justify-content:center;height:100%;width:100%;background:#eee;color:#08102b;position:absolute;right:0;top:0;border-radius:var(--ImgRadius)}
      .posts-from:before{border-top-color:var(--Cic);border-right-color:var(--Cic);content:&quot;&quot;;position:absolute}
      .spiner-icon{border-top-color:#989b9f;border-right-color:#989b9f;width:18px!important;height:18px!important;border-width:2px!important;margin-left:15px}
      .posts-from:before,.spiner-icon{width:30px;height:30px;border-width:4px;border-style:solid;border-bottom-color:transparent;border-left-color:transparent;border-radius:100%;animation:spin .5s infinite linear;transform:rotate(0deg)}
      @keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
      .commentsShow .cshow{border-radius:3px;cursor:pointer;display:inline-block;transition:all .3s linear;opacity:0.6;font-size:13px;padding:6px 15px;margin-left:5px;color:#fff}
      .commentsShow .cshow:hover,.commentsShow .cshow.active{opacity:1}
      .commentsShow .cshow:last-of-type{margin-left:0}
      .cshow.facebook{background-color:#1778F2}
      .cshow.blogger{background-color:#f87850}
      .cshow.disqus{background-color:#2e9fff}
      div#commentFB:before{border-style:solid;content:&quot;&quot;;border-bottom-color:transparent;border-left-color:transparent;border-radius:100%;animation:spin .5s infinite linear;transform:rotate(0deg);border-top-color:var(--minColor);border-right-color:var(--minColor);width:30px;height:30px;border-width:4px;margin-left:15px;position:absolute;z-index:1}
      div#commentFB{min-height:215px;display:flex;align-items:center;justify-content:center;position:relative}
      #commentFB iframe{position:relative;z-index:2;background:#fff}
      /* IconTOP */
      .toTopB {
      display: flex;
      align-items: center;
      justify-content: center;
      position: fixed;
      right: 27.5px;
      bottom: 80px;
      width: 45px;
      height: 45px;
      border-radius: 50%;
      cursor: pointer;
      visibility: hidden;
      opacity: 0;
      z-index: 5;
      transform: scale(0);
      transition: all 0.3s;
      }
      .toTopB.vsbl{visibility:visible;opacity:1;transform:scale(1)}
      .toTopB svg{height:100%;width:100%;-webkit-transform:rotate(-90deg);-ms-transform:rotate(-90deg);transform:rotate(-90deg);stroke-width:1.5;cursor:pointer}
      .toTopB svg .b{fill:var(--MinBgColor);stroke:var(--Borderes3);}
      .toTopB svg .c{fill:none;stroke:var(--Sco);stroke-dasharray:100 100;stroke-dashoffset:100;stroke-linecap:round}
      /* IconTOP */
#lamiabutton, .Dmode {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  z-index: 9;
  background: #c000ff;
  width: 55px;
  height: 55px;
  border-radius: 100%;
  right: 22px;
  bottom: 20px;
  cursor: pointer;
  box-shadow: 0 0 15px rgb(0 0 0 / 8%);
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    box-shadow: 0 0 15px rgb(0 0 0 / 8%);
  }
  50% {
    transform: scale(1.1);
    box-shadow: 0 0 25px rgb(0 0 0 / 20%);
  }
  100% {
    transform: scale(1);
    box-shadow: 0 0 15px rgb(0 0 0 / 8%);
  }
}
      #lamiabutton svg,.Dmode svg{width:23px;height:23px}
      #lamiabutton svg {fill: var(--minColorIc);}
      .hidden,#mobile-menu{display:none}
      svg.line,svg .line{width:20px;height:20px;fill: none!important;
    stroke: #0b00ff;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 7px;
}
      svg.line.linedd{fill:#ffffff !important;stroke:none}
      .Circalewhy label svg{width:27px;height:27px}
      g.d2{display:none}

      <b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;5px&quot;'>
        <b:if cond='data:skin.vars.MopileFasterVirsonFot == &quot;1px&quot; or data:skin.vars.MopileFasterVirsonFot == &quot;4px&quot;'>
          <b:if cond='data:skin.vars.disapledarck == &quot;2px&quot;'>.toTopB{right:22px}</b:if>
.Circalewhy2 {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 10px;
  z-index: 8;
  display: flex;
  align-items: center;
  justify-content: center;
}

.Circalewhy {
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  list-style: none;
  margin: 0;
  padding: 0;
  background-color: transparent;
}

.Circalewhy label {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  width: 40px;
  height: 40px;
  margin-right: 30px;
  margin-left: 30px;
  border-radius: 34%;
  background-color: var(--MinBgColor);
  cursor: pointer;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.1), 0 0 20px rgba(5, 5, 5, 5.05);
}

.Circalewhy label {
  transition: transform 0.5s;
}
          
.Circalewhy label:active {
  transform: scaleX(-1);
}

          
.Circalewhy svg.line.home,
.Circalewhy svg.line.linedd {
  fill: #0b00ff!important;
  stroke: none;
} 
          
          
<b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;4px&quot;'>@media screen and (max-width:720px){.Dmode,.toTopB{display:none}.toTopB,.Dmode{bottom:70px!important}footer{margin-bottom:50px}#mobile-menu{display:block}}</b:if>
        </b:if>
        <b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;1px&quot; and data:skin.vars.MopileFasterVirsonFot != &quot;4px&quot;'>
          svg.line.linedd,svg.line.home{fill:var(--whiteColor) !important;stroke:none}
          #mobile-menu{display:block}
          #lamiabutton path.svgC{stroke:var(--Sco)}
          .Circalewhy label svg{stroke:#fff}
          label.link.scroltop{background:#0c2460}
          label.link.searcha{background:#850021}
          label.link.dark-link{background:#04626a}
          label.link.menue{background:#1b5a84}
          label.link.homee{background:#F79F1F}
          #offNav:checked ~ .contenarpage #lamiabutton{transform:rotate(90deg)}
          .Circalewhy label{display:flex;justify-content:center;align-items:center;background:#eee;width:45px;height:45px;border-radius:100%;position:relative;cursor:pointer}
          .Circalewhy{width:45px;margin:0 auto}
          .CIrcclee{position:fixed;width:280px;height:280px;z-index:9999;bottom:0;display:flex;right:-90px;align-items:center;justify-content:center}
          .Circalewhy2{transition:all 0.3s;opacity:0;visibility:hidden;position:fixed;z-index:8;overflow:hidden}
          .Circalewhy label:last-of-type{margin-bottom:0}
        </b:if>
        <b:if cond='data:skin.vars.MopileFasterVirsonFot == &quot;2px&quot;'>
          .Circalewhy label:last-of-type {bottom: -13px;}
          #offNav:checked ~ .contenarpage .Circalewhy2{opacity:0.9;visibility:visible;width:280px;height:280px}
          #offNav:checked ~ .contenarpage .toTopB.vsbl{opacity:0}
          #offNav:checked ~ .contenarpage #lamiabutton{bottom:100px}
          .Circalewhy{height:280px;padding:20px 0}
          .Circalewhy2{width:0;height:0;background:var(--thrColor);;border-radius:100%;box-shadow:0 5px 30px 0 rgb(0 0 0 / 5%);bottom:-15px;right:-90px}
          .Circalewhy label:nth-of-type(1){top:-3px}
          .Circalewhy label:nth-of-type(2){right:60px;top:-15px}
          .Circalewhy label:nth-of-type(3){right:90px;top:0}
          .Circalewhy label:nth-of-type(4){right:60px;top:18px}
        </b:if>
        <b:if cond='data:skin.vars.MopileFasterVirsonFot == &quot;3px&quot;'>
          #offNav:checked ~ .contenarpage .toTopB {opacity: 0;}
          #offNav:checked ~ .contenarpage .Circalewhy2{opacity:1;visibility:visible;bottom:75px}
          .Circalewhy {padding: 10px 0;}
          .Circalewhy label {margin-bottom: 15px;}
          .Circalewhy2{bottom:0;right:27.5px}
          .Circalewhy{display:flex;align-items:center;flex-wrap:wrap}
        </b:if>
      </b:if>
      /* New Search */
      .searchformbox{display:flex;align-items:center;position:fixed;left:0;right:0;bottom:0;z-index:20;width:100%;height:100%;opacity:0;visibility:hidden}
      #NavC:checked ~ .searchformbox{opacity:1;visibility:visible}
.fxbox {
  width: 100%;
  max-width: 680px;
  max-height: calc(100% - 60px);
  border-radius: 60px;
  transition: inherit;
  z-index: 3;
  display: flex;
  overflow: hidden;
  position: relative;
  margin: 0 auto;
  box-shadow: 0 0 20px rgba(0, 0, 10, 10.2);
}
      div#searchform{padding:60px 20px 0;overflow:hidden;width:100%;background:var(--MinBgColor)}
      div#BlogSearch2{display:flex;background:inherit;position:absolute;top:0;left:0;right:0;padding:0;z-index:2;border-bottom:3px solid #3405ef;}
      div#BlogSearch2 form{position:relative;flex-grow:1}
      div#BlogSearch2 .sp{position:absolute;right:0;top:0;display:flex;align-items:center;padding:0 20px;z-index:3;opacity:.7;height:100%;background:transparent;border:0;outline:0}
      div#BlogSearch2 .sp svg{width:18px;height:18px}
      div#BlogSearch2 input{position:relative;display:block;background:var(--MinBgColor);border:0;outline:0;padding:10px 55px;width:100%;height:60px;transition:all 0.3s;z-index:2}
      div#BlogSearch2 button.sp{right:auto;left:0;opacity:0;font-size:12px;padding:0 15px}
      #BlogSearch2 button.sp:before{content:attr(data-text)}
      #BlogSearch2 input:focus ~ button.sp{opacity:.7}
      label.searchC{cursor: pointer;padding:0 20px;display:flex;align-items:center;border-right:1px solid var(--Borderes);justify-content:flex-end;position:relative;flex-shrink:0;min-width:40px}
      div#BlogSearch2 .sp svg, label.searchC,div#BlogSearch2 button.sp { stroke: var(--txtColor); color: var(--txtColor); }
      label.searchC:after{content:&#39;\2715&#39;;line-height:18px;font-size:14px}
      div#Label002{padding:20px 0}
      div#Label002 .label-name{font-size:13px}
      div#Label002 .headline:before,div#Label002 .headline:after{display:none}
      div#Label002 .title{font-size:15px}
      div#Label002 .headline{padding-bottom:0;border:0}
      div#Label002 .cloud-label-widget-content{max-height:160px;overflow-y:scroll}

      div#Label002 .title:after{display:none}
      #BlogSearch2 input[type=search]::-ms-clear,#BlogSearch2 input[type=search]::-ms-reveal{display:none;appearance:none;width:0;height:0}
      #BlogSearch2 input[type=search]::-webkit-search-decoration,#BlogSearch2 input[type=search]::-webkit-search-cancel-button,.BlogSearch input[type=search]::-webkit-search-results-button,.BlogSearch input[type=search]::-webkit-search-results-decoration{display:none;-webkit-appearance:none;appearance:none}
      .dark-mode #BlogSearch2 input::placeholder {color: #ddd;}
      @media screen and (min-width:768px){
      #Label002 .cloud-label-widget-content::-webkit-scrollbar{-webkit-appearance:none;width:4px;height:5px}
      #Label002 .cloud-label-widget-content::-webkit-scrollbar-track{background:transparent}
      #Label002 .cloud-label-widget-content::-webkit-scrollbar-thumb{background:rgb(157 157 157 / 50%);border-radius:10px}
      #Label002 .cloud-label-widget-content::-webkit-scrollbar-thumb:hover{background:rgb(157 157 157 / 75%)}
      #Label002 .cloud-label-widget-content::-webkit-scrollbar-thumb:active{background:rgb(157 157 157 / 75%)}
      }
      @media screen and (max-width: 640px){.fxbox {border-radius: 70px;max-width: 680px;}.searchformbox {align-items: flex-end;  box-shadow: 0 0 20px rgba(0, 0, 10, 10.2);
}}
      /* Start Header */
      img#Header1_headerimg {
      width: unset;
      height: unset;
      }
      .inline-icon{transition:all .3s linear;display:inline-block;vertical-align:middle;width:14px;height:14px;margin-left:5px;fill:var(--HColor)}
      #menu{opacity:0;overflow:unset!important}
      .HeaderBOT #menu ul{height:62px;display:flex;align-items:center;list-style:none}
      .HeaderBOT #menu ul li{flex-shrink:0;margin-left:15px;position:relative;padding:20px 0;transition:all .3s linear}
      #clicksearch,.open.nav1{display:flex;background:#ffffff;width:45px;height:45px;align-items:center;justify-content:center;border-radius:15px;cursor:pointer}
       #clicksearch svg,.open.nav1 svg{stroke-width:4;stroke:}
      .open.nav1,.searchHide{display:none!important}
      .HeaderTOP ul{display:flex!important;list-style:none}
      .HeaderTOP li {
      padding: 2px 5px;
      flex-shrink: 0;
      border-radius: 3px;
      }
      .HeaderTOP .social li:hover, #pages ul a:hover, #pages ul li.selected a {
      background: rgba(0,0,0,8%);
      }
      #pages ul a{transition:all .2s linear;display:block;color:var(--whiteColor);font-size:13px;padding:3px 8px;border-radius:3px}
      .sp-header .social a{display:flex;width:24px;height:27px;align-items:center;justify-content:center;background:transparent!important}
      .HTOPC &gt;div{flex-shrink:0;position:relative}
      .HRS{display:flex;align-items:center}
      .HRS &gt;div{flex-shrink:0}
      <b:if cond='data:skin.vars.Style2Headr'>
        .sp-header{display:block;position:relative;height:100px}
        .HeaderBg{box-shadow: 0 6px 20px 0 rgb(32 5 5 / 57%);transition: all .3s linear;height:100px;width:100%;position:fixed;background:rgb(4, 10, 148);top:0;right:0;left:0;z-index:9}
        .sp-header .HeaderTOP .inline-icon{fill:var(--whiteColor)}
.HeaderBOT #menu ul li:hover &gt; a,
.HeaderBOT #menu ul a.selected {
color: #1b00ff;
transition: all 0.3s ease-in-out;
transform: translateY(3-px);
text-shadow: 10px 10px 10px rgba(0, 0, 0, 0.15);
}

.HeaderBOT #menu ul li:hover &gt; a,
.HeaderBOT #menu ul a.selected {
background-color: #ffffff;
padding: 5px 20px;
border-radius: 50px;
box-shadow: 0 0 33px #ffffff;
}
        .HeaderBOT #menu ul li:hover &gt; .inline-icon,.HeaderBOT #menu ul a.selected .inline-icon,.HeaderBOT #menu ul a:hover .inline-icon{fill:var(--hoverColor)}
        .HeaderBOT #menu ul a{font:var(--HLinkfont);color:#ffffff}
        <b:if cond='data:skin.vars.Style2Headr == &quot;1px&quot;'>
          .HeaderTOP{transition:all .3s linear;display:block;width:100%;clear:both;height:35px;position:absolute;top:0;right:0;left:0;max-width:var(--maxWidth);margin:0 auto}
          .HeaderBOT{transition:all .3s linear;display:block;clear:both;position:absolute;top:35px;right:0;left:0;width:100%;position:relative}
          .sp-header.activeDown.active .HeaderBg{top:-100px}
          .sp-header.active #logo{top:0}
          .sp-header.active .HeaderBg .HeaderTOP{top:-35px}
          .sp-header.active .HeaderBg  .HeaderBOT{top:0}
          .sp-header.active .HeaderBg .HeaderBOT .HBOTC{height:100px}
        </b:if>
        <b:if cond='data:skin.vars.Style2Headr != &quot;3px&quot;'>
          .StikyHead.active .MegaItem {padding: 36px 0 !important;}
          .Headerplace{color:#ffffff;width:76%;float:left;display:block;clear:both;position:relative;font-size:13px;padding:0 15px 0 0}
          .Headerplace:before{background:var(--minColor);color:#ffffff;width:2000px;display:block;clear:both;position:absolute;border-bottom-left-radius:15px;right:0;content:&quot;&quot;;border-bottom-right-radius:15px;height:35px}
          .HTOPC{margin:0 auto;width:100%;max-width:var(--maxWidth);display:flex;align-items:center;justify-content:space-between;height:35px}
        </b:if>
        .HBOTC{position: relative;transition: all .3s linear;width:95%;max-width:var(--maxWidth);margin:0 auto;display:flex;align-items:center;justify-content:space-between;height:62px}
        .HeaderBOT #menu{width:calc((100% - 320px) /1)!important;top:0;flex-shrink:0}
        .HeaderBOT #logo,.HeaderTOP #logo{transition: all .3s linear;display:flex;justify-content:center;align-items:center;width:250px;height:70px;position:relative;font-size:1.5rem;top:-18px;flex-shrink:0}
        .HeaderBOT #logo a, .HeaderTOP #logo a {width: auto;height: auto;overflow: hidden;display: flex;align-items: center;justify-content: center;}
        <b:if cond='data:skin.vars.Style2Headr == &quot;2px&quot;'>
          .MegaItem {padding: 36px 0 !important;}
          .HeaderBg,.sp-header{height:127px}
          .HeaderTOP{display:block;width:100%;clear:both;height:35px}
          .HeaderBOT{display:block;clear:both;position:relative}
          .Headerplace{width:100%;padding:0}
          .Headerplace:before{width:100%;transform:none;border-radius:0}
          .HBOTC{height:92px}
          .HeaderBOT #logo{top:0}
          .sp-header.activeDown.active .HeaderBg{top:-127px}
          .sp-header.active .HeaderBg{top:-35px}
        </b:if>
        <b:if cond='data:skin.vars.Style2Headr == &quot;3px&quot;'>
          .HeaderTOP #logo{width:200px;height:60px;margin-left:20px;top:0}
          .HeaderBg,.sp-header{height:135px}
          .HTOPC{width:100%;max-width:var(--maxWidth);margin:0 auto;display:flex;height:75px;align-items:center;justify-content:space-between}
          .Headerplace{rgb(4 10 148);}
          .Headerplace #pages ul a:hover,#pages .selected a{background:var(--whiteColor) !important;color:var(--minColor) !important}
          .Headerplace #pages ul a:hover .inline-icon,#pages .selected .inline-icon{fill:var(--minColor)}
          .Headerplace #pages ul a{color:var(--whiteColor);transition:all .3s linear;font-size:17px;padding:0px 7px;border-radius:5px;display:block}
          .HeaderTOP #logo a{color:var(--whiteColor)}
          .HeaderBOT #menu{width:calc((100% - 50px) /1)!important}
          .sp-header.activeDown.active .HeaderBg{top:-135px}
          .sp-header.active .HeaderBg{top:-75px}
        </b:if>
        <b:if cond='data:skin.vars.StykiHeadr == &quot;1px&quot;'>
          .HeaderBg{position:relative}
        </b:if>
        @media screen and (max-width: 1100px){.HTOPC, .HBOTC {width: 95%;}}
        <b:if cond='data:skin.vars.Style2Headr != &quot;3px&quot;'>
          @media screen and (max-width: 992px){
          .HeaderTOP,#menu{display:none}
          .HeaderBOT{top:0}
          .HeaderBg,.sp-header{height:92px}
          .HBOTC{height:92px}
          .HeaderBOT #logo,.HeaderTOP #logo{top:0}
          .open.nav1{display:flex!important}
          .sp-header.active .HBOTC{height:92px}
          .sp-header.active .HeaderBg{top:0;height:92px}
          }
        </b:if>
        <b:if cond='data:skin.vars.Style2Headr == &quot;3px&quot;'>
          @media screen and (max-width: 992px){
          .HeaderBOT,#menu,#topsocialL,#pages{display:none}
          #clicksearch,.open.nav1{display:flex!important;background:var(--whiteColor)!important}
          #clicksearch svg,.open.nav1 svg{stroke: #6600ff!important;}
          .HeaderBg,.sp-header{height:75px}
          .sp-header.active .HeaderBg{top:0}
          }
        </b:if>
      </b:if>

      .MegaItem .mega-wraper{position:absolute;right:0;left:0;width:100%;background:var(--Hbg);top:100%;transform:translateY(40px);visibility:hidden;opacity:0;border-radius:3px;border-top:2px solid var(--OldMin);box-shadow:0 0 5px 1px rgb(0 0 0 / 8%);z-index:2;padding:20px;transition:all .2s linear}
      .MegaPosts{height:260px!important;min-height:260px!important}
      .mega-wraper.Sp-posts3:before{content:&quot;&quot;;width:25px;height:25px;position:absolute;background:var(--Hbg);top:-13px;right:8%;border-radius:8px;transform:rotate(45deg);box-shadow:0 0 5px 1px rgb(0 0 0 / 8%);z-index:-1;border:2px solid var(--OldMin)}
      .mega-wraper.Sp-posts3&gt;div{background:var(--Hbg);border-radius:8px;padding:15px}
      .mega-wraper.Sp-posts2 .Posts-byCategory{grid-template-columns:repeat(4,1fr)}
      .mega-wraper.Sp-posts1 .thumb{padding-top:56.25%}
      .MegaItem{position:static!important}
      .MegaItem:hover .mega-wraper{display:block;transform:translateY(-2px);visibility:visible;opacity:1}
      .mega-wraper .thumb{display:block;width:90px;height:70px}
      .mega-wraper.Sp-posts3{right:auto;left:auto;width:300px;padding:0}
    </style>

    <b:if cond='data:blog.adsenseClientId'>&lt;!--</b:if>&lt;/head&gt;&lt;!--</head><b:if cond='!data:blog.adsenseClientId'>--&gt;</b:if>

  <body expr:class='data:blog.languageDirection' expr:data-id='data:blog.blogId'>
   <b:class cond='data:view.isHomepage' name='home'/>
    <b:class cond='data:view.isSingleItem' name='post'/>
    <b:class cond='data:view.isMultipleItems' name='lapel'/>
    <b:class cond='data:view.isPage' name='page'/>
    <b:class cond='data:skin.vars.MopileFasterVirsonFot == &quot;2px&quot;' name='AmopFot'/>
    <b:class cond='data:skin.vars.darckmoodF == &quot;2px&quot;' name='dark-mode'/>
    <b:class cond='data:skin.vars.darckmoodF == &quot;2px&quot;' name='dark-modex'/>
    <b:class cond='data:skin.vars.darckmoodF == &quot;1px&quot;' name='lite-modex'/>
    <b:class cond='data:blog.view == &quot;ReadMode&quot;' name='readMode'/>

    <input class='navI hidden' id='offNav' type='checkbox'/>
    <input class='navM hidden' id='NavM' type='checkbox'/>

    <b:if cond='data:skin.vars.darckmoodF == &quot;2px&quot;'>
      <script>/*<![CDATA[*/
document.body.classList.contains("dark-modex")&&"darck"!==localStorage.getItem("modex")&&(localStorage.setItem("modex","darck"),localStorage.removeItem("mode")),"light"===localStorage.getItem("mode")?(_$("body").classList.remove("dark-mode"),_$("html").setAttribute("mode", 'light')):(_$("body").classList.add("dark-mode"),_$("html").setAttribute("mode", 'dark'));
/*]]>*/</script>
      <b:else/>
      <script>/*<![CDATA[*/
document.body.classList.contains("lite-modex")&&"darck"===localStorage.getItem("modex")&&(localStorage.removeItem("modex"),localStorage.removeItem("mode")),"darkmode"===localStorage.getItem("mode")?(_$("body").classList.add("dark-mode"),_$("html").setAttribute("mode", 'dark')):(_$("body").classList.remove("dark-mode"),_$("html").setAttribute("mode", 'light'));
/*]]>*/</script>
    </b:if>

    <b:section class='hide' id='sitting' maxwidgets='1' showaddelement='no'>
      <b:widget id='BlogArchive400' locked='true' title='BlogArchive' type='BlogArchive' version='2' visible='true'>
        <b:widget-settings>
          <b:widget-setting name='showStyle'>HIERARCHY</b:widget-setting>
          <b:widget-setting name='yearPattern'>yyyy</b:widget-setting>
          <b:widget-setting name='showWeekEnd'>true</b:widget-setting>
          <b:widget-setting name='monthPattern'>MMMM</b:widget-setting>
          <b:widget-setting name='dayPattern'>MMM dd</b:widget-setting>
          <b:widget-setting name='weekPattern'>MM/dd</b:widget-setting>
          <b:widget-setting name='chronological'>false</b:widget-setting>
          <b:widget-setting name='showPosts'>true</b:widget-setting>
          <b:widget-setting name='frequency'>MONTHLY</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main'><b:tag name='script' type='text/javascript'>var PostCount=<b:eval expr='data:data map (d=&gt; d.post-count)'/>.reduce(function(a,b){return a+b});</b:tag></b:includable>
        <b:includable id='content'/>
        <b:includable id='flat'/>
        <b:includable id='hierarchy'/>
        <b:includable id='interval' var='intervals'/>
        <b:includable id='posts' var='posts'/>
      </b:widget>
      <b:widget id='Profile400' locked='true' title='BlogAuthors' type='Profile' version='2' visible='true'>
        <b:widget-settings>
          <b:widget-setting name='showaboutme'>true</b:widget-setting>
          <b:widget-setting name='showlocation'>true</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main'>
          <b:tag name='script' type='text/javascript'>
            let AuthorsInfo=new Object();
            <b:if cond='data:team'>
              <b:loop values='data:authors' var='author'>
                AuthorsInfo[&quot;<data:author.display-name/>&quot;] = {&quot;userUrl&quot;:&quot;<data:author.userUrl/>&quot;,&quot;name&quot;:&quot;<data:author.display-name/>&quot;,&quot;avatar&quot;:&quot;<b:include data='author' name='authorImageTeam'/>&quot;,};
              </b:loop>
              <b:else/>
              AuthorsInfo[&quot;<data:displayname/>&quot;] = {&quot;userUrl&quot;:&quot;<data:userUrl/>&quot;,&quot;name&quot;:&quot;<data:displayname/>&quot;,&quot;avatar&quot;:&quot;<b:include name='authorImageSingle'/>&quot;,};
            </b:if>
            AuthorsInfo.postAds = {};
          </b:tag>
        </b:includable>
        <b:includable id='authorImageSingle'><b:if cond='data:authorPhoto.image'><b:eval expr='resizeImage(data:authorPhoto.image, 1600)'/><b:else/>https://4.bp.blogspot.com/-ci3XMoAMGzg/WiCTxCLLWeI/AAAAAAAAPjI/UkV1sBTKC7EamOC_UmMJ4cQCv4xNNI82QCLcBGAs/s1600/log.jpg</b:if></b:includable>
        <b:includable id='authorImageTeam' var='author'><b:if cond='data:author.authorPhoto.image'><b:eval expr='resizeImage(data:author.authorPhoto.image, 1600)'/><b:else/>https://4.bp.blogspot.com/-ci3XMoAMGzg/WiCTxCLLWeI/AAAAAAAAPjI/UkV1sBTKC7EamOC_UmMJ4cQCv4xNNI82QCLcBGAs/s1600/log.jpg</b:if></b:includable>
        <b:includable id='authorProfileImage'/>
        <b:includable id='content'/>
        <b:includable id='defaultProfileImage'/>
        <b:includable id='profileImage'/>
        <b:includable id='teamProfile'/>
        <b:includable id='teamProfileLink'/>
        <b:includable id='userGoogleProfile'/>
        <b:includable id='userLocation'/>
        <b:includable id='userProfile'/>
        <b:includable id='userProfileData'/>
        <b:includable id='userProfileImage'/>
        <b:includable id='userProfileInfo'/>
        <b:includable id='userProfileLink'/>
        <b:includable id='userProfileText'/>
        <b:includable id='viewProfileLink'/>
      </b:widget>
      <b:widget id='Label400' locked='true' title='BlogLabels' type='Label' version='2' visible='true'>
        <b:widget-settings>
          <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
          <b:widget-setting name='display'>LIST</b:widget-setting>
          <b:widget-setting name='selectedLabelsList'/>
          <b:widget-setting name='showType'>ALL</b:widget-setting>
          <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main' var='this'><b:if cond='data:labels'><script>var _bl=<b:eval expr='data:labels map (l =&gt; l.name.jsEscaped + &quot;:&quot; + l.count)'/></script><b:else/><script>var _bl={Labels:0}</script></b:if></b:includable>
        <b:includable id='cloud'/>
        <b:includable id='content'/>
        <b:includable id='list'/>
      </b:widget>
    </b:section>

    <b:if cond='data:view.isPreview'>
      <b:if cond='!data:view.isSingleItem'>
        <div class='isPreview' style=' position: fixed; top: 0; right: 0; left: 0; bottom: 0; display: flex; align-items: center; justify-content: center; font-size: 25px; font-family: sans-serif !important; '>
          نموذج المعاينة يعمل فقط للمقالات والصفحات
        </div>
        <style>
          .contenarpage {display: none;}
        </style>
      </b:if>
    </b:if>
    <div class='contenarpage'>

      <b:if cond='!data:view.search.query'>
        <div class='TEMPsittings hide'>
          <b:section class='hide' id='lazy' maxwidgets='1' showaddelement='no'>
            <b:widget id='HTML001' locked='true' title='تأجيل الاعلانات' type='HTML' version='2' visible='false'>
              <b:widget-settings>
                <b:widget-setting name='content'/>
              </b:widget-settings>
              <b:includable id='main'><b:tag name='script' type='text/javascript'>LazyAdsense = true;AdsenseUrl = &#39;<data:content/>&#39;;function Lazy(){if(LazyAdsense){LazyAdsense = false;var Adsensecode = document.createElement(&#39;script&#39;);Adsensecode.src = AdsenseUrl;Adsensecode.async = true;Adsensecode.crossOrigin = &#39;anonymous&#39;;document.head.appendChild(Adsensecode)}}</b:tag></b:includable>
            </b:widget>
          </b:section>
          <b:if cond='data:view.isLayoutMode'><b:include name='customeIcons'/></b:if>
          <b:if cond='data:view.isLayoutMode'><b:include name='customeAnalytics'/></b:if>
          <b:if cond='data:view.isLayoutMode'><b:include name='HeaderSearch'/></b:if>
          <b:include name='MopileMenuLogo'/>
          <b:if cond='data:view.isLayoutMode'><b:include name='ArticaleSittings'/></b:if>
          <b:if cond='data:view.isLayoutMode'><b:include name='CommentSittings'/></b:if>
        </div>
      </b:if>
      <!-- start header -->
      <header class='sp-header' id='sp-header'>
        <b:class cond='data:skin.vars.StykiHeadr == &quot;2px&quot;' name='StikyHead'/>
        <b:if cond='data:skin.vars.Style2Headr == &quot;1px&quot; or data:skin.vars.Style2Headr == &quot;2px&quot;'>
          <div class='HeaderBg'>
            <div class='HeaderTOP'>
              <div class='Headerplace'>
                <div class='HTOPC'>
                  <b:include name='HeaderPages'/>
                  <b:include name='HeaderIcons'/>
                </div>
              </div>
            </div>
            <div class='HeaderBOT'>
              <div class='HBOTC'>
                <label aria-label='القائمة الرئيسي' class='open nav1' for='NavM' id='navMopile' onclick='openSidenav()'><svg class='line' viewBox='0 0 24 24'><line x1='3' x2='21' y1='12' y2='12'/><line x1='3' x2='21' y1='5' y2='5'/><line x1='3' x2='21' y1='19' y2='19'/></svg></label>
                <b:include name='HeaderLogo'/>
                <b:include name='HeaderLinks'/>
                <label aria-label='بحث' class='search' for='NavC' id='clicksearch'><svg class='line'><use href='#ic-search'/></svg></label>
              </div>
            </div>
          </div>
        </b:if>
        <b:if cond='data:skin.vars.Style2Headr == &quot;3px&quot;'>
          <div class='HeaderBg'>
            <div class='HeaderTOP'>
              <div class='Headerplace'>
                <div class='HTOPC'>
                  <label aria-label='القائمة الرئيسي' class='open nav1' for='NavM' id='navMopile' onclick='openSidenav()'><div class='lines'>
  <span class='line1'/>
  <span class='line2'/>
  <span class='line3'/>
</div>
</label>
                  <div class='HRS'>
                    <b:include name='HeaderLogo'/>
                    <b:include name='HeaderPages'/>
                  </div>
                  <b:include name='HeaderIcons'/>
                  <label aria-label='بحث' class='searchHide' for='NavC' id='clicksearch'><svg class='line'><use href='#ic-search'/></svg></label>
                </div>
              </div>
            </div>
            <div class='HeaderBOT'>
              <div class='HBOTC'>
                <b:include name='HeaderLinks'/>
                <label aria-label='بحث' class='search' for='NavC' id='clicksearch'><svg class='line'><use href='#ic-search'/></svg></label>
              </div>
            </div>
          </div>
        </b:if>
        <!-- N** H***** -->
        <b:if cond='data:view.isLayoutMode'><b:include name='HeaderAds'/></b:if>

      </header>

      <!-- Header markups -->
      <b:defaultmarkups>
        <b:defaultmarkup type='Common'>
          <b:includable id='MopileMenuLogo'>
            <b:section id='MopileMenuLogo' maxwidgets='1' showaddelement='no'>
              <b:widget id='Image002' locked='true' title='موقع كوتشينا' type='Image' version='2' visible='false'>
                <b:widget-settings>
                  <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/a/AVvXsEik9wA2l4LGAmhSGsefqdy8i1fD1snHf0M-iA-kDbmBnCNhy4uhifV3ys0AiZ10botSlCErjiprVJuUbCKRZG8n_-DakHGg57agGxuGd8ReD5wqieT-RnlFzQMojy3sqKRDWkDuPxtqNeI7Nw-NOSvpYNGJe4GwWKPGUZxM32dBqfeq3Ywf-5X-joWvCg=s308</b:widget-setting>
                  <b:widget-setting name='displayHeight'>73</b:widget-setting>
                  <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                  <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                  <b:widget-setting name='displayWidth'>308</b:widget-setting>
                  <b:widget-setting name='link'>https://blogger.googleusercontent.com/img/a/AVvXsEik9wA2l4LGAmhSGsefqdy8i1fD1snHf0M-iA-kDbmBnCNhy4uhifV3ys0AiZ10botSlCErjiprVJuUbCKRZG8n_-DakHGg57agGxuGd8ReD5wqieT-RnlFzQMojy3sqKRDWkDuPxtqNeI7Nw-NOSvpYNGJe4GwWKPGUZxM32dBqfeq3Ywf-5X-joWvCg=s308</b:widget-setting>
                  <b:widget-setting name='caption'/>
                </b:widget-settings>
                <b:includable id='main'><b:if cond='data:sourceUrl'><i class='hide dataheader' expr:site-dis='data:caption' expr:site-logo='data:sourceUrl' expr:site-title='data:title'/></b:if></b:includable>
                <b:includable id='content'/>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderLogo'>
            <b:section id='logo' maxwidgets='1' showaddelement='no'>
              <b:widget id='Header1' locked='true' title='للللللل (رأس الصفحة)' type='Header' version='1'>
                <b:widget-settings>
                  <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/a/AVvXsEiWuuXgWwdJnPuIlZkx7oYBB2jKJAuSbrm6phcvUD4VkeTAXnhbJHroqAzn5Pb1j-9kEk-jx8uUCP8ZZydqARy5qHpcWJ9Yri27A9J_3uas6BtEoE9Ia2zplr5DAQxPsdtehVN8gL4c5N0qvJp7nroDiwbffoqgGsgYReJMU5cnmMXqiufayueEI9CgO5CD=s250</b:widget-setting>
                  <b:widget-setting name='displayHeight'>70</b:widget-setting>
                  <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                  <b:widget-setting name='useImage'>true</b:widget-setting>
                  <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                  <b:widget-setting name='imagePlacement'>BEHIND</b:widget-setting>
                  <b:widget-setting name='displayWidth'>250</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:include name='content'/></b:includable>
                <b:includable id='behindImageStyle'/>
                <b:includable id='content'><div id='header-inner'><b:if cond='data:useImage'><a class='img-logo' expr:href='data:blog.homepageUrl' expr:title='data:blog.title' style='display: flex'><b:if cond='data:sourceUrl'><img expr:alt='data:blog.title' expr:src='data:sourceUrl' expr:title='data:blog.title' height='70' id='Header1_headerimg' width='250'/></b:if></a><b:if cond='data:view.isHomepage'><h1 style='display: none'><data:blog.title/></h1><b:else/><h2 style='display: none'><data:blog.title/></h2></b:if><b:else/><div class='titlewrapper'><b:include name='title'/><b:include name='description'/></div></b:if></div></b:includable>
                <b:includable id='description'><p class='descriptionwrapper' style='display: none'><data:description/></p></b:includable>
                <b:includable id='image'>
                  <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
                    <b:include data='{image: data:image,altText: data:blog.title.escaped,originalWidth: data:width,originalHeight: data:height}' name='responsiveImage'/>
                  </a>
                </b:includable>
                <b:includable id='title'><b:if cond='data:view.isHomepage'><h1 class='title'><a expr:href='data:blog.homepageUrl' expr:title='data:blog.title'><data:title/></a></h1><b:else/><h2 class='title'><a expr:href='data:blog.homepageUrl' expr:title='data:blog.title'><data:title/></a></h2></b:if></b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderPages'>
            <b:section id='pages' maxwidgets='1' showaddelement='no'>
              <b:widget id='PageList1' locked='true' title='الصفحات' type='PageList' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='pageListJson'>{}</b:widget-setting>
                  <b:widget-setting name='homeTitle'>الصفحة الرئيسية</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:include name='content'/></b:includable>
                <b:includable id='content'><div class='widget-content'><b:include name='pageList'/></div></b:includable>
                <b:includable id='overflowButton'/>
                <b:includable id='overflowablePageList'/>
                <b:includable id='pageLink'><li><b:class cond='data:view.url==data:link.href or data:blog.url==data:link.href' name='selected'/><a expr:href='data:link.href'><data:link.title/></a></li></b:includable>
                <b:includable id='pageList'><ul><b:class cond='data:pageListClass' expr:name='data:pageListClass'/><b:loop values='data:links' var='link'><b:include name='pageLink'/></b:loop></ul></b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderIcons'>
            <b:section id='topsocialL' maxwidgets='1' showaddelement='no'>
              <b:widget id='LinkList3' locked='true' title='مواقع التواصل الإجتماعي' type='LinkList' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='shownum'>4</b:widget-setting>
                  <b:widget-setting name='sorting'>NONE</b:widget-setting>
                  <b:widget-setting name='text-0'>https://www.facebook.com/</b:widget-setting>
                  <b:widget-setting name='link-0'>https://www.facebook.com/profile.php?id=100084100745794</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:include name='content'/></b:includable>
                <b:includable id='AUTH'/>
                <b:includable id='DEF'/>
                <b:includable id='content'><ul class='social-static social'><b:loop values='data:links' var='link'><li><a expr:href='data:link.target' expr:title='data:link.name' rel='nofollow noopener' target='_blank'><svg><use expr:href='&quot;#ic-&quot; + data:link.name'/></svg></a></li></b:loop></ul></b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderLinks'>
            <b:section id='menu' maxwidgets='1' showaddelement='no'>
              <b:widget id='LinkList001' locked='true' title='القائمة الرئيسية' type='LinkList' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='link-5'>https://cot12a.blogspot.com/</b:widget-setting>
                  <b:widget-setting name='link-6'>https://cot12a.blogspot.com/</b:widget-setting>
                  <b:widget-setting name='link-3'>https://cot12a.blogspot.com/search/label/%D8%AA%D8%AD%D8%B3%D9%8A%D9%86%20%D9%85%D8%AD%D8%B1%D9%83%D8%A7%D8%AA%20%D8%A7%D9%84%D8%A8%D8%AD%D8%AB%20%28SEO%29</b:widget-setting>
                  <b:widget-setting name='link-4'>https://cot12a.blogspot.com/search/label/%D9%82%D9%88%D8%A7%D9%84%D8%A8%20%D8%A8%D9%84%D9%88%D8%AC%D8%B1</b:widget-setting>
                  <b:widget-setting name='text-1'>الربح من الأنترنت</b:widget-setting>
                  <b:widget-setting name='text-0'>تطبيقات</b:widget-setting>
                  <b:widget-setting name='text-3'>تحسين محركات البحث (SEO)</b:widget-setting>
                  <b:widget-setting name='text-2'>الربح من بلوجر</b:widget-setting>
                  <b:widget-setting name='text-5'>+محركات البحث</b:widget-setting>
                  <b:widget-setting name='text-4'>قوالب بلوجر</b:widget-setting>
                  <b:widget-setting name='text-6'>+الجديد</b:widget-setting>
                  <b:widget-setting name='sorting'>NONE</b:widget-setting>
                  <b:widget-setting name='link-1'>https://cot12a.blogspot.com/search/label/%D8%A7%D9%84%D8%B1%D8%A8%D8%AD%20%D9%85%D9%86%20%D8%A7%D9%84%D8%A3%D9%86%D8%AA%D8%B1%D9%86%D8%AA</b:widget-setting>
                  <b:widget-setting name='link-2'>https://cot12a.blogspot.com/search/label/%D8%A7%D9%84%D8%B1%D8%A8%D8%AD%20%D9%85%D9%86%20%D8%A8%D9%84%D9%88%D8%AC%D8%B1?m=1</b:widget-setting>
                  <b:widget-setting name='link-0'>https://cot12a.blogspot.com/search/label/%D8%AA%D8%B7%D8%A8%D9%8A%D9%82%D8%A7%D8%AA</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:include name='content'/></b:includable>
                <b:includable id='AUTH'/>
                <b:includable id='DEF'/>
                <b:includable id='content'>
                  <div class='widget-content'>
                    <ul>

                      <b:loop index='index' values='data:links' var='link'>
                        <b:if cond='data:link.name contains &quot;+&quot;'>
                          <b:if cond='data:link.name contains &quot;++&quot;'>
                            <li class='ssitem'><a expr:href='data:link.target' expr:title='data:link.name'><data:link.name/></a></li>
                            <b:else/>
                            <b:if cond='data:index != 0'>
                              <b:eval expr='data:links[data:index - 1].name contains &quot;+&quot; ? &quot;&lt;/ul&gt;&lt;/li&gt;&quot; : &quot;&quot;'/>
                            </b:if>
                            &lt;li class=&#39;sitem&#39;&gt;
                            <a expr:href='data:link.target' expr:title='data:link.name'><data:link.name/></a>
                            <b:eval expr='data:links[data:index + 1].name contains &quot;+&quot; ? &quot;&lt;ul&gt;&quot; : &quot;&lt;/li&gt;&quot;'/>
                          </b:if>
                          <b:else/>
                          <b:if cond='data:index != 0'>
                            <b:eval expr='data:links[data:index - 1].name contains &quot;++&quot; ? &quot;&lt;/ul&gt;&lt;/li&gt;&quot; : &quot;&quot;'/>
                            <b:eval expr='&quot;&lt;/ul&gt;&lt;/li&gt;&quot;'/>
                          </b:if>
                          <!-- start -->
                          <b:if cond='data:link.target contains &quot;MegaStyle&quot; and data:link.target.size &gt; 1'>
                            &lt;li class=&#39;item MegaItem fullwide&#39;&gt;
                            <a expr:href='data:link.target' expr:title='data:link.name'> <data:link.name/> </a>
                            <div class='mega-wraper'><b:class cond='data:link.target contains &quot;Mega3&quot;' name='Sp-posts2'/><b:class cond='data:link.target contains &quot;Mega2&quot;' name='Sp-posts1'/><b:class cond='data:link.target contains &quot;Mega1&quot;' name='Sp-posts3'/><div class='MegaPosts' data-index='1' data-number='4'/></div>
                            <b:else/>
                            &lt;li class=&#39;item&#39;&gt;
                            <a expr:href='data:link.target' expr:title='data:link.name'><b:class cond='data:view.url==data:link.target or data:blog.url==data:link.target' name='selected'/><data:link.name/></a>
                          </b:if>
                          <!-- start -->
                          <b:eval expr='data:index+1 == data:links.length ? &quot;&lt;/li&gt;&quot; : &quot;&lt;ul&gt;&quot;'/>
                        </b:if>
                      </b:loop>
                    </ul>
                  </div>

                </b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderAds'>
            <b:section class='HAD' cond='!data:view.isError and !data:blog.isMobileRequest' id='Topa3lan-sc' maxwidgets='1' showaddelement='no'>
              <b:widget id='HTML100' locked='true' title='اعلان اسفل القائمة العلوية للحاسوب' type='HTML' version='2' visible='false'>
                <b:widget-settings>
                  <b:widget-setting name='content'/>
                </b:widget-settings>
                <b:includable id='main'><div class='SeoPlusAds'><data:content/></div></b:includable>
              </b:widget>
            </b:section>
            <b:section cond='not data:view.isError and data:blog.isMobileRequest' id='Topa3lan-sc2' maxwidgets='1' showaddelement='no'>
              <b:widget id='HTML101' locked='true' title='اعلان اسفل القائمة العلوية للهاتف' type='HTML' version='2' visible='false'>
                <b:widget-settings>
                  <b:widget-setting name='content'/>
                </b:widget-settings>
                <b:includable id='main'><div class='SeoPlusAds'><data:content/></div></b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='HeaderSearch'>
            <div class='searchformbox'>
              <div class='fxbox'>
                <b:section id='searchform' maxwidgets='2' showaddelement='no'>
                  <b:widget id='BlogSearch2' locked='true' title='بحث ...' type='BlogSearch' version='2' visible='true'>
                    <b:includable id='main'>
                      <form class='sharef' expr:action='data:blog.searchUrl' role='search' target='_top'>
                        <label class='sp' for='searchIn'>
                          <svg class='line'><use href='#ic-search'/></svg>
                        </label>
                        <input autocomplete='off' expr:aria-label='data:messages.searchThisBlog' expr:placeholder='data:title' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' id='searchIn' minlength='3' name='q' required='required' type='search'/>
                        <button aria-label='Clear' class='sp' data-text='حذف' type='reset'/>
                      </form>
                      <label aria-label='Close' class='searchC' for='NavC'/>
                      <b:if cond='data:view.isHomepage'><b:tag name='script' type='application/ld+json'>{&quot;@context&quot;: &quot;http://schema.org&quot;,&quot;@type&quot;: &quot;WebSite&quot;,&quot;url&quot;: &quot;<data:blog.homepageUrl/>&quot;,&quot;potentialAction&quot;: [{&quot;@type&quot;: &quot;SearchAction&quot;,&quot;target&quot;: &quot;<data:blog.searchUrl/>?q={search_term_string}&quot;,&quot;query-input&quot;: &quot;required name=search_term_string&quot;}]}</b:tag></b:if>
                    </b:includable>
                    <b:includable id='content'/>
                    <b:includable id='searchForm'/>
                    <b:includable id='searchSubmit'/>
                  </b:widget>
                  <b:widget id='Label002' locked='true' title='أقسام الوصول السريع ( مربع البحث )' type='Label' version='2' visible='true'>
                    <b:widget-settings>
                      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                      <b:widget-setting name='display'>LIST</b:widget-setting>
                      <b:widget-setting name='selectedLabelsList'/>
                      <b:widget-setting name='showType'>ALL</b:widget-setting>
                      <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
                    </b:widget-settings>
                    <b:includable id='main' var='this'>
                      <b:include name='widget-title'/>
                      <div class='widget-content cloud-label-widget-content'>
                        <b:loop index='m' values='data:labels' var='label'>
                          <b:if cond='data:m &lt;= 20'>
                            <span class='label-size'>
                              <a class='label-name' expr:href='data:label.url'>
                                <data:label.name/>
                                <b:if cond='data:this.showFreqNumbers'>
                                  <span class='label-count'><data:label.count/></span>
                                </b:if>
                              </a>
                            </span>
                          </b:if>
                        </b:loop>
                      </div>
                    </b:includable>
                    <b:includable id='cloud'/>
                    <b:includable id='content'/>
                    <b:includable id='list'/>
                  </b:widget>
                </b:section>
              </div>
             <label class='fCls searchbg' for='NavC'/>

            </div>
          </b:includable>
          <b:includable id='post-commentDisqus'>

            <div id='disqus_thread'/>
            <script>

              /*<![CDATA[*/
function load_disqus(){$getScript("//"+_$("#disqus-id").getAttribute('content')+".disqus.com/embed.js",()=>{_$(".BloggerComment").style.display="none",_$(".DisqusComment").style.display="block",_$(".FacebookComment").style.display="none",console.clear(),document.querySelectorAll(".cshow").forEach(s=>{s.classList.remove("active"),s.classList.contains("disqus")&&s.classList.add("active")})})}
/* load_disqus() */
/*]]>*/</script>
          </b:includable>
          <b:includable id='post-commentFB'>        
            <div id='fb-root'/>
            <div id='commentFB'><div class='fb-comments facebookcmt' expr:href='data:post.url' num_posts='10' width='100%'/></div>

            <script>/*<![CDATA[*/
function load_facebook(){var e="ar"===BlogLang?"ar_AR":"es"===BlogLang?"es_LA":"en"===BlogLang?"en_US":-1==BlogLang.indexOf("_")?BlogLang.toLowerCase()+"_"+BlogLang.toUpperCase():BlogLang;$getScript("//connect.facebook.net/"+e+"/sdk.js",function(){W=!0,FB.init({appId:_$('meta[property="fb:app_id"]').getAttribute("content"),version:"v3.3"}),FB.XFBML.parse(),_$(".BloggerComment").style.display="none",_$(".DisqusComment").style.display="none",_$(".FacebookComment").style.display="block",console.clear(),document.querySelectorAll(".cshow").forEach(e=>{e.classList.remove("active"),e.classList.contains("facebook")&&e.classList.add("active")})})}
        /*]]>*/</script>
          </b:includable>
          <b:includable id='CommentSittings'>        
            <b:section id='sitteng-menu hide' maxwidgets='1' showaddelement='false'>
                      <b:widget id='TextList88' locked='true' title='قائمة التعليقات' type='TextList' version='2' visible='false'>
                        <b:widget-settings>
                          <b:widget-setting name='shownum'>3</b:widget-setting>
                          <b:widget-setting name='sorting'>NONE</b:widget-setting>
                          <b:widget-setting name='item-2'>Disqus</b:widget-setting>
                          <b:widget-setting name='item-1'>Facebook</b:widget-setting>
                          <b:widget-setting name='item-0'>Blogger</b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main'>
                  <b:include name='content'/>
                </b:includable>
                        <b:includable id='content'><script>_$(&#39;.commentsShow&#39;).innerHTML = &quot;<b:loop index='m' values='data:items' var='item'><b:if cond='data:m &lt;= 2'><b:if cond='data:item == &quot;Blogger&quot;'><span class='cshow blogger'>تعليقات Blogger</span><b:elseif cond='data:item == &quot;Facebook&quot;'/><span class='cshow facebook' onclick='load_facebook()'>تعليقات Facebook</span><b:elseif cond='data:item == &quot;Disqus&quot;'/><span class='cshow disqus' onclick='load_disqus()'>تعليقات Disqus</span></b:if></b:if></b:loop>&quot;;
                  <b:loop index='m' values='data:items' var='item'><b:if cond='data:m == 0'><b:if cond='data:item == &quot;Blogger&quot;'>commentjs = &#39;bloggerjs&#39;;<b:elseif cond='data:item == &quot;Facebook&quot;'/>commentjs = &#39;facebookjs&#39;;<b:elseif cond='data:item == &quot;Disqus&quot;'/>commentjs = &#39;disqusjs&#39;;</b:if></b:if></b:loop></script>
                </b:includable>
                      </b:widget>
                    </b:section>
          </b:includable>
          <b:includable id='ArticaleSittings'>
            <b:section id='AddOns' maxwidgets='1' showaddelement='no'>
              <b:widget id='LinkList500' locked='true' title='ميزة تحويل الروابط الخارجية' type='LinkList' version='2' visible='true'>
                <b:includable id='main'><b:if cond='data:view.isSingleItem'>
                  <b:tag name='script' type='text/javascript'>
                    Settingsredirect={
                    <b:loop values='data:links' var='link'>&#39;<data:link.name/>&#39; : <b:if cond='data:link.target in {&quot;true&quot;,&quot;false&quot;}'><data:link.target/><b:else/>&#39;<data:link.target.jsEscaped/>&#39;</b:if>,</b:loop>};

                    let page_redirect = void 0 !== Settingsredirect[&quot;page-url&quot;] ? Settingsredirect[&quot;page-url&quot;] : &quot;noNamePage&quot;,
                    redirect_T_Configure = void 0 !== Settingsredirect[&quot;text-Configure&quot;] ? Settingsredirect[&quot;text-Configure&quot;] : configtxt,
                    redirect_T_ready = void 0 !== Settingsredirect[&quot;text-ready&quot;] ? Settingsredirect[&quot;text-ready&quot;] : redytxt,
                    redirect_T_err = void 0 !== Settingsredirect[&quot;text-err&quot;] ? Settingsredirect[&quot;text-err&quot;] : errtxt,
                    redirect_timer = void 0 !== Settingsredirect[&quot;redirect_timer&quot;] ? Settingsredirect[&quot;redirect_timer&quot;] : &quot;10&quot;,
                    redirect_match = void 0 !== Settingsredirect[&quot;Block-Site&quot;] ? Settingsredirect[&quot;Block-Site&quot;] : &quot;fulaxcbontent&quot;,
                    button = void 0 !== Settingsredirect[&quot;button&quot;] ? Settingsredirect[&quot;button&quot;] : true,
                    skin = void 0 !== Settingsredirect[&quot;skin&quot;] ? Settingsredirect[&quot;skin&quot;] : false;
                    popup = void 0 !== Settingsredirect[&quot;popup&quot;] ? Settingsredirect[&quot;popup&quot;] : false;
                    protection = void 0 !== Settingsredirect[&quot;protection&quot;] ? Settingsredirect[&quot;protection&quot;] : true;
                    skinclass = void 0 !== Settingsredirect[&quot;skinclass&quot;] == &#39;1&#39; ? &quot;ln&quot; : &quot;out&quot; ;

                  </b:tag><b:if cond='data:view.isPage'><script id='PageRedirect'>/*<![CDATA[*/const _0x4ed6bd=_0x2698,_0x2b1ba1=_0x5cb5;function _0x1705(){const _0x4d5a86=['axVcNMC9','oSoRACoEW655c8kQiq','WP4Zedikbmofadq','W73cMZDSASkSqSkwW4/dLs/cMCk5','gfpcOrffq0lcL0NdQgTBW6JcS8kbW7OvW7X4WPiBbvGItSkyzrbCWRVcQfviW7JdGCoBxrVdGgH9W47dUCkRWRG6WR7cU0hdQ2bQA8kZW6iQWRRcRdytW6SOW48etmoCgSkzESoYFCouaSkyjmk3f8k1CmoXmSoOWOFcKCkshrJdUmo9WONcISoeWR7dVSkhjxeTyJalW5rTc8kAWRniesNdKCogsmkKFLpcJLFdG8oRf03cQCojWQRcPSkXW6W9eCoAwHFdKmo1WQiyDmkknKL+WO4fBGm8dMVcTZRdTYT0g2lcHmk6bM/cN3CUCmkzW7StW5bjW6lcVmoHAubGWQCdrCkLW40NzSoDCv58adP1W7DhWPecWRtcJ8oxycDNW5NdGmoCBCkdWP7dISktWRTsWRxdUZbCc8owW6JdU8o1wNZdKmk4W6/cPmkxs8kEEZrNW5jNvuhcRbv5W4BdPSoFaSkHxmkDmrBcN8kYD8owECkOW6DabCkSWPVcOmkGaZncwmowc8oDWQtdLCkBk8oKyutcMSouW6r4W6WQcaJdUmo8hCkpfvRcOqNdS0WIW71FWRjAWRddJZNdSCkXCSouWQ3dV8os','mtK5mdu5EvzvtMTe','WRPcWRFdKSoMz8kAWRzdvN8Y','W7pdS8kYW7BcOSkCW6FcUb1gWObXua','mtbqq1bVtfu','W7xdR8o4mSk8W6ZcJttdIa','k8k9WPZdUHBdSqldJ8oQWOu','CMvTB3zL','Aw5Zzxj0qwrQywnLBNrive1m','mtboDMzArgW','DxjS','W6KjDmkSx8koW7S','pc9HpJWVzgL2pG','AhjLzG','CMvTB3zLsxrLBq','lMncDxr0B24GlMvYCG','lMncDxr0B24GlNjLywr5','ntKWmZG2ohv2zgn5Aq','W6/dMCoEcrnUdCkBWRbzDSoyWQC','BM9vCMW','WOhdLSopW7KcxmkckG','z2v0sxrLBq','FCkVmG','mte3nZr6uK5xA2O','AgLKzq','W41MDr0BketdNfxcNt4aWOG','W4bXjSkzWOxdL8o8W4hcGwD8','W47dSmonj8oPt2tcOb/dNITyxG','C3rYB2TLrgfZAg9MzNnLDa','pc9HpJXHihrHCMDLDd0Ix2jSyw5RiIbJBgfZCZ0Iy0XPBMSGCMvHzhKGAgLKzsbUB3jLzgKIihjLBd0IBM9MB2XSB3CGBM9YzwzLCNjLCIiGAhjLzJ0IAMf2yxnJCMLWDdO7iJ4','mJG3nJeZD2nNtKv5','W7rlW7K','ndHUsNjvCM8','mZaZndm3mJbXCg9Wz0q','C2vHCMnO','i3bHz2vYzwrPCMvJDa','WPVcRmkwEmkSeG','pc9IpJWVzgL2pJXKAxyGy2XHC3m9iMncDxr0B24IpJXHignSyxnZpsjJtgLUAYbSB2rLCIbUB3jLzgKIigHYzwy9iMPHDMfZy3jPChq6oYiGCMvSpsjUB2zVBgXVDYbUB3jLzMvYCMvYiJ4','C2v0qxr0CMLIDxrL','Aw5Uzxjive1m'];_0x1705=function(){return _0x4d5a86;};return _0x1705();}function _0x2698(_0x5eee44,_0x4f2a6e){const _0x1705e7=_0x1705();return _0x2698=function(_0x5cb5f5,_0x58859d){_0x5cb5f5=_0x5cb5f5-0x1ad;let _0x13ecd9=_0x1705e7[_0x5cb5f5];if(_0x2698['qiDBuG']===undefined){var _0x34c6d0=function(_0x269804){const _0x283f6d='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x627185='',_0x3ac83c='';for(let _0x47261d=0x0,_0xaaa314,_0x22814d,_0x33e795=0x0;_0x22814d=_0x269804['charAt'](_0x33e795++);~_0x22814d&&(_0xaaa314=_0x47261d%0x4?_0xaaa314*0x40+_0x22814d:_0x22814d,_0x47261d++%0x4)?_0x627185+=String['fromCharCode'](0xff&_0xaaa314>>(-0x2*_0x47261d&0x6)):0x0){_0x22814d=_0x283f6d['indexOf'](_0x22814d);}for(let _0x241029=0x0,_0x1a82b8=_0x627185['length'];_0x241029<_0x1a82b8;_0x241029++){_0x3ac83c+='%'+('00'+_0x627185['charCodeAt'](_0x241029)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x3ac83c);};_0x2698['fneuVf']=_0x34c6d0,_0x5eee44=arguments,_0x2698['qiDBuG']=!![];}const _0x3952fb=_0x1705e7[0x0],_0x51bebe=_0x5cb5f5+_0x3952fb,_0x424383=_0x5eee44[_0x51bebe];return!_0x424383?(_0x13ecd9=_0x2698['fneuVf'](_0x13ecd9),_0x5eee44[_0x51bebe]=_0x13ecd9):_0x13ecd9=_0x424383,_0x13ecd9;},_0x2698(_0x5eee44,_0x4f2a6e);}(function(_0x13750f,_0xa7ff2b){const _0x328bc0=_0x2698,_0x5c4137=_0x5cb5,_0x468427=_0x13750f();while(!![]){try{const _0x43e0fa=-parseInt(_0x5c4137(0x1d2,'s)(f'))/0x1+parseInt(_0x328bc0(0x1bb))/0x2*(-parseInt(_0x5c4137(0x1d5,'dr5k'))/0x3)+parseInt(_0x5c4137(0x1cf,'752u'))/0x4*(parseInt(_0x328bc0(0x1d4))/0x5)+-parseInt(_0x328bc0(0x1b5))/0x6+parseInt(_0x328bc0(0x1d1))/0x7*(parseInt(_0x328bc0(0x1c4))/0x8)+-parseInt(_0x5c4137(0x1bf,'#]!N'))/0x9+-parseInt(_0x328bc0(0x1ad))/0xa*(-parseInt(_0x328bc0(0x1c5))/0xb);if(_0x43e0fa===_0xa7ff2b)break;else _0x468427['push'](_0x468427['shift']());}catch(_0x539827){_0x468427['push'](_0x468427['shift']());}}}(_0x1705,0x8ffe0));function _0x5cb5(_0x5eee44,_0x4f2a6e){const _0x1705e7=_0x1705();return _0x5cb5=function(_0x5cb5f5,_0x58859d){_0x5cb5f5=_0x5cb5f5-0x1ad;let _0x13ecd9=_0x1705e7[_0x5cb5f5];if(_0x5cb5['BUoQce']===undefined){var _0x34c6d0=function(_0x283f6d){const _0x627185='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';let _0x3ac83c='',_0x47261d='';for(let _0xaaa314=0x0,_0x22814d,_0x33e795,_0x241029=0x0;_0x33e795=_0x283f6d['charAt'](_0x241029++);~_0x33e795&&(_0x22814d=_0xaaa314%0x4?_0x22814d*0x40+_0x33e795:_0x33e795,_0xaaa314++%0x4)?_0x3ac83c+=String['fromCharCode'](0xff&_0x22814d>>(-0x2*_0xaaa314&0x6)):0x0){_0x33e795=_0x627185['indexOf'](_0x33e795);}for(let _0x1a82b8=0x0,_0x466e41=_0x3ac83c['length'];_0x1a82b8<_0x466e41;_0x1a82b8++){_0x47261d+='%'+('00'+_0x3ac83c['charCodeAt'](_0x1a82b8)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x47261d);};const _0x269804=function(_0x7ea7cf,_0x3695c6){let _0x2f713f=[],_0x2d04a5=0x0,_0x3bfa80,_0x52d4b1='';_0x7ea7cf=_0x34c6d0(_0x7ea7cf);let _0x4ec71e;for(_0x4ec71e=0x0;_0x4ec71e<0x100;_0x4ec71e++){_0x2f713f[_0x4ec71e]=_0x4ec71e;}for(_0x4ec71e=0x0;_0x4ec71e<0x100;_0x4ec71e++){_0x2d04a5=(_0x2d04a5+_0x2f713f[_0x4ec71e]+_0x3695c6['charCodeAt'](_0x4ec71e%_0x3695c6['length']))%0x100,_0x3bfa80=_0x2f713f[_0x4ec71e],_0x2f713f[_0x4ec71e]=_0x2f713f[_0x2d04a5],_0x2f713f[_0x2d04a5]=_0x3bfa80;}_0x4ec71e=0x0,_0x2d04a5=0x0;for(let _0x568cf1=0x0;_0x568cf1<_0x7ea7cf['length'];_0x568cf1++){_0x4ec71e=(_0x4ec71e+0x1)%0x100,_0x2d04a5=(_0x2d04a5+_0x2f713f[_0x4ec71e])%0x100,_0x3bfa80=_0x2f713f[_0x4ec71e],_0x2f713f[_0x4ec71e]=_0x2f713f[_0x2d04a5],_0x2f713f[_0x2d04a5]=_0x3bfa80,_0x52d4b1+=String['fromCharCode'](_0x7ea7cf['charCodeAt'](_0x568cf1)^_0x2f713f[(_0x2f713f[_0x4ec71e]+_0x2f713f[_0x2d04a5])%0x100]);}return _0x52d4b1;};_0x5cb5['YEbUZq']=_0x269804,_0x5eee44=arguments,_0x5cb5['BUoQce']=!![];}const _0x3952fb=_0x1705e7[0x0],_0x51bebe=_0x5cb5f5+_0x3952fb,_0x424383=_0x5eee44[_0x51bebe];return!_0x424383?(_0x5cb5['kAnjsK']===undefined&&(_0x5cb5['kAnjsK']=!![]),_0x13ecd9=_0x5cb5['YEbUZq'](_0x13ecd9,_0x58859d),_0x5eee44[_0x51bebe]=_0x13ecd9):_0x13ecd9=_0x424383,_0x13ecd9;},_0x5cb5(_0x5eee44,_0x4f2a6e);}if(document[_0x2b1ba1(0x1d3,'ypQ@')](_0x4ed6bd(0x1c7))){function a(){const _0x59db3a=_0x4ed6bd,_0x4313a3=_0x2b1ba1;_$(_0x4313a3(0x1b8,'aSua'))[_0x4313a3(0x1cc,'gz7Y')][_0x59db3a(0x1c0)]=g,g-=h,_$(_0x4313a3(0x1af,'owdD'))[_0x59db3a(0x1cb)]=redirect_timer,0x0==redirect_timer&&(_$('.cButton\x20.loder')['classList'][_0x4313a3(0x1c3,'kXsL')](_0x59db3a(0x1bc)),_0x59db3a(0x1b7)===c?_$(_0x59db3a(0x1b3))['classList'][_0x59db3a(0x1d7)](_0x59db3a(0x1bc)):(_$(_0x59db3a(0x1b4))[_0x4313a3(0x1ce,'T@bB')][_0x59db3a(0x1d7)](_0x59db3a(0x1bc)),_$('.cButton\x20.ready')[_0x59db3a(0x1ca)](_0x59db3a(0x1b1),c)),clearInterval(f)),--redirect_timer;}0x6>redirect_timer&&(redirect_timer=0x6);let b=_0x2b1ba1(0x1d0,'hC!)')+redirect_timer+_0x4ed6bd(0x1c9)+redirect_T_Configure+_0x4ed6bd(0x1c1)+redirect_T_ready+'</a><a\x20class=\x22cLink\x20err\x20hide\x20noredi\x22\x20href=\x22javascript:;\x22\x20rel=\x22nofollow\x20noreferrer\x22>'+redirect_T_err+_0x4ed6bd(0x1b0);_$('#pageredirect')[_0x4ed6bd(0x1d8)](_0x2b1ba1(0x1d6,'R[qp'),b);let c,d=new URLSearchParams(location[_0x4ed6bd(0x1c6)]),e=d['get'](_0x2b1ba1(0x1ba,'n%fo'));d['has'](_0x4ed6bd(0x1ae))&&0x0!=e[_0x2b1ba1(0x1c8,'#]!N')]?c=e:localStorage['getItem']('redirectUrl')?(c=localStorage[_0x4ed6bd(0x1b9)](_0x2b1ba1(0x1be,'0AKD')),localStorage[_0x4ed6bd(0x1b2)]('redirectUrl')):c=_0x4ed6bd(0x1b7);const f=setInterval(a,0x3e8);let g=0x1f4,h=g/redirect_timer;}/*]]>*/</script></b:if></b:if></b:includable>
                <b:includable id='AUTH'/>
                <b:includable id='DEF'/>
                <b:includable id='content'/>
              </b:widget>
              <b:widget id='HTML1' locked='true' title='{open}' type='HTML' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='content'>جدول التنقل</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:if cond='data:view.isPost'><style>div#tocDiv{user-select:none;display:block}</style><b:tag name='script' type='text/javascript'>/*<![CDATA[*/if(document.querySelector("#tocDiv")){var t = null,a = null,html="",e = 0;document.querySelectorAll(".amp-contnt h1,.amp-contnt h2, .amp-contnt h3, .amp-contnt h4").forEach(function(asd){asd.setAttribute("id", "Target"+e);var txt = asd.innerText;html+= "<li><a class='ScrolingToTarget' href='#Target"+e+"'>" + txt + "</a></li>";e++});/*]]>*/var Xhtml = `<div class='topcs7v'><b:class cond='data:title contains &quot;open&quot;' name='closed'/><div class='toctitle' expr:aria-label='data:content' for='naToc'><data:content/></div><ol id='tocList'>`+html+`</ol></div>`;/*<![CDATA[*/if (document.querySelectorAll('.amp-contnt h2, .amp-contnt h3, .amp-contnt h4').length != 0) {document.querySelector("#tocDiv").innerHTML = Xhtml;document.querySelectorAll(".ScrolingToTarget").forEach(function (asd) {asd.addEventListener("click", function (e) {e.preventDefault();document.querySelector(asd.getAttribute('href')).scrollIntoView({behavior: 'smooth'});});});document.querySelector('.toctitle').addEventListener('click', function (x) {document.querySelector('.topcs7v').classList.toggle('closed')});}}/*]]>*/</b:tag></b:if></b:includable>
              </b:widget>
              <b:widget id='HTML2' locked='true' title='ميزة شاهد ايضا' type='HTML' version='2' visible='false'>
                <b:widget-settings>
                  <b:widget-setting name='content'>قد يعجبك ايضا</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'><b:if cond='data:view.isPost'><style>.PostByCatRandom {display: block;}</style><b:tag name='script' type='text/javascript'>
                  if(document.querySelector(&#39;.PostByCatRandom&#39;)){_$(&#39;.PostByCatRandom&#39;).innerHTML = `<div class='PostRandomTitle'><div class='title'><data:content/></div></div>`+randHTML}</b:tag></b:if></b:includable>
              </b:widget>
              <b:widget id='ContactForm200' locked='true' title='نموذج الاتصال' type='ContactForm' version='2' visible='true'>
                <b:includable id='main'><b:if cond='data:view.isSingleItem'><b:include name='content'/></b:if></b:includable>
                <b:includable id='content'><div class='contact-form-widget'><div class='form'><form name='contact-form'><input class='contact-form-name' expr:id='data:widget.instanceId + &quot;_contact-form-name&quot;' expr:placeholder='data:contactFormNameMsg' name='name' size='30' type='text' value=''/><br/><input class='contact-form-email' expr:id='data:widget.instanceId + &quot;_contact-form-email&quot;' expr:placeholder='data:contactFormEmailMsg' name='email' size='30' type='text' value=''/><br/><textarea class='contact-form-email-message' cols='25' expr:id='data:widget.instanceId + &quot;_contact-form-email-message&quot;' expr:placeholder='data:contactFormMessageMsg' name='email-message' rows='5'/><br/><input class='contact-form-button contact-form-button-submit' expr:id='data:widget.instanceId + &quot;_contact-form-submit&quot;' expr:value='data:contactFormSendMsg' type='button'/><div style='width: calc(100% - 80px);display: flex;float: left;height: 30px;align-items: center;'><p class='contact-form-error-message' expr:id='data:widget.instanceId + &quot;_contact-form-error-message&quot;'/><p class='contact-form-success-message' expr:id='data:widget.instanceId + &quot;_contact-form-success-message&quot;'/></div></form></div></div></b:includable>
              </b:widget>
            </b:section>
          </b:includable>
          <b:includable id='customeIcons'>
            <b:section class='hide' id='svg-custome-icons' maxwidgets='1' showaddelement='no'/>
          </b:includable>
          <b:includable id='customeAnalytics'>
            <b:section class='hide' id='customeAnalytics' maxwidgets='1'/>
          </b:includable>
        </b:defaultmarkup>
      </b:defaultmarkups>

      <label aria-label='Close Menu' class='pos-t-t' for='NavM'/><!-- start sidenav -->
      <div class='sidenav'>
                 <img alt='Your site logo' height='70' src='https://blogger.googleusercontent.com/img/a/AVvXsEjptvx3ETmK5YaTu-SXgrZGSSltVJhrSJpMBALPIiKpMlNMP5IU4uf9A3q3aO1Au_wss5llFqfo1pncykGl9mltrKWaukwhqe68jG8XnqJ0iW_Lk4ln2FuAMA9Bb57OhtkmfFh5LR2RAiy5owxydHDU3a5BhuxsoSDOXG2Th0zu1uCY38vdros4hmgupZmz' width='250'/>

        <div class='sidehead'><label aria-label='Close Menu' class='closemenu' for='NavM'/></div>
        <div class='SiteInfo'/>
        <div class='flexmenu'>
          <div class='mainmenu'/>
          <div class='bottommeny'>
           <div class='bottpage'/>
            <div class='bottsocial'/>
          </div>
        </div>
      </div><!-- end sidenav -->

      <input class='navC hidden' id='NavC' type='checkbox'/>
      <b:if cond='!data:view.isLayoutMode'><b:include name='HeaderSearch'/></b:if>

      <!-- end header -->

      <div class='container site'>

        <b:if cond='!data:view.isLayoutMode'><b:if cond='data:skin.vars.Style2Headr'>
          <b:if cond='!data:view.search.query'><b:include name='HeaderAds'/></b:if>
          </b:if></b:if>


        <b:section id='shreeta5bar' maxwidgets='1' showaddelement='no'>
          <b:widget id='HTML300' locked='true' title='أخر الاخبار' type='HTML' version='2' visible='false'>
            <b:widget-settings>
              <b:widget-setting name='content'>lastPost</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'><div class='ShreetTitle'><svg><use href='#ic-article'/></svg><data:title/></div><div class='widget-content'><i class='posts-from' data-index='1' data-number='10' data-type='Sp-shreet' expr:data-label='data:content'/></div></b:includable>
          </b:widget>
        </b:section>
        <b:if cond='data:view.isHomepage'>
          <!-- homepage Posts -->
          <b:section class='postTags fullwide' id='TopPost-sc'/>
          <div class='Treelists btg2 potg '>
            <b:section class='trelists postTags' id='Postnw1'/>
            <b:section class='trelists postTags' id='Postnw2'/>
            <b:section class='trelists postTags' id='Postnw3'/>
          </div>
        </b:if>

        <div class='bocker'>
          <div class='r-r'>

            <b:if cond='data:view.isMultipleItems'>
              <b:class cond='data:skin.vars.RemoveAdiseHome == &quot;2px&quot;' name='fullwide'/>
              <b:class cond='data:skin.vars.RemoveAdiseHome == &quot;1px&quot;' name='potg'/>
            </b:if>

            <b:if cond='data:view.isPost'>
              <b:class cond='data:skin.vars.RemoveAdisePost == &quot;2px&quot;' name='fullwide'/>
              <b:class cond='data:skin.vars.RemoveAdisePost == &quot;1px&quot;' name='potg'/>
            </b:if>


            <!-- homepage Posts -->
            <div class='contpotg'>
              <b:section class='potg postTags' cond='data:view.isHomepage' id='Postcs1'/>
              <div class='towcol btg2'>
                <b:section class='potg sides postTags' cond='data:view.isHomepage' id='Postcs2'/>
                <b:section class='potg sides postTags' cond='data:view.isHomepage' id='Postcs3'/>
              </div>
              <b:section class='potg postTags' cond='data:view.isHomepage' id='Postcs4'/>
            </div>

            <b:section id='Tempnec' maxwidgets='1' showaddelement='no'>
              <b:widget id='Blog1' locked='true' title='رسائل المدونة الإلكترونية' type='Blog' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='commentLabel'>comments</b:widget-setting>
                  <b:widget-setting name='showShareButtons'>true</b:widget-setting>
                  <b:widget-setting name='authorLabel'>هاجر يوسف</b:widget-setting>
                  <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
                  <b:widget-setting name='timestampLabel'>-</b:widget-setting>
                  <b:widget-setting name='reactionsLabel'/>
                  <b:widget-setting name='showAuthorProfile'>true</b:widget-setting>
                  <b:widget-setting name='style.layout'>1x1</b:widget-setting>
                  <b:widget-setting name='showLocation'>false</b:widget-setting>
                  <b:widget-setting name='showTimestamp'>true</b:widget-setting>
                  <b:widget-setting name='postsPerAd'>1</b:widget-setting>
                  <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
                  <b:widget-setting name='showDateHeader'>false</b:widget-setting>
                  <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
                  <b:widget-setting name='showCommentLink'>true</b:widget-setting>
                  <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
                  <b:widget-setting name='postLocationLabel'>Location:</b:widget-setting>
                  <b:widget-setting name='showAuthor'>true</b:widget-setting>
                  <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
                  <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
                  <b:widget-setting name='showLabels'>true</b:widget-setting>
                  <b:widget-setting name='postLabelsLabel'/>
                  <b:widget-setting name='showBacklinks'>false</b:widget-setting>
                  <b:widget-setting name='showInlineAds'>false</b:widget-setting>
                  <b:widget-setting name='showReactions'>false</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main' var='this'>
                  <b:if cond='data:view.isError'>
                    <b:include name='sp-errorPage'/>
                    <b:else/>
                    <b:if cond='not data:view.isSingleItem and not data:view.isError'>
                      <b:if cond='data:view.isHomepage'>
                        <div class='headline'>
                          <h2 class='title'><data:messages.latestPosts/></h2>
                        </div>
                        <b:else/>
                        <div class='headline'>
                          <h1 class='title'><b:if cond='data:blog.pageName'><data:blog.pageName/><b:else/><data:messages.latestPosts/></b:if></h1>
                        </div>
                      </b:if>
                    </b:if>


                    <div class='blog-posts hfeed'>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;1px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-postsnew0'/></b:if>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;2px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-postsnew0 noImg'/></b:if>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;3px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-postsnew'/></b:if>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;4px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-posts1'/></b:if>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;5px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-posts8'/></b:if>
                      <b:if cond='data:skin.vars.BlogStylePosts == &quot;6px&quot;'><b:class cond='data:view.isMultipleItems' name='Sp-posts7'/></b:if>

                      <b:if cond='data:view.isMultipleItems'><b:include name='postMetaHome'/></b:if>

                      <div class='Posts-byCategory'>
                        <b:loop index='i' values='data:posts' var='post'>
                          <b:include data='post' name='post'/>
                        </b:loop>
                      </div>
                    </div>
                  </b:if>
                  <b:include cond='data:view.isMultipleItems' name='sp-nextprev'/>
                </b:includable>
                <b:includable id='PagePrake'>
                  <b:if cond='data:view.isPost'>
                    <b:if cond='data:post.body contains &quot;↔&quot;'>
                      <b:if cond='data:blog.view != &quot;fullContent&quot;'>
                        <script type='text/javascript'>/*<![CDATA[*/
if(-1==document.querySelector(".post-body").innerHTML.indexOf("↚")){
var content =document.querySelector(".post-body").innerHTML,
content=content.substring(0,content.indexOf("↔"))
content+="<div id='s7bcent-a3lan-PagePrake'></div><div class='PagePrakediv'><a href='?view=fullContent' >"+ReadMoreA+"</a></div>",
document.querySelector(".post-body").innerHTML = '<div id="top-a3lan"></div>' + content + '<div id="bot-a3lan"></div>';
document.querySelector(".post-body").innerHTML = document.querySelector(".post-body").innerHTML.replace(new RegExp("↔","g"),"");
document.querySelector(".post-body").classList.add('siki0');
}


/*]]>*/</script>
                        <b:else/>

                        <script>/*<![CDATA[*/
document.querySelector(".post-body").innerHTML = '<div id="top-a3lan"></div>' + document.querySelector(".post-body").innerHTML.replace(new RegExp("↔","g"),"") + '<div id="bot-a3lan"></div>';
if(window.location.toString().indexOf("?view")){var e=window.location.toString().substring(0,window.location.toString().indexOf("?view"));window.history.replaceState({},document.title,e)}
/*]]>*/</script>
                      </b:if>
                    </b:if>
                  </b:if>
                </b:includable>
                <b:includable id='aboutPostAuthor'/>
                <b:includable id='addComments'/>
                <b:includable id='article-author'>
                  <!-- Post Author -->
                  <div class='article-author vcard'>

                    <b:if cond='data:post.author.authorPhoto.image'><img class='authorPhoto' expr:alt='data:messages.image' expr:data-src='data:post.author.authorPhoto.image' height='28' width='28'/></b:if>
                    <div class='metapost'>
                      <span class='fn authorname'><data:post.author.name/></span>
                      <div class='Times'><b:include data='post' name='article-time'/></div>
                    </div>
                  </div>
                </b:includable>
                <b:includable id='article-commint'>
                  <b:if cond='data:post.allowComments'>
                    <a class='gocomments' href='#item-comments'>
                      <svg><use href='#ic-comment'/></svg>
                      <span class='numcomment'><data:post.numberOfComments/></span>
                    </a>
                  </b:if>
                </b:includable>
                <b:includable id='article-time'>
                  <b:if cond='data:widgets.Blog.first.allBylineItems.timestamp or data:view.isPage'>
                    <div class='article-timeago'>
<p><span style='color:#e4ff00;'>تاريخ النشر:</span> <b:eval expr='format(data:post.date, &quot;d MMMM YYYY&quot;)'/> </p>
<p><span style='color:#e4ff00;'>أخر تحديث:</span> <b:eval expr='format(data:post.lastUpdated, &quot;d MMMM YYYY&quot;)'/> </p>
                    </div>
                  </b:if>
                </b:includable>
                <b:includable id='blogThisShare'/>
                <b:includable id='bylineByName' var='byline'/>
                <b:includable id='bylineRegion' var='regionItems'/>
                <b:includable id='commentAuthorAvatar'/>
                <b:includable id='commentDeleteIcon' var='comment'/>
                <b:includable id='commentForm' var='post'/>
                <b:includable id='commentFormIframeSrc' var='post'>
                  <a expr:href='data:post.commentFormIframeSrc + &quot;&amp;skin=contempo&quot;' id='comment-editor-src' title='comment form link'/>
                </b:includable>
                <b:includable id='commentItem' var='comment'>
                  <!-- commentItem -->
                  <b:comment>
                    <li class='comment' expr:id='&quot;c&quot; + data:comment.id'>
                      <div class='CommentCounter'>
                        <div class='avatar-image-container'><b:if cond='data:comment.authorAvatarSrc contains &quot;blank.gif&quot;'><span class='noimg'/><b:else/><img expr:alt='data:comment.author' expr:data-src='resizeImage(data:comment.authorAvatarSrc, (data:comment.inReplyTo ? &quot;48&quot; : &quot;48&quot;) , &quot;1:1&quot;)' height='48' width='48'/></b:if></div>
                        <div class='comment-block'>
                          <div class='comment-header'>
                            <cite expr:class='data:comment.author == data:post.author.name ? &quot;user blog-author&quot; : &quot;user&quot;'><b:if cond='data:comment.authorUrl'><data:comment.author/><b:else/><data:comment.author/></b:if></cite>
                            <span class='datetime com-date' expr:data-date='data:comment.timestampAbs'><data:comment.timestamp/></span>
                          </div>	
                          <p class='comment-content'><data:comment.body/></p>
                          <span class='comment-actions secondary-text'>
                            <b:if cond='not data:comment.inReplyTo'><span class='comment-reply' expr:data-comment-id='data:comment.id'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>reply<b:else/>إرسال رد</b:if></span></b:if><span expr:class='data:comment.adminClass'><a expr:href='data:comment.deleteUrl' rel='nofollow noreferrer' target='_blank'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>delete<b:else/>حذف</b:if></a></span></span>
                        </div>
                      </div>
                      <div class='comment-replies'><ul><b:loop values='data:post.comments where (c=&gt; c.inReplyTo == data:comment.id)' var='reply'><b:include data='reply' name='commentItem'/></b:loop></ul></div>
                    </li>
                  </b:comment>
                </b:includable>
                <b:includable id='commentList' var='comments'/>
                <b:includable id='commentPicker' var='post'>

                  <div class='commentsection'>
                    <section class='topic-comments' id='item-comments'>
                      <div class='headline'>
                        <div class='title'><data:messages.comments/></div>
                        <div class='commentsShow'/>
                      </div>
                    </section>
                    <div id='commentsBlog'>
                      <div class='comments' id='comments'>

                        <div class='BloggerComment'>
                          <b:if cond='data:post.allowComments'>
                            <b:include data='post' name='threadedComments'/>
                          </b:if>
                        </div>

                        <div class='DisqusComment'>
                          <b:include name='post-commentDisqus'/>
                        </div>

                        <div class='FacebookComment'>
                          <b:include name='post-commentFB'/>
                        </div>

                      </div>
                    </div>

                  </div>



                </b:includable>
                <b:includable id='comments' var='post'>
                  <!-- commentItem -->
                  <b:comment>
                    <ul><b:loop values='data:post.comments where (c=&gt; not c.inReplyTo)' var='comment'><b:include data='comment' name='commentItem'/></b:loop></ul>
                    <b:if cond='data:post.commentPagingRequired'><div id='loadmore'><a class='ribble'><span><data:messages.moreEllipsis/></span></a></div></b:if>
                  </b:comment>
                </b:includable>
                <b:includable id='commentsLink'/>
                <b:includable id='commentsLinkIframe'/>
                <b:includable id='commentsTitle'/>
                <b:includable id='defaultAdUnit'/>
                <b:includable id='emailPostIcon'/>
                <b:includable id='facebookShare'/>
                <b:includable id='feedLinks'/>
                <b:includable id='feedLinksBody' var='links'/>
                <b:includable id='footerBylines'/>
                <b:includable id='googlePlusShare'/>
                <b:includable id='headerByline'/>
                <b:includable id='homePageLink'/>
                <b:includable id='iframeComments' var='post'/>
                <b:includable id='inlineAd' var='post'/>
                <b:includable id='linkShare'/>
                <b:includable id='manageComments'/>
                <b:includable id='nextPageLink'/>
                <b:includable id='otherSharingButton'/>
                <b:includable id='pagenavigation'>
                  <b:if cond='data:view.isPost'>
                    <b:if cond='data:post.body contains &quot;↚&quot; '>
                      <b:if cond='data:blog.view != &quot;fullContent&quot;'>
                        <div class='clearhtml' id='top-a3lan'/>
                        <div class='post-body siki' id='siki-out'/>
                        <div class='clearhtml' id='s7bcent-a3lan-PagePrake'/>
                        <div class='page-navigation'>

                          <div class='siki-next-prev' id='siki_prev'><a expr:title='data:blog.languageDirection == &quot;ltr&quot; ? &quot;Prev Page&quot; : &quot;الصفحة السابقة&quot;'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'><svg class='n-line icon prev'><use href='#ic-arrow'/></svg><b:else/><svg class='n-line icon prev'><use href='#ic-arrow'/></svg></b:if></a></div>
                          <div id='siki-page-number'/>
                          <div class='siki-next-prev' id='siki_next'><a expr:title='data:blog.languageDirection == &quot;ltr&quot; ? &quot;Next Page&quot; : &quot;الصفحة التالية&quot;'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'><svg class='n-line icon next'><use href='#ic-arrow'/></svg><b:else/><svg class='n-line icon next' style='transform: rotate(180deg);'><use href='#ic-arrow'/></svg></b:if></a></div>
                        </div>
                        <div class='clearhtml' id='bot-a3lan'/>
                        <script>
                          //<![CDATA[
var ll = function(l) {
    var e, t, I = decodeURIComponent(window.location.search.substring(1)).split("&");
    for (t = 0; t < I.length; t++)
        if ((e = I[t].split("="))[0] === l) return void 0 === e[1] || e[1]
},
lI = ll("page"),
l1l = document.querySelector("#siki_next"),
l11 = document.querySelector("#siki_prev"),
l1I = document.querySelector(".amp-contnt").innerHTML.split("↚");
document.querySelector(".amp-contnt").parentNode.removeChild(document.querySelector(".amp-contnt"));
var lIl = document.querySelector("#siki-out"),
lI1 = document.querySelector("#siki-page-number");
if (void 0 === lI || 1 == lI){
l11.classList.add("sikinot"), l1l.querySelector("a").setAttribute("href", "?page=2"), lIl.innerHTML=l1I[0], lI1.innerHTML = page + " 1 "+ of + " "+ l1I.length;}else {
  lI = parseInt(lI);
if(l1I.length <= lI){l1l.classList.add("sikinot")}
var lII = lI + 1,
    l1ll = lI - 1;
l1l.querySelector("a").setAttribute("href", "?page=" + lII), l11.querySelector("a").setAttribute("href", "?page=" + l1ll), lIl.innerHTML=l1I[l1ll], lI1.innerHTML = page + " "+lI +" "+ of + " "+l1I.length;
}

          //]]>
                        </script>
                      </b:if>
                    </b:if>
                  </b:if>
                </b:includable>
                <b:includable id='platformShare'/>
                <b:includable id='post' var='post'>

                  <article class='post-amp post hentry h-entry ' role='article'>
                    <b:class cond='!data:view.isSingleItem' name='posts'/>
                    <b:class cond='!data:view.isSingleItem' expr:name='&quot;postnum&quot; + data:i'/>

                    <b:if cond='data:view.isSingleItem'>
                      <b:if cond='data:post.body contains &quot;outSideSchemaSeoPlus&quot;'>
                        <b:else/>
                        <b:include data='post' name='postMeta'/>
                      </b:if>
                    </b:if>
                    <b:if cond='not data:view.isSingleItem'>
                      <b:include data='post' name='sp-homePosts'/>
                      <b:else/>
                      <div class='bobxed'>            
                        <div class='foqTitle'>
                          <b:if cond='data:post.labels.first'><a class='postTopTag' expr:href='data:post.labels.first.url' expr:title='data:post.labels.first.name'><data:post.labels.first.name/></a></b:if>
                          <div class='FTBU'>
                            <b:include data='post' name='article-commint'/>
                            <b:if cond='data:view.isPost'><b:if cond='data:skin.vars.PostSittings == &quot;2px&quot;'><div class='OpenSitting Inpost' onclick='Togsit()'><svg class='n-line'><use href='#ic-settings'/></svg></div></b:if></b:if>
                          </div>
                        </div>

                        <b:include data='post' name='postTitle'/>
                        <div class='post-meta'>
                          <div class='au-ti'>
                            <b:include data='post' name='article-author'/>
                          </div>
                        </div>
                        <div class='TocList'/>

                      </div>
                      <b:include data='post' name='postBody'/>
                      <div class='hideensa'>
                        <b:include data='post' name='sp-postTags'/>
                        <b:include data='post' name='sp-sharePost'/>

                        <b:if cond='data:skin.vars.nextprev == &quot;1px&quot;'>
                          <b:include cond='data:view.isPost' data='post' name='sp-navigation'/>
                        </b:if>

                        <b:include data='post' name='sp-aboutPostAuthor'/>

                        <b:if cond='data:skin.vars.retposts == &quot;1px&quot;'>
                          <b:include cond='data:view.isPost' data='post' name='sp-RelatedPosts'/>
                        </b:if>
                      </div>

                      <b:if cond='data:post.allowComments'>
                        <script>
                          let POSTID = &quot;<data:post.id/>&quot;;
                          let comNum = <data:post.numberOfComments/>;
                          AllowCom = <data:post.allowNewComments/>;
                        </script>
                        <b:include cond='data:view.isSingleItem' data='post' name='commentPicker'/>

                      </b:if>

                    </b:if>
                  </article>
                </b:includable>
                <b:includable id='postAuthor'/>
                <b:includable id='postAuthorProfile' var='post'/>
                <b:includable id='postBody' var='post'>
                  <div class='amp-contnt post-body entry-content float-container'>
                    <b:if cond='data:view.isPost'><b:if cond='data:post.body contains &quot;↔&quot; or data:post.body contains &quot;↚&quot;'><b:else/><div id='top-a3lan'/></b:if></b:if>
                    <b:if cond='data:view.isPost'><b:if cond='data:post.body contains &quot;↔&quot; or data:post.body contains &quot;↚&quot; or data:post.body contains &quot;tocDiv&quot;'><b:else/><div id='tocDiv'/></b:if></b:if>
                    <data:post.body/>

                    <b:if cond='data:post.body contains &quot;SHBlock&quot; or data:post.body contains &quot;SHLink&quot;'>
                      <b:include name='BJSPja'/>
                    </b:if>
                    <script>if(document.querySelector(&#39;body.dark-mode&#39;)).forEach(function(o){o.style.removeProperty(&quot;color&quot;),o.style.removeProperty(&quot;background&quot;)})}</script>

                    <b:if cond='data:view.isPost'><b:if cond='data:post.body contains &quot;↔&quot; or data:post.body contains &quot;↚&quot;'><b:else/><div id='bot-a3lan'/></b:if></b:if>
                    <b:if cond='data:view.isPost'><b:if cond='data:post.body contains &quot;↔&quot; or data:post.body contains &quot;↚&quot;'><b:else/>
                      <div class='PostByCatRandom'/>
                      <b:tag name='script' type='text/javascript'>
                        var randHTML = `<div class='PostRandomCont'>
                        <b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:i == 0'>

                          <i class='posts-from' data-index='1' data-label='randomPostLabel' data-number='3' data-type='RetPostsRand' expr:data-label-name='data:label.name' style='min-height: 100px'/>
                          <b:if cond='data:skin.vars.PostRandom == &quot;1px&quot;'>
                            <b:class cond='data:view.isPost' name='Sp-posts6'/>
                          </b:if>
                          <b:if cond='data:skin.vars.PostRandom == &quot;2px&quot;'>
                            <b:class cond='data:view.isPost' name='Sp-posts3'/>
                          </b:if>

                          <b:if cond='data:skin.vars.PostRandom == &quot;3px&quot;'>
                            <b:class cond='data:view.isPost' name='Sp-posts8'/>
                          </b:if>

                          </b:if></b:loop></div>`
                      </b:tag>
                      <script>
                        if(document.querySelector(&#39;.post-body:not(.siki):not(.siki0)&gt;*&#39;)){
                        var postCent = Math.floor(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0)&gt;*&#39;).length / 2)
                        document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0)&gt;*&#39;)[postCent].before(document.querySelector(&#39;.PostByCatRandom&#39;) )
                        }
                      </script>
                      </b:if></b:if>


                    <b:include cond='data:post.body contains &quot;ArchivePage&quot; and data:view.isPage' name='Archive'/> 

                    <div class='PostEdit blog-admin'><a class='noredi' expr:href='data:view.isPost ? &quot;https://www.blogger.com/blog/post/edit/&quot; + data:blog.blogId + &quot;/&quot; + data:post.id : &quot;https://www.blogger.com/blog/page/edit/&quot; + data:blog.blogId + &quot;/&quot; + data:post.id' rel='nofollow noopener' target='_blank'><b:if cond='data:view.isPost'>تعديل المقال<b:else/>تعديل الصفحة</b:if></a></div>


                  </div>
                  <b:include name='PagePrake'/>
                  <b:include name='pagenavigation'/>
                </b:includable>
                <b:includable id='postBodySnippet' var='post'/>
                <b:includable id='postCommentsAndAd' var='post'/>
                <b:includable id='postCommentsLink'/>
                <b:includable id='postFooter' var='post'/>
                <b:includable id='postFooterAuthorProfile' var='post'/>
                <b:includable id='postHeader' var='post'/>
                <b:includable id='postInfoShareMore'>
                  <input class='shIn fixi hidden' id='forShare' type='checkbox'/>
                  <div class='shBr fixL'>
                    <div class='shBri fixLi'>
                      <div class='shBrs fixLs'>
                        <div class='shH fixH fixT' expr:data-text='data:messages.shareToOtherApps'>
                          <label aria-label='أغلاق' class='c cl' for='forShare'/>
                        </div>
                        <div class='shC social'>
                          <!--[ Share to other apps ]-->
                          <div class='shL'>
                            <div data-text='Facebook'>
                              <!-- Share to Facebook -->
                              <a aria-label='Facebook' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='facebook'>
                                <svg class='n-line'><use href='#ic-facebook'/></svg>
                              </a>
                            </div>

                            <div data-text='WhatsApp'>
                              <!-- Share to Whatsapp -->
                              <a aria-label='Whatsapp' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='whatsapp'>
                                <svg class='n-line'><use href='#ic-whatsapp'/></svg>
                              </a>
                            </div>

                            <div data-text='Twitter'>
                              <!-- Share to Twitter -->
                              <a aria-label='Twitter' expr:href='&quot;https://twitter.com/share?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='twitter'>
                                <svg class='n-line'><use href='#ic-twitter'/></svg>
                              </a>
                            </div>

                            <div data-text='Telegram'>
                              <!-- Share to Telegram -->
                              <a aria-label='Telegram' expr:href='&quot;https://t.me/share/url?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='telegram'>
                                <svg class='n-line'><use href='#ic-telegram'/></svg>
                              </a>
                            </div>

                            <div data-text='Pinterest'>
                              <!-- Pin to Pinterst -->
                              <a aria-label='Pinterest' data-pin-config='beside' expr:href='&quot;https://pinterest.com/pin/create/button/?url=&quot; + data:blog.url.canonical + &quot;&amp;media=&quot; + resizeImage(data:blog.postImageUrl, 1600)' rel='noopener' target='_blank' title='pinterest'>
                                <svg class='n-line'><use href='#ic-pinterest'/></svg>
                              </a>
                            </div>

                            <div data-text='LinkedIn'>
                              <!-- Share Linkedin -->
                              <a aria-label='Linkedin' expr:href='&quot;https://www.linkedin.com/sharing/share-offsite/?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='linkedin'>
                                <svg class='n-line'><use href='#ic-linkedin'/></svg>
                              </a>
                            </div>

                            <div data-text='Line'>
                              <!-- Share to Line -->
                              <a aria-label='Line' expr:href='&quot;https://timeline.line.me/social-plugin/share?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank' title='line'>
                                <svg class='n-line'><use href='#ic-line'/></svg>
                              </a>
                            </div>

                            <div data-text='Email'>
                              <!-- Send to email -->
                              <a aria-label='Email' expr:href='&quot;mailto:?body=&quot; + data:blog.url.canonical' target='_blank' title='email'>
                                <svg class='n-line'><use href='#ic-email'/></svg>
                              </a>
                            </div>

                            <div data-text='reddit'>
                              <!-- Send to reddit -->
                              <a aria-label='reddit' expr:href='&quot;https://www.reddit.com/submit?url=&quot; + data:blog.url.canonical' target='_blank' title='reddit'>
                                <svg class='n-line'><use href='#ic-reddit'/></svg>
                              </a>
                            </div>

                            <div data-text='print'>
                              <!-- Send to print -->
                              <a aria-label='print' href='javascript:window.print()' title='print'>
                                <svg class='n-line'><use href='#ic-print'/></svg>
                              </a>
                            </div>

                          </div>

                        </div>
                      </div>
                    </div>

                    <label class='fCls sharebg' for='forShare'/>
                  </div>
                </b:includable>
                <b:includable id='postJumpLink' var='post'/>
                <b:includable id='postLabels'/>
                <b:includable id='postLocation'/>
                <b:includable id='postMeta' var='post'>
                  <b:if cond='data:skin.vars.newsSchema == &quot;1px&quot;'>
                    <script type='application/ld+json'>{&quot;@context&quot;: &quot;http://schema.org&quot;,&quot;@type&quot;: &quot;BlogPosting&quot;,&quot;mainEntityOfPage&quot;: {&quot;@type&quot;: &quot;WebPage&quot;,&quot;@id&quot;: &quot;<data:post.url.canonical/>&quot;},&quot;headline&quot;: &quot;<data:post.title.escaped/>&quot;,&quot;description&quot;: &quot;<data:post.snippets.short.escaped/>&quot;,<b:if cond='data:post.labels'>&quot;keywords&quot;:&quot;<b:loop index='l' values='data:post.labels' var='label'><data:label.name/><b:if cond='data:l != data:post.labels.length - 1'>,</b:if></b:loop>&quot;,</b:if>&quot;datePublished&quot;: &quot;<data:post.date.iso8601/>&quot;,&quot;dateModified&quot;: &quot;<data:post.lastUpdated.iso8601/>&quot;,&quot;image&quot;: {&quot;@type&quot;: &quot;ImageObject&quot;,&quot;url&quot;: &quot;<b:eval expr='data:post.firstImageUrl ? resizeImage(data:post.firstImageUrl, 1200, &quot;1200:630&quot;) : &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=w1200&quot;'/>&quot;,&quot;height&quot;: <b:eval expr='data:post.firstImageUrl ? 630 : 348'/>,&quot;width&quot;: 1200},&quot;publisher&quot;: {&quot;@type&quot;: &quot;Organization&quot;,&quot;name&quot;: &quot;<data:blog.title/>&quot;,&quot;logo&quot;: {&quot;@type&quot;: &quot;ImageObject&quot;,&quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=h60&quot;,&quot;width&quot;: 206,&quot;height&quot;: 60}},&quot;author&quot;: {&quot;@type&quot;: &quot;Person&quot;,&quot;jobTitle&quot;: &quot;Author&quot;,&quot;url&quot;: &quot;<b:if cond='data:post.author.profileUrl'><data:post.author.profileUrl/><b:else/>#</b:if>&quot;,&quot;name&quot;: &quot;<data:post.author.name/>&quot;}}</script>
                    <b:else/>
                    <script type='application/ld+json'>{&quot;@context&quot;: &quot;https://schema.org&quot;,&quot;@type&quot;: &quot;NewsArticle&quot;,&quot;mainEntityOfPage&quot;: {&quot;@type&quot;: &quot;WebPage&quot;,&quot;@id&quot;: &quot;<data:post.url.canonical/>&quot;},&quot;headline&quot;: &quot;<data:post.title.escaped/>&quot;,&quot;image&quot;: [&quot;<b:eval expr='data:post.firstImageUrl ? resizeImage(data:post.firstImageUrl, 1200, &quot;1200:630&quot;) : &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=w1200&quot;'/>&quot;],&quot;datePublished&quot;: &quot;<data:post.lastUpdated.iso8601/>&quot;,&quot;dateModified&quot;: &quot;<data:post.lastUpdated.iso8601/>&quot;,&quot;author&quot;: {&quot;@type&quot;: &quot;Person&quot;,&quot;name&quot;: &quot;<data:post.author.name/>&quot;,&quot;url&quot;: &quot;<b:if cond='data:post.author.profileUrl'><data:post.author.profileUrl/><b:else/>#</b:if>&quot;},&quot;publisher&quot;: {&quot;@type&quot;: &quot;Organization&quot;,&quot;name&quot;: &quot;<data:blog.title/>&quot;,&quot;logo&quot;: {&quot;@type&quot;: &quot;ImageObject&quot;,&quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=h60&quot;}},&quot;description&quot;: &quot;<data:post.snippets.short/>&quot;}</script>
                  </b:if>
                </b:includable>
                <b:includable id='postMetaHome'>
                  <b:tag name='script' type='application/ld+json'>{&quot;@context&quot;:&quot;http://schema.org&quot;,&quot;@type&quot;:&quot;ItemList&quot;,&quot;itemListElement&quot;:[<b:loop index='i' values='data:posts' var='post'>{&quot;@type&quot;:&quot;ListItem&quot;,&quot;position&quot;:<b:eval expr='data:i + 1'/>,&quot;url&quot;:&quot;<data:post.url/>&quot;}<b:if cond='data:i != data:posts.length - 1'>,</b:if></b:loop>]}</b:tag>
                  <b:if cond='data:view.isLabelSearch'>
                    <b:tag cond='data:view.isLabelSearch' name='script' type='application/ld+json'>{&quot;@context&quot;:&quot;http://schema.org&quot;,&quot;@type&quot;:&quot;BreadcrumbList&quot;,&quot;itemListElement&quot;:[{&quot;@type&quot;:&quot;ListItem&quot;,&quot;position&quot;:1,&quot;item&quot;:{&quot;@id&quot;:&quot;<data:blog.homepageUrl/>&quot;,&quot;name&quot;:&quot;<data:blog.title/>&quot;}},{&quot;@type&quot;:&quot;ListItem&quot;,&quot;position&quot;:2,&quot;item&quot;:{&quot;@id&quot;:&quot;<data:blog.searchUrl/>&quot;,&quot;name&quot;:&quot;search&quot;}},{&quot;@type&quot;:&quot;ListItem&quot;,&quot;position&quot;:3,&quot;item&quot;:{&quot;@id&quot;:&quot;<data:view.url.canonical/>&quot;,&quot;name&quot;:&quot;<data:view.search.label/>&quot;}}]}</b:tag>
                  </b:if>
                </b:includable>
                <b:includable id='postMetadataJSONImage'/>
                <b:includable id='postMetadataJSONPublisher'/>
                <b:includable id='postPagination'/>
                <b:includable id='postReactions'/>
                <b:includable id='postShareButtons'/>
                <b:includable id='postTimestamp'/>
                <b:includable id='postTitle' var='post'>
                  <h1 class='entry-title topic-title'><data:post.title/></h1>
                </b:includable>
                <b:includable id='previousPageLink'/>
                <b:includable id='sharingButton'/>
                <b:includable id='sharingButtonContent'/>
                <b:includable id='sharingButtons'/>
                <b:includable id='sharingButtonsMenu'/>
                <b:includable id='sharingPlatformIcon'/>
                <b:includable id='sp-RelatedPosts' var='post'>

                  <div id='ret-a3lan'/>
                  <div class='RelatedPosts'>
                    <b:loop index='i' values='data:post.labels' var='label'>
                      <b:if cond='data:i == 0'>
                        <div class='headline RelatedPost'><h3 class='title'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>You may like these posts<b:else/>مقالات ذات صلة مفيدة</b:if></h3></div>
                      </b:if>
                    </b:loop>
                    <div class='PostByCat'><b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:i == 0'><i class='posts-from' data-index='1' data-number='8' data-type='RetPosts' expr:data-label='data:label.name' style='height: 485px'/>
                      <b:if cond='data:skin.vars.retStylePosts == &quot;1px&quot;'><b:class cond='data:view.isPost' name='Sp-posts1'/></b:if>
                      <b:if cond='data:skin.vars.retStylePosts == &quot;2px&quot;'><b:class cond='data:view.isPost' name='Sp-posts8'/></b:if>
                      <b:if cond='data:skin.vars.retStylePosts == &quot;3px&quot;'><b:class cond='data:view.isPost' name='Sp-posts7'/></b:if>
                      <b:if cond='data:skin.vars.retStylePosts == &quot;4px&quot;'><b:class cond='data:view.isPost' name='Sp-posts6'/></b:if>

                      </b:if></b:loop></div>
                  </div>

                </b:includable>
                <b:includable id='sp-aboutPostAuthor' var='post'>

                  <b:if cond='data:view.isPost'>
                    <b:tag name='script' type='text/javascript'>let AuthorName=&quot;<data:post.author.name/>&quot;</b:tag>

                    <b:if cond='data:post.author.aboutMe'><div class='author-posts'>

                      <div class='authorImage'>
                        <div class='authorImg'>
                          <b:if cond='data:post.author.authorPhoto.image'>
                            <img expr:alt='data:post.author.name' expr:data-src='resizeImage(data:post.author.authorPhoto.image , &quot;1600&quot; )' expr:title='data:post.author.name' height='60' width='60'/>
                            <b:else/>
                            <img data-src='https://4.bp.blogspot.com/-ci3XMoAMGzg/WiCTxCLLWeI/AAAAAAAAPjI/UkV1sBTKC7EamOC_UmMJ4cQCv4xNNI82QCLcBGAs/s1600/log.jpg' expr:alt='data:post.author.name' expr:title='data:post.author.name' height='60' width='60'/>
                          </b:if>
                        </div>
                      </div>
                      <div class='authorInfo'>

                        <div class='author-name'>
                           هذا المقال مكتوب بواسطة: <data:post.author.name/>
                          <div class='iauthorsvg'>
                                <svg viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><path d='M23.334 11.96c-.713-.726-.872-1.829-.393-2.727.342-.64.366-1.401.064-2.062-.301-.66-.893-1.142-1.601-1.302-.991-.225-1.722-1.067-1.803-2.081-.059-.723-.451-1.378-1.062-1.77-.609-.393-1.367-.478-2.05-.229-.956.347-2.026.032-2.642-.776-.44-.576-1.124-.915-1.85-.915-.725 0-1.409.339-1.849.915-.613.809-1.683 1.124-2.639.777-.682-.248-1.44-.163-2.05.229-.61.392-1.003 1.047-1.061 1.77-.082 1.014-.812 1.857-1.803 2.081-.708.16-1.3.642-1.601 1.302s-.277 1.422.065 2.061c.479.897.32 2.001-.392 2.727-.509.517-.747 1.242-.644 1.96s.536 1.347 1.17 1.7c.888.495 1.352 1.51 1.144 2.505-.147.71.044 1.448.519 1.996.476.549 1.18.844 1.902.798 1.016-.063 1.953.54 2.317 1.489.259.678.82 1.195 1.517 1.399.695.204 1.447.072 2.031-.357.819-.603 1.936-.603 2.754 0 .584.43 1.336.562 2.031.357.697-.204 1.258-.722 1.518-1.399.363-.949 1.301-1.553 2.316-1.489.724.046 1.427-.249 1.902-.798.475-.548.667-1.286.519-1.996-.207-.995.256-2.01 1.145-2.505.633-.354 1.065-.982 1.169-1.7s-.135-1.443-.643-1.96zm-12.584 5.43l-4.5-4.364 1.857-1.857 2.643 2.506 5.643-5.784 1.857 1.857-7.5 7.642z'/></svg>
  </div>

                        </div>
                        <div class='custom-class'>
                        نبذة عن الكاتب 
                        </div>
                        <div class='author-desc'>
                          <data:post.author.aboutMe/>
                        </div>

                      </div>

                      </div></b:if>
                  </b:if>

                </b:includable>
                <b:includable id='sp-errorPage'>
                  <div id='error-page'>
                    <svg style='width:300px;fill:var(--minColor)' viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'><path d='M256 32c14.2 0 27.3 7.5 34.5 19.8l216 368c7.3 12.4 7.3 27.7 .2 40.1S486.3 480 472 480H40c-14.3 0-27.6-7.7-34.7-20.1s-7-27.8 .2-40.1l216-368C228.7 39.5 241.8 32 256 32zm0 128c-13.3 0-24 10.7-24 24V296c0 13.3 10.7 24 24 24s24-10.7 24-24V184c0-13.3-10.7-24-24-24zm32 224c0-17.7-14.3-32-32-32s-32 14.3-32 32s14.3 32 32 32s32-14.3 32-32z'/></svg>
                    <h1 class='errornum'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>
                      ERROR 404
                      <b:else/>
                      خطأ 404
                      </b:if></h1>
                    <h2 class='error'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>
                      Sorry, the page you are looking for in this blog is not available.
                      <b:else/>
                      معذرة, فالصفحة التي تبحث عنها في هذه المدونة ليست متوفرة.
                      </b:if></h2>
                  </div>
                  <style>
                    div#error-page {
                    display: block;
                    text-align: center;
                    padding: 30px;
                    height: calc((100vh - 245px));
                    }
                    .r-r {
                    float: none;
                    width: 100%;
                    }
                    h1.errornum {
                    font-size: 80px;
                    }
                    h2.error {
                    font-size: 23px;
                    color: #4e4e4e;
                    }

                    @media screen and (max-width:992px){div#error-page {height:auto;}}
                  </style>
                </b:includable>
                <b:includable id='sp-homePosts' var='post'>

                  <a class='Img-Holder thumb' expr:href='data:post.url' expr:title='data:post.title'>
                    <span expr:class='&quot;postcat catnum&quot; + data:i' rel='tag'><data:post.labels.first.name/></span>
                    <b:if cond='data:post.thumbnailUrl'>
                      <img class='post-thumb' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.thumbnailUrl, 1600)' expr:title='data:post.title' height='170' width='300'/>
                      <b:else/>
                      <span class='Noimger'/>
                    </b:if>
                  </a>

                  <div class='post-home cont'>
                    <div class='post-info'>
                      <span class='Date published updated'><svg><use href='#ic-clock'/></svg><a class='agotime' expr:datetime='data:post.lastUpdated.iso8601' expr:href='data:post.url'/></span>
                      <h2 class='rnav-title entry-title p-name'><a class='Title' expr:href='data:post.url' rel='bookmark'><data:post.title/></a></h2>
                    </div>
                    <div class='items'>
                      <b:if cond='data:post.author.profileUrl'>
                        <a class='author vcard' expr:href='data:post.author.profileUrl'>
                          <span class='fn'><data:post.author.name/></span></a>
                        <b:else/>
                        <span class='vcard'><span class='fn'><data:post.author.name/></span></span>
                      </b:if>
                    </div>
                    <div class='Short_content entry-content'><data:post.snippets.short/></div>
                    <a class='moreLink' expr:href='data:post.url' expr:title='data:post.title'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>read more<b:else/>اقرأ المزيد</b:if></a>
                  </div>
                </b:includable>
                <b:includable id='sp-navigation' var='post'>

                </b:includable>
                <b:includable id='sp-nextprev'>

                  <b:if cond='data:skin.vars.blogPager == &quot;2px&quot;'>
                    <div class='blog-pager-older-link' id='blog-pager'>
                      <b:if cond='data:newerPageUrl'>
                        <div id='blog-pager-newer-link'>
                          <a class='blog-pager blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' title='older'>
                            <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'><svg class='n-line icon right' style='transform: rotate(180deg);'><use href='#ic-arrow'/></svg><b:else/><svg class='n-line icon left'><use href='#ic-arrow'/></svg></b:if>
                          </a>
                        </div>
                      </b:if>
                      <div class='homelink' id='loadMorePosts'><a class='blog-pager' expr:href='data:blog.homepageUrl' title='Home'><svg class='n-line icon home'><use href='#ic-home'/></svg></a></div>
                      <b:if cond='data:olderPageUrl'>
                        <div id='blog-pager-older-link'>
                          <a class='blog-pager blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' title='NextUrl'>
                            <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'><svg class='n-line icon left'><use href='#ic-arrow'/></svg><b:else/><svg class='n-line icon right' style='transform: rotate(180deg);'><use href='#ic-arrow'/></svg></b:if>
                          </a>
                        </div>
                      </b:if>
                    </div>
                    <b:else/>
                    <div class='loadMore'>
                      <a class='blog-pager-older-link hide' expr:href='data:olderPageUrl' title='NextUrl'/>
                      <div expr:data-index='data:numPosts' id='loadMorePosts'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>Show more <b:else/>مشاهدة المزيد من المقالات</b:if></div>
                      <div id='loadMoreWait'><span class='spiner-icon'/> <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>Showing<b:else/>جاري التحميل ...</b:if></div>
                      <div id='loadMoreNomore'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>No More Posts<b:else/>لم يتم العثور على أي نتائج</b:if></div>
                    </div>
                  </b:if>

                </b:includable>
                <b:includable id='sp-postQuickEdit' var='post'>
                  <b:if cond='data:view.isPost'>
                    <!-- Quick Edit -->
                    <span expr:class='&quot;edit-post item-control &quot; + data:post.adminClass'>
                      <a expr:href='&quot;https://www.blogger.com/blog/post/edit/&quot; + data:blog.blogId + &quot;/&quot; + data:post.id' target='_blank'> <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>

                        <b:else/>

                        </b:if> </a>
                    </span></b:if>
                  <b:if cond='data:view.isPage'>
                    <!-- Quick Edit -->
                    <span expr:class='&quot;edit-post item-control &quot; + data:post.adminClass'>
                      <a expr:href='&quot;https://www.blogger.com/blog/page/edit/&quot; + data:blog.blogId + &quot;/&quot; + data:post.id' target='_blank'> <b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>

                        <b:else/>

                        </b:if> </a>
                    </span></b:if>
                </b:includable>
                <b:includable id='sp-postTags' var='post'>
                  <b:if cond='data:widgets.Blog.first.allBylineItems.labels and data:post.labels.any'>
                    <!-- Post Labels -->
                    <div class='post-tags'>
                      <span class='tagstitle'><b:if cond='data:blog.languageDirection == &quot;ltr&quot;'>Tags<b:else/>هذا المقال ضمن قسم</b:if></span>
                      <b:loop values='data:post.labels' var='label'>
                        <a expr:href='data:label.url' expr:title='data:label.name' rel='tag'><data:label.name/></a>
                      </b:loop>
                    </div>
                    <b:loop index='item' values='data:post.labels' var='label'>
                      <b:if cond='data:item lt 1'>
                        <script type='application/ld+json'>{
                          &quot;@context&quot;: &quot;http://schema.org&quot;,&quot;@type&quot;: &quot;BreadcrumbList&quot;,&quot;itemListElement&quot;: [{&quot;@type&quot;: &quot;ListItem&quot;,&quot;position&quot;: 1,&quot;item&quot;: {&quot;@id&quot;: &quot;<data:blog.homepageUrl.canonical/>&quot;,&quot;name&quot;: &quot;<data:blog.title/>&quot;}},{&quot;@type&quot;: &quot;ListItem&quot;,&quot;position&quot;: 2,&quot;item&quot;: {&quot;@id&quot;: &quot;<data:label.url.canonical/>&quot;,&quot;name&quot;: &quot;<data:label.name/>&quot;}},{&quot;@type&quot;: &quot;ListItem&quot;,&quot;position&quot;: 3,&quot;item&quot;: {&quot;@id&quot;: &quot;<data:post.url.canonical/>&quot;,&quot;name&quot;: &quot;<data:view.title.escaped/>&quot;}}]}</script>
                      </b:if>
                    </b:loop>
                  </b:if>
                </b:includable>
                <b:includable id='sp-sharePost' var='post'>

                  <b:if cond='data:widgets.Blog.first.allBylineItems.share and data:view.isPost'>
                    <div class='pSh'>
                      <div class='pShc' expr:data-text='data:messages.share + &quot; : &quot;'>
                        <!-- Share to Facebook -->
                        <a aria-label='Facebook' class='c fb' data-text='Share' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><svg class='n-line'><use href='#ic-facebook'/></svg></a>

                        <!-- Share to Whatsapp -->
                        <a aria-label='Whatsapp' class='c wa' data-text='Share' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><svg class='n-line'><use href='#ic-whatsapp'/></svg></a>

                        <!-- Share to Twitter -->
                        <a aria-label='Twitter' class='c tw' data-text='Tweet' expr:href='&quot;https://twitter.com/share?url=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><svg class='n-line'><use href='#ic-twitter'/></svg></a>

                        <label class='sharemore' expr:aria-label='data:messages.shareToOtherApps' for='forShare'><svg class='n-line'><use href='#ic-share'/></svg></label>
                      </div>
                    </div>

                  </b:if>

                  <b:include cond='data:post.shareUrl and data:view.isPost and !data:view.isPreview' name='postInfoShareMore'/>

                </b:includable>
                <b:includable id='theme-custom-lang'>
                  <b:switch var='data:message'>
                    <b:case value='prevPost'/> <data:post.author.name/>
                  </b:switch>
                </b:includable>
                <b:includable id='threadedCommentForm' var='post'><div id='comments-respond'><div class='conart'><a class='go-respond ribble' href='#item-comments' id='comment-post-message'><data:messages.postAComment/></a><b:if cond='data:this.messages.blogComment != &quot;&quot;'><p><data:this.messages.blogComment/></p></b:if></div><a expr:href='data:post.commentFormIframeSrc + &quot;&amp;skin=contempo&quot;' id='comment-editor-src' title='comment form link'/><iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:data-src='data:post.commentFormIframeSrc + &quot;&amp;skin=contempo&quot;' frameborder='0' height='95px' id='comment-editor' name='comment-editor' title='comment form' width='100%'/><noscript>&lt;!--<data:post.cmtfpIframe/>--&gt;</noscript></div></b:includable>
                <b:includable id='threadedCommentJs' var='post'/>
                <b:includable id='threadedComments' var='post'><section class='comments threaded' expr:data-embed='data:post.embedCommentForm' expr:data-num-comments='data:post.numberOfComments' id='comments-wrap'><b:if cond='data:post.allowNewComments'><div class='comment-footer'><b:include data='post' name='threadedCommentForm'/></div><b:else/><p class='c-not-allowed'><data:post.noNewCommentsText/></p></b:if><b:if cond='data:showCmtPopup'><p class='c-not-allowed'><data:post.noNewCommentsText/></p></b:if><div class='comments-content'><div class='comments-list' id='comment-holder'><ul/></div></div></section>
                </b:includable>
              </b:widget>
            </b:section>

            <b:section cond='data:view.isPost or data:view.isLayoutMode' id='PostA3lan2'/>
            <b:section cond='data:view.isPost or data:view.isLayoutMode' id='PostA3lan' maxwidgets='1' showaddelement='no'>
              <b:widget id='LinkList005' locked='true' title='أعلانات المقال أساسي' type='LinkList' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='shownum'>1</b:widget-setting>
                  <b:widget-setting name='sorting'>NONE</b:widget-setting>
                  <b:widget-setting name='text-0'>ad-bot</b:widget-setting>
                  <b:widget-setting name='link-0'><![CDATA[<!-- ShareThis BEGIN --> <div class="your-custom-div-class">    <p>ما مدي تقييمك لهذا المقال؟</p>    <div class="sharethis-inline-reaction-buttons"></div> </div> <!-- ShareThis END -->]]></b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'>

                  <b:loop index='i' values='data:widgets.LinkList any (l =&gt; l.sectionId == &quot;PostA3lan2&quot;)' var='widget'><b:if cond='data:i == 0'><b:if cond='!data:widget'><b:loop values='data:links' var='link'><b:if cond='data:link.name contains &quot;ad-&quot;'><div class='HTML' expr:id='data:link.name'><data:link.target/></div></b:if></b:loop>
                    <b:tag name='script' type='text/javascript'><b:loop index='x' values='data:links' var='link'><b:if cond='data:link.name contains &quot;ad-top&quot;'>_$(&#39;#top-a3lan&#39;).prepend(_$(&#39;#<data:link.name/>&#39;));</b:if><b:if cond='data:link.name contains &quot;ad-bot&quot;'>_$(&#39;#bot-a3lan&#39;).prepend(_$(&#39;#<data:link.name/>&#39;));</b:if><b:if cond='data:link.name contains &quot;ad-ret&quot;'>_$(&#39;#ret-a3lan&#39;).prepend(_$(&#39;#<data:link.name/>&#39;));</b:if><b:if cond='data:link.name contains &quot;ad-cent&quot;'>let len = document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0)&gt;*&#39;);if(len.length){len[Math.floor(len.length / 2)].after(_$(&#39;#<data:link.name/>&#39;))}else if(document.querySelector(&quot;#s7bcent-a3lan-PagePrake&quot;)){_$(&quot;#s7bcent-a3lan-PagePrake&quot;).prepend(_$(&#39;#<data:link.name/>&#39;))}</b:if><b:if cond='data:link.name contains &quot;ad-p-&quot;'>if(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0) p&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-p-&#39;)[1]]){document.querySelectorAll(&#39;.post-body p&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-p-&#39;)[1] - 1].after(_$(&#39;#<data:link.name/>&#39;))}else{_$(&#39;#<data:link.name/>&#39;).remove();}</b:if><b:if cond='data:link.name contains &quot;ad-h2-&quot;'>if(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0) h2&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h2-&#39;)[1] - 1]){document.querySelectorAll(&#39;.post-body h2&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h2-&#39;)[1] - 1].after(_$(&#39;#<data:link.name/>&#39;))}else{_$(&#39;#<data:link.name/>&#39;).remove();}</b:if><b:if cond='data:link.name contains &quot;ad-h3-&quot;'>if(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0) h3&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h3-&#39;)[1] - 1]){document.querySelectorAll(&#39;.post-body h3&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h3-&#39;)[1] - 1].after(_$(&#39;#<data:link.name/>&#39;))}else{_$(&#39;#<data:link.name/>&#39;).remove();}</b:if><b:if cond='data:link.name contains &quot;ad-h4-&quot;'>if(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0) h4&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h4-&#39;)[1] - 1]){document.querySelectorAll(&#39;.post-body h4&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-h4-&#39;)[1] - 1].after(_$(&#39;#<data:link.name/>&#39;))}else{_$(&#39;#<data:link.name/>&#39;).remove();}</b:if><b:if cond='data:link.name contains &quot;ad-bq-&quot;'>if(document.querySelectorAll(&#39;.post-body:not(.siki):not(.siki0) blockquote&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-bq-&#39;)[1] - 1]){document.querySelectorAll(&#39;.post-body blockquote&#39;)[&quot;<data:link.name/>&quot;.split(&#39;ad-bq-&#39;)[1] - 1].after(_$(&#39;#<data:link.name/>&#39;))}else{_$(&#39;#<data:link.name/>&#39;).remove();}</b:if></b:loop></b:tag></b:if></b:if></b:loop>

                </b:includable>
                <b:includable id='AUTH'/>
                <b:includable id='DEF'/>
                <b:includable id='content'/>
                <b:includable id='lista' var='widget'/>
              </b:widget>
            </b:section>

            <b:if cond='!data:view.isLayoutMode'><b:if cond='data:view.isSingleItem'><b:include name='ArticaleSittings'/></b:if></b:if>



            <!-- homepage Posts -->
            <div class='contpotg'>
              <b:section class='potg postTags' cond='data:view.isHomepage' id='Postcs5'/>
              <div class='towcol btg2'>
                <b:section class='potg sides postTags' cond='data:view.isHomepage' id='Postcs6'/>
                <b:section class='potg sides postTags' cond='data:view.isHomepage' id='Postcs7'/>
              </div>
              <b:section class='potg postTags' cond='data:view.isHomepage' id='Postcs8'/>
            </div>
          </div>

          <b:if cond='data:skin.vars.RemoveAdiseMopile == &quot;2px&quot; and data:blog.isMobileRequest'>
            <b:else/>
            <b:if cond='!data:view.isError'>
              <aside class='potg btg2' id='sidepar-wid'>
                <b:section id='sidepar'>
                  <b:widget id='LinkList4' locked='true' title='مواقع التواصل الإجتماعي' type='LinkList' version='2' visible='true'>
                    <b:includable id='main'><b:include name='widget-title'/><b:include name='content'/></b:includable>
                    <b:includable id='AUTH'/>
                    <b:includable id='DEF'/>
                    <b:includable id='content'><ul class='social-static social'><b:loop values='data:links' var='link'><li><a expr:href='data:link.target' expr:title='data:link.name' rel='nofollow noopener' target='_blank'><svg><use expr:href='&quot;#ic-&quot; + data:link.name'/></svg></a></li></b:loop></ul></b:includable>
                  </b:widget>
                </b:section>
              </aside>
            </b:if>
          </b:if>
        </div>

        <div class='EndSides'/>

        <!-- homepage Posts -->
        <div class='Treelists potg btg2'>
          <b:section class='trelists' cond='data:view.isHomepage' id='Postnw4'/>
          <b:section class='trelists' cond='data:view.isHomepage' id='Postnw5'/>
          <b:section class='trelists' cond='data:view.isHomepage' id='Postnw6'/>
        </div>
        <b:section class='fullwide' cond='data:view.isHomepage' id='BotPostsc'/>

      </div>

      <footer>
        <div class='container'>
          
          <div class='mid-top-footer'>
            <b:section class='footer-col' id='footer-col1'/>
            <b:section class='footer-col' id='footer-col2'/>
            <b:section class='footer-col' id='footer-col3'/>
            <b:section class='footer-col' id='footer-col4'/>
          </div>
        </div>
        
    <div class='bottom-footer'>
    <div class='container'>
      <div class='yemen'>
        <div class='shmal'>
        <div class='fotecol'>
              <img alt='موقع كوتشينا' decoding='async' height='70' loading='lazy' src='https://blogger.googleusercontent.com/img/a/AVvXsEiWuuXgWwdJnPuIlZkx7oYBB2jKJAuSbrm6phcvUD4VkeTAXnhbJHroqAzn5Pb1j-9kEk-jx8uUCP8ZZydqARy5qHpcWJ9Yri27A9J_3uas6BtEoE9Ia2zplr5DAQxPsdtehVN8gL4c5N0qvJp7nroDiwbffoqgGsgYReJMU5cnmMXqiufayueEI9CgO5CD=s250' width='250'>
              </img>
          <p style='float: right;'>قالب كوتشينا هو قالب عصري حديث يجمع بين السرعة والجمال&#1548; حاز القالب علي أعجاب مشرفي المواقع الإلكترونية منذ أطلاقه. ما يميز هذا القالب عن القوالب الأخري هو إمكانية تصميمه الحديث ولوحة تحكم بسيطة</p>
        </div>
        </div>
        </div>
        </div>
        </div>
        
                            <div class='bottom-footer'>
                                   <div class='shmal'>
              <b:section id='footer-social' maxwidgets='1' showaddelement='no'>
                <b:widget id='LinkList2' locked='true' title='مواقع التواصل الإجتماعي' type='LinkList' version='2' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='shownum'>4</b:widget-setting>
                    <b:widget-setting name='link-3'>https://cot12a.blogspot.com/</b:widget-setting>
                    <b:widget-setting name='sorting'>NONE</b:widget-setting>
                    <b:widget-setting name='text-1'>youtube</b:widget-setting>
                    <b:widget-setting name='link-1'>https://cot12a.blogspot.com/</b:widget-setting>
                    <b:widget-setting name='text-0'>facebook</b:widget-setting>
                    <b:widget-setting name='link-2'>https://cot12a.blogspot.com/</b:widget-setting>
                    <b:widget-setting name='text-3'>instagram</b:widget-setting>
                    <b:widget-setting name='link-0'>https://cot12a.blogspot.com/</b:widget-setting>
                    <b:widget-setting name='text-2'>twitter</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'><b:include name='content'/></b:includable>
                  <b:includable id='AUTH'/>
                  <b:includable id='DEF'/>
                  <b:includable id='content'><ul class='social-static social'><b:loop values='data:links' var='link'><li><a expr:href='data:link.target' expr:title='data:link.name' rel='nofollow noopener' target='_blank'><svg><use expr:href='&quot;#ic-&quot; + data:link.name'/></svg></a></li></b:loop></ul></b:includable>
                </b:widget>
              </b:section>
            </div>
            </div>

        <div class='bottom-footer'>
          <div class='container'>
            <div class='yemen'>
          <a href='https://cot12a.blogspot.com/' id='credit'>كوتشينـا</a>   جميع الحقوق محفوظة لـ  <a expr:href='data:blog.homepageUrl' id='7qok' target='_blank'><data:blog.title/></a>
            </div>

                      
            <div class='shmal'>
            <ul style='float: left;'>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/' style='color: white;'>الرئيسية</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_3.html' style='color: white;'>اتصل بنا</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page.html' style='color: white;'>من نحن</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_30.html' style='color: white;'>الأحكام والشروط</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_79.html' style='color: white; '>الفهرس</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_57.html' style='color: white;'>أتفاقية الأستخدام</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_17.html' style='color: white;'>سياسية الخصوصية</a></li>
              <li style='display: inline; margin-right: 10px;'><a href='https://kootcheena.blogspot.com/p/blog-page_9.html' style='color: white;'>نبذة عن هاجر يوسف</a></li>

           </ul>
           </div> 
         </div>
        </div>  
      </footer>
      
      <b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;5px&quot;'>
        <b:if cond='data:skin.vars.MopileFasterVirsonFot'>
          <!-- Mopile buttons -->
          <b:if cond='data:skin.vars.disapledarck == &quot;1px&quot;'><b:if cond='data:skin.vars.MopileFasterVirsonFot == &quot;1px&quot; or data:skin.vars.MopileFasterVirsonFot == &quot;4px&quot;'><div class='Dmode' onclick='darkMode()'><svg class='line linedd'><use href='#ic-moon-sun'/></svg></div></b:if></b:if>
          <div class='toTopB' id='backTop' onclick='window.scrollTo({top: 0});'><b:include name='arrow-up-circle-icon'/></div>
          <b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;4px&quot;'>
            <b:if cond='data:skin.vars.MopileFasterVirsonFot != &quot;1px&quot; and data:skin.vars.MopileFasterVirsonFot != &quot;4px&quot;'><label for='offNav' id='lamiabutton'><svg class='n-line'><use href='#ic-settings'/></svg></label></b:if>
            <div id='mobile-menu'><div class='Circalewhy2'><div class='Circalewhy'><b:include name='mopilemenu'/></div></div></div>
          </b:if>
          <!-- Mopile buttons -->
        </b:if>
      </b:if>
      <b:if cond='!data:view.isLayoutMode'><b:if cond='data:view.isSingleItem'><b:include name='CommentSittings'/></b:if></b:if>


      <b:if cond='data:view.isSingleItem'><div id='ReadPage'/></b:if>
      <b:if cond='data:skin.vars.PostSittings == &quot;2px&quot;'><b:include name='PostSittings'/></b:if></div>

    <b:include name='themeFunctions'/>

    <svg class='hide'>
      <b:include name='themeIcons'/>
    </svg>
    <b:if cond='!data:view.isLayoutMode'><b:include name='customeIcons'/></b:if>
    <b:if cond='!data:view.isLayoutMode'><b:include name='customeAnalytics'/></b:if>
        <script async='async' src='https://platform-api.sharethis.com/js/sharethis.js#property=6483448e8bdd800012e15fc2&amp;product=inline-reaction-buttons' type='text/javascript'/>

    &lt;noscript id=&#39;blogger-components&#39;&gt;</body>&lt;/noscript&gt;&lt;/body&gt;
  
</html>
