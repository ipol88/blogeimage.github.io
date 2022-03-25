<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' b:templateUrl='indie.xml' b:templateVersion='1.3.0' expr:dir='data:blog.languageDirection' lang='id' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>      
    <b:attr name='xmlns' value=''/>
	<b:attr name='xmlns:b' value=''/>
	<b:attr name='xmlns:expr' value=''/>
	<b:attr name='xmlns:data' value=''/>
  <b:if cond='data:view.isError'><title>Error 404: Page Not Found</title></b:if>
  <b:if cond='data:view.isHomepage'><title><data:blog.pageTitle/></title></b:if>
  <b:if cond='!data:view.isMultipleItems'><title><data:blog.pageName/> - <data:blog.title/></title></b:if>
  <b:if cond='data:view.isMultipleItems'>
    <b:if cond='data:view.search.query'><title><data:messages.search/>: <data:view.search.query/> - <data:blog.title/></title></b:if>
    <b:if cond='data:view.search.label'><title><data:blog.pageName/> - <data:blog.title/></title></b:if>
    <b:if cond='data:view.isArchive'><title><data:messages.blogArchive/>: <data:blog.pageName/> - <data:blog.title/></title></b:if>
    <b:if cond='data:view.search and !data:view.search.label and !data:view.search.query and !data:view.isArchive'><title><data:messages.posts/>: <data:blog.title/></title></b:if>
  </b:if>
  <!-- Meta Title -->
  <b:if cond='data:view.isMultipleItems'>
    <meta expr:content='data:blog.pageTitle' property='og:title'/>
    <meta expr:content='data:blog.pageTitle' property='og:image:alt'/>
    <meta expr:content='data:blog.pageTitle' name='twitter:title'/>
    <meta expr:content='data:blog.pageTitle' name='twitter:image:alt'/>
    <b:else/>
    <meta expr:content='data:blog.pageName' property='og:title'/>
    <meta expr:content='data:blog.pageName' property='og:image:alt'/>
    <meta expr:content='data:blog.pageName' name='twitter:title'/>
    <meta expr:content='data:blog.pageName' name='twitter:image:alt'/>
  </b:if>
  <meta expr:content='data:blog.title' property='og:site_name'/>
    <b:if cond='data:blog.postImageUrl'>
<meta expr:content='data:blog.postImageUrl' property='og:image:secure_url'/>
  </b:if>
  <!-- Meta Image -->
  <b:if cond='data:blog.postImageUrl'>
    <meta expr:content='data:blog.postImageUrl' property='og:image'/>
    <b:else/>
    <b:if cond='data:blog.postImageThumbnailUrl'>
      <meta expr:content='data:blog.postThumbnailUrl' property='og:image'/>
      <b:else/>
      <meta content='ce3046516bef6e55bfeed5c61bc8cf97' name='p:domain_verify'/>
      <meta content='https://1.bp.blogspot.com/-8iwc70zdPfg/XoeWd_PgAsI/AAAAAAAAEtE/P1Gd2XH40g0jJN5IlJNH8I0DBgyAW_kbACLcBGAsYHQ/s640/dog-4977599_1280-picsay.jpg' property='og:image'/>
    </b:if>
  </b:if>
  <b:if cond='data:view.isMultipleItems'>
    <meta content='https://1.bp.blogspot.com/-8iwc70zdPfg/XoeWd_PgAsI/AAAAAAAAEtE/P1Gd2XH40g0jJN5IlJNH8I0DBgyAW_kbACLcBGAsYHQ/s640/dog-4977599_1280-picsay.jpg' name='twitter:image'/>
    <b:else/>
    <meta expr:content='data:blog.postImageUrl' name='twitter:image'/>
  </b:if>
  <b:if cond='data:view.isPost'>
    <link expr:href='resizeImage(data:blog.postImageUrl, 700, &quot;18:9&quot;)' rel='image_src'/>
  </b:if>
  
  <!-- Meta Description -->
<b:if cond='data:view.isSearch'>
    <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title + &quot; - &quot; + data:blog.metaDescription' name='description'/> 
    <b:else/>
        <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title + &quot; - &quot; + data:blog.homepageUrl' name='description'/>
    </b:if>
<b:elseif cond='data:view.isHomepage'/>
    <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription + &quot; - &quot; + data:blog.title' name='description'/>
    <b:else/>
        <meta expr:content='data:blog.title + &quot; - &quot; + data:blog.homepageUrl' name='description'/>
    </b:if>
<b:elseif cond='data:view.isSingleItem'/>
    <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription + &quot; - &quot; + data:blog.title' name='description'/>
    <b:else/>
        <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='description'/>
    </b:if> 
</b:if>
<b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' property='og:description'/>
    <b:else/>
    <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:description'/>
  </b:if>
<b:if cond='data:blog.metaDescription'>
  <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
      <b:else/>
  <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:description'/>
  </b:if>
  <!-- Meta Keywords -->
  <meta expr:content='data:blog.title + &quot;, &quot; + data:blog.pageName' name='keywords'/>
  <meta expr:content='data:blog.title' property='article:tag'/>
  
  <!-- Link Canonical -->
  <link expr:href='data:blog.url' rel='canonical'/>
  <link expr:href='data:blog.url' hreflang='x-default' rel='alternate'/>
  <meta expr:content='data:blog.canonicalUrl' property='og:url'/>
  
  <!-- Site Owner -->
  <meta content='Admin' name='Author'/>
  <link href='https://www.facebook.com/IDLang' rel='me'/>
  <link href='https://www.facebook.com/IDLang' rel='author'/>
  <link href='https://www.facebook.com/IDLang' rel='publisher'/>
  <meta content='100001578783517' property='fb:admins'/>
  <meta content='696750553739909' property='fb:pages'/>
  <meta content='1804789006468790' property='fb:app_id'/>
  <meta content='https://www.facebook.com/100001578783517' property='article:author'/>
  <meta content='https://www.facebook.com/100001578783517' property='article:publisher'/>
  <meta content='' name='twitter:site'/>
  <meta content='' name='twitter:creator'/>

  <!-- Link Icon -->
  <link expr:href='data:blog.homepageUrl + &quot;/favicon.ico&quot;' rel='icon' type='image/x-icon'/>

  <!-- Theme Color -->
  <meta content='#f7f9f8' name='theme-color'/>
  <meta content='#f7f9f8' name='msapplication-navbutton-color'/>
  <meta content='#f7f9f8' name='apple-mobile-web-app-status-bar-style'/>
  <meta content='yes' name='apple-mobile-web-app-capable'/>
  
  <!-- Blogger Rss -->
  <meta content='blogger' name='generator'/>
  <link href='https://www.blogger.com/openid-server.g' rel='openid.server'/>
  <link expr:href='data:blog.url' rel='openid.delegate'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link expr:href='&quot;//www.blogger.com/feeds/&quot; + data:blog.blogId + &quot;/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - RSS&quot;' rel='alternate' type='application/rss+xml'/>
  
  <!-- Open Graph -->
  <meta content='article' property='og:type'/>
  <meta content='id_ID' property='og:locale'/>
  <meta content='en_US' property='og:locale:alternate'/>
  <meta content='en_GB' property='og:locale:alternate'/>
  <meta content='summary_large_image' name='twitter:card'/>
    
  <!-- Robots Search -->
  <meta content='width=device-width, initial-scale=1.0, user-scalable=1.0, minimum-scale=1.0, maximum-scale=5.0' name='viewport'/>
  <meta content='text/html; charset=UTF-8' http-equiv='Content-Type'/>
  <meta content='IE=Edge' http-equiv='X-UA-Compatible'/>
  <meta content='Indonesia' name='geo.placename'/>
  <meta content='id' name='geo.country'/>
  <meta content='ID-BT' name='geo.region'/>
  <meta content='id' name='language'/>
  <meta content='global' name='target'/>
  <meta content='global' name='distribution'/>
  <meta content='general' name='rating'/>
  <meta content='1 days' name='revisit-after'/>
  <meta content='true' name='MSSmartTagsPreventParsing'/>
  <meta content='index, follow' name='googlebot'/>
  <meta content='follow, all' name='Googlebot-Image'/>
  <meta content='follow, all' name='msnbot'/>
  <meta content='follow, all' name='Slurp'/>
  <meta content='follow, all' name='ZyBorg'/>
  <meta content='follow, all' name='Scooter'/>
  <!-- Sife Verification -->
  <meta content='XXXX' name='google-site-verification'/>
  <meta content='XXXX' name='msvalidate.01'/>
  <meta content='XXXX' name='p:domain_verify'/>
  <meta content='XXXX' name='majestic-site-verification'/>
  <meta expr:content='data:blog.title' name='copyright'/>
  <link crossorigin='' href='https://res.cloudinary.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://www.blogger.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://fonts.gstatic.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://fonts.googleapis.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://resources.blogblog.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://www.google-analytics.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://www.gstatic.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://www.googletagservices.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://cdn.ampproject.org' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://3p.ampproject.net' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://tpc.googlesyndication.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://www.googletagmanager.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://1.bp.blogspot.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://2.bp.blogspot.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://3.bp.blogspot.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://4.bp.blogspot.com' rel='preconnect dns-prefetch'/><link crossorigin='' href='https://cdn.statically.io' rel='preconnect dns-prefetch'/>
   <script type='application/ld+json'>{ &quot;@context&quot;: &quot;http://schema.org&quot;, &quot;@type&quot;: &quot;WebSite&quot;, &quot;@id&quot;: &quot;#website&quot;, &quot;url&quot;: &quot;<data:blog.homepageUrl/>&quot;, &quot;potentialAction&quot;: { &quot;@type&quot;: &quot;SearchAction&quot;, &quot;target&quot;: &quot;<data:blog.homepageUrl/>search?q={search_term}&quot;, &quot;query-input&quot;: &quot;required name=search_term&quot; } }</script>

  &lt;style&gt;&lt;!-- /* <b:skin version='1.3.0'><![CDATA[ 
				-----------------------------------------------
				Blogger Template Style
				Name        : Wallpaper Blogger Template
				Create by : https://fyi.my.id
				----------------------------------------------- */

	/* Variable definitions start
   ==========================
   <Variable name="keycolor" description="Main Color" type="color" default="#43ce8e" value="#000000"/>

   <Group description="Text Halaman" selector="body">
     <Variable name="body.font" description="Font" type="font"
         default="normal normal 16px Roboto, Arial, sans-serif" value="normal normal 16px Roboto, Arial, sans-serif"/>
     <Variable name="body.text.color" description="Main Text Color" type="color" default="#777777" value="#222222"/>
   </Group>

   <Group description="Backgrounds" selector=".body-fauxcolumns-outer">
     <Variable name="body.background.color" description="Body" type="color" default="#ffffff" value="#b22e2e"/>
     <Variable name="header.background.color" description="Header" type="color" default="#43ce8e" value="#b22e2e"/>
	 <Variable name="widget.background.color" description="Widget" type="color" default="#f7f7f7" value="#f1f1f1"/>
	 <Variable name="footer.background.color" description="Footer" type="color" default="#222222" value="#000000"/>
   </Group>
   
   <Variable name="body.background" description="Body Background" type="background"
       color="$(body.background.color)" default="$(color) none repeat scroll top left" value="#000000 url(https://themes.googleusercontent.com/image?id=19aLMMHI-WXcxsojpERe8MlodYlS7yd1qQU1wcTStU21I3bbY7bmlrvVCWE474_XXwWjd) no-repeat scroll top center /* Credit: fpm (http://www.istockphoto.com/portfolio/fpm?platform=blogger) */"/>
   <Variable name="body.background.override" description="Body Background Override" type="string" default="" value=""/>
   
   <Group description="Links" selector=".main-outer">
     <Variable name="link.color" description="Link Color" type="color" default="#1a73e8" value="#b3b712"/>
     <Variable name="link.visited.color" description="Visited Color" type="color" default="#3688d7" value="#b7af24"/>
     <Variable name="link.hover.color" description="Hover Color" type="color" default="#3688d7" value="#b7af24"/>
   </Group>

   <Group description="Widget" selector="#widget-footer-container">
     <Variable name="widget.color" description="Color" type="color" default="#777777" value="#535353"/>
	 <Variable name="widget.link.color" description="Link Color" type="color" default="#43ce8e" value="#b22e2e"/>
	 <Variable name="widget.hover.color" description="Hover Color" type="color" default="#777777" value="#535353"/>
   </Group>
   
   <Group description="Footer" selector="#footer-wrapper">
     <Variable name="footer.color" description="Color" type="color" default="#dddddd" value="#d5d5d5"/>
	 <Variable name="footer.link.color" description="Link Color" type="color" default="#dddddd" value="#d5d5d5"/>
	 <Variable name="footer.hover.color" description="Hover Color" type="color" default="#ffffff" value="#ffffff"/>
   </Group>

   Variable definitions end
   ========================*/

html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;/*font-size:100%;*/font:inherit;vertical-align:baseline;}

/* HTML5 display-role reset for older browsers */
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block;}body{line-height:1;display:block;}*{margin:0;padding:0;}html{display:block;}blockquote,q{quotes:none;}table{border-collapse:collapse;border-spacing:0;}

/* Blogger CSS Reset */
.section,.widget{margin:0 0 0 0;padding:0 0 0 0;}
.navbar,.blog-feeds,.feed-links,#backlinks-container,a.home-link,.blog-mobile-link{display:none;}
.post-body .separator > a, .post-body .separator > span {margin-left: 0 !important;}

.quickedit,.thread-toggle,.edit-post,.item-control{display:none;}

/* FRAMEWORK */
strong,b{font-weight:bold;}
cite,em,i{font-style:italic;}
a{color:$(link.color);text-decoration:none;outline:none;}
a:hover{color:$(link.hover.color);text-decoration:none;}
a img{border:none;border-width:0;outline:none;}
abbr,acronym{border-bottom:1px dotted;cursor:help;}
sup,sub{vertical-align:baseline;position:relative;top:-.4em;font-size:86%;}
sub{top:.4em;}small{font-size:86%;}
kbd{font-size:80%;border:1px solid #777;padding:2px 5px;border-bottom-width:2px;border-radius:3px;}
mark{background-color:#ffce00;color:black;}
p,blockquote,pre,table,figure,hr,form,ol,ul,dl{margin:0;}
hr{height:1px;border:none;background-color:#666;}

/* heading */
h1,h2,h3,h4,h5,h6 {margin: 0 0 0.6em;letter-spacing: -0.2px;}
h1{font-size:1.8rem}
h2{font-size:1.6rem}
h3{font-size:1.4rem}
h4{font-size:1.2rem}
h5{font-size:1rem}
h6{font-size:0.9rem}

/* list */
ol,ul,dl{margin: 0}
.post ol {display: block;list-style-type: decimal;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;padding-inline-start: 40px;}
.post ul {display: block;list-style-type: disc;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;padding-inline-start: 40px;}
dt{font-weight: 500}

/* form */
input,button,select,textarea{font:inherit;font-size:100%;line-height:normal;vertical-align:baseline;}
textarea{display:block;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;}

/* code & blockquote */
.post pre{font-size:12px;position:relative;background-color:#161617;color:#bbc2e2;border-radius:10px;padding:15px 20px;margin:20px auto;-moz-tab-size:2;-o-tab-size:2;tab-size:2;-webkit-hyphens:none;-moz-hyphens:none;-ms-hyphens:none;hyphens:none;transition:all .2s ease;overflow:auto;font-family:'source code pro',menlo,consolas,monaco,monospace;line-height:1.5em;}
.post pre code{display:block;padding:0;white-space:pre}
.post pre span{color:#3a7bd5}
.post pre span.block{color:#fff;background:#3a7bd5}
.post pre i{color:#519bd6}
.post pre i.comment{color:#898ea4;user-select:text;-moz-user-select:text;-ms-user-select:text;-khtml-user-select:text;-webkit-user-select:text;-webkit-touch-callout:text;}
.post .code{display:inline-block;font-size:.98rem;line-height:1.48rem;color:#3a7bd5}
blockquote{position:relative;color:#767676;font-size:15px;line-height:1.48em}

/* Addtional Style */
.button{display:inline-flex;align-items:center;margin:15px 15px 15px 0;padding:10px 20px;outline:0;border:0;color:#fefefe;background-color:#3a7bd5;border-radius:3px;font-size:13px;line-height:22px;}
.button.outline{color:#505050;background-color:transparent;border:1px solid #767676}
.button.whatsapp{background-color:#25D366}
.button:hover{color:#fefefe;opacity:.75}
.button.outline:hover{color:#3a7bd5;border-color:#3a7bd5}
.button-info{display:flex;flex-wrap:wrap;justify-content:center;margin:12px 0 0}
.button-info > *{margin:0 12px 12px 0}
.button-info > *:last-child{margin-right:0}
.lazy-youtube{background-color:#505050;position:relative;overflow:hidden;padding-top:56.30%;cursor:pointer;border-radius:8px;}
.lazy-youtube img{width:100%;top:-16.84%;left:0;opacity:.95;cursor:pointer}
.lazy-youtube .play-button{width:60px;height:60px;z-index:1;opacity:.98;border-radius:50px;border:2px solid rgba(255,255,255,.8);cursor:pointer}
.lazy-youtube .play-button:hover{border-color:#3a7bd5}
.lazy-youtube .play-button:hover:before{border-color:transparent transparent transparent #3a7bd5}
.lazy-youtube .play-button:before{content:'';border-style:solid;border-width:12px 0 12px 18px;border-color:transparent transparent transparent rgba(255,255,255,.8);border-radius:3px;margin-left:1px}
.lazy-youtube img, .lazy-youtube iframe, .lazy-youtube .play-button,.lazy-youtube .play-button:before{position:absolute!important}
.lazy-youtube .play-button, .lazy-youtube .play-button:before{top:50%;left:50%;transform:translate3d(-50%,-50%,0)}
.lazy-youtube iframe{height:100%;width:100%;top:0;left:0}
.lazy-youtube .playBut{display:inline-block;position:absolute;width:70px;height:70px;z-index:1;top:50%;left:50%;transform:translate3d(-50%,-50%,0);-webkit-transform:translate3d(-50%,-50%,0);-webkit-transition:all 0.5s ease;transition:all 0.5s ease}
.lazy-youtube .playBut svg{width:inherit;height:inherit}
.lazy-youtube .playBut .svg-play{fill:none;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;stroke-width:7}
.lazy-youtube .circle{stroke:rgba(255,255,255,.8);stroke-dasharray:650;stroke-dashoffset:650;-webkit-transition:all 0.5s ease-in-out;transition:all 0.5s ease-in-out;opacity:0.3;}
.lazy-youtube .triangle{stroke:rgba(255,255,255,.8);stroke-dasharray:240;stroke-dashoffset:480;-webkit-transition:all 0.7s ease-in-out;transition:all 0.7s ease-in-out;transform:translateY(0);-webkit-transform:translateY(0)}
.lazy-youtube .playBut:hover .triangle{stroke-dashoffset:0;opacity:1;stroke:#fefefe;animation:nudge 0.7s ease-in-out;-webkit-animation:nudge 0.7s ease-in-out}
.lazy-youtube .playBut:hover .circle{stroke-dashoffset:0;opacity:1;stroke:#fefefe}
.post .accordion{position:relative;list-style:none;margin:20px 0 0;padding:0!important;display:flex;flex-wrap:wrap}
.post .accordion li{width:100%;padding:12px 0;border-bottom:1px solid #ebeced}
.post .accordion .accor-title{display:flex;align-items:center}
.post .accordion .accor-title .icon-2{display:none}
.post .accordion .accor-title svg{flex-shrink:0;width:18px;height:18px;margin-right:12px;-webkit-transition:all .1s ease;transition:all .1s ease;}
.Blog .accordion .accor-title .title{flex-grow:1;margin:0;line-height:1.48em;font-weight:700;font-size:14px;-webkit-transition:all .1s ease;transition:all .1s ease;}
.post .accordion .accor-menu:checked + .accor-title .icon-1{display:none}
.post .accordion .accor-menu:checked + .accor-title .icon-2{display:block}
.post .accordion .accor-menu:checked + .accor-title svg,
.post .accordion .accor-menu:checked + .accor-title .title{stroke:#3a7bd5;color:#3a7bd5}
.post .accordion .accor-menu:checked + .accor-title + .content{height:100px;padding:15px 0}
.post .accordion .content{margin:0;padding:0;position:relative;overflow:hidden;height:0;font-size:14px;-webkit-transition:all .2s ease;transition:all .2s ease;}
svg .svg-c{fill:#3a7bd5}
svg.line{fill:none;stroke:#161617;stroke-linecap:round;stroke-linejoin:round;stroke-width:1.5}
svg.line .svg-c{fill:none;stroke:#3a7bd5}
.Blog .daftar-isi{border-top:1px solid rgba(0,0,0,.05);border-bottom:1px solid rgba(0,0,0,.05);padding:25px 15px;margin:30px 0;font-size:14px}
.post .daftar-isi .isi-judul{outline:0;font-weight:700;display:flex;cursor:pointer}
.post .daftar-isi .isi-judul:after{content:'Sembunyikan';font-weight:400;font-size:12px;margin-left:auto}
.post .daftar-isi .isi-content{}
.post .daftar-isi .isi-content ol{counter-reset:daftar-count;margin-bottom:0;padding:0;list-style:none}
.post .daftar-isi .isi-content ol ol{width:100%;margin-left:25px}
.post .daftar-isi .isi-content ol li{display:flex;align-items:flex-start;flex-wrap:wrap}
.post .daftar-isi .isi-content ol li a{display:inline-block;max-width:calc(100% - 20px)}
.post .daftar-isi .isi-content li ul li a{max-width:none}
.post .daftar-isi .isi-content ol li:before{content:counter(daftar-count) '.';counter-increment:daftar-count;min-width:20px;color:#505050;flex-shrink:0}
.post .daftar-isi .isi-content ol ul{width:100%;padding-left:45px}
.post .daftar-isi .isi-content ol ul li{display:list-item}
.post .daftar-isi .isi-content ol ul li:before{display:none}
.post .daftar-isi .isi-content ul{margin-bottom:0;padding-left:20px}
.post .daftar-isi .isi-input:checked + .isi-judul + .isi-content{display:none}
.post .daftar-isi .isi-input:checked + .isi-judul:after{content:'Tampilkan'}
.post .spoiler .spoiler-judul{margin:15px 0}
.post .spoiler .spoiler-isi{display:none}
.post .spoiler .spoiler-isi pre{margin-top:0}
.post .spoiler .spoiler-judul .button{margin:0 0 0 0;padding:4px 12px;font-size:11px}
.post .spoiler .spoiler-judul .button:before{content:'Tampilkan'}
.post .spoiler .spoiler-input:checked + .spoiler-judul .button:before{content:'Sembunyikan'}
.post .spoiler .spoiler-input:checked + .spoiler-judul + .spoiler-isi{display:block}
.credit {text-align: center;position: absolute;bottom: 0;background: #333;width: 100%;}
.credit, .credit a {visibility: visible!important;display: block!important;}
.credit a {color: #fff;}
/* table */
.post table.tr-caption-container{min-width:100%;width:auto;margin:0 auto;border:0;position:relative}
.post table.tr-caption-container tbody{border:0}
.post table.tr-caption-container tr td{background-color:transparent;border:0;padding:0;position:relative}
.post table.tr-caption-container tr:nth-child(2n+1) td, .Blog table.tr-caption-container tr:nth-child(2n+1) td:first-child{border:0}
.post table.tr-caption-container a, .Blog table.tr-caption-container img{display:block}
.post table.tr-caption-container .tr-caption{position:relative;bottom:0;right:0;display:block;font-size:10px;color:inherit;background-color:transparent;margin-top:5px;padding:5px 15px;border:0;border-radius:10px 0 10px 0}
.post table{min-width:70%;margin:0 auto;border:0px solid rgba(0,0,0,.05);border-bottom:1px solid rgba(0,0,0,.05);border-radius:3px;overflow:hidden;font-size:14px;}
.post table th{background-color:#505050;color:#fff;padding:10px;border-right:1px solid rgba(255,255,255,.25)}
.post table th:last-child, .Blog table tr td:last-child, .Blog table tr:nth-child(2n) td:last-child{border-right:0}
.post table tr:nth-child(2n+1) td:first-child{border-left:1px solid rgba(0,0,0,.05)}
.post table tr:nth-child(2n+1) td{border-right:1px solid rgba(0,0,0,.05)}
.post table td{padding:10px 15px;border:0;vertical-align:middle;}
.post table tr:nth-child(2n) td{background-color:rgba(0,0,0,.05);border-right:1px solid rgba(0,0,0,.06)}
.post .table{display:block;overflow-y:hidden;overflow-x:auto;border-radius:3px}

img {max-width: 100%;height: auto;margin-left: auto;margin-right: auto;display: block;}
iframe {max-width: 100%;}
td.tr-caption {color: #777;}
.clear {clear: both;}
.clear:after {visibility: hidden;display: block;font-size: 0;content: " ";clear: both;height: 0;}

/* TRANSISI */
a:link, .label-count, #cssmenu ul ul li, #cssmenu > ul > li.has-sub > a:before, #cssmenu ul ul li.has-sub > a:before, .button:before, .button.menu-opened:after {transition:all 0.2s;-moz-transition:all 0.2s;-webkit-transition:all 0.2s;}
body {background: $(body.background);margin: 0 0 0 0;padding: 0 0 0 0;color: $(body.text.color);font: $(body.font);text-align: left;}

/* WRAPPER */
#wrapper {width: 100%;background-color: #fff;margin: 0 auto;overflow: hidden;box-sizing: border-box;padding-top:45px!important;max-width:1300px;}
.above-post-widget h2 {font-size: 18px;}
.above-post-widget .widget {margin-bottom: 30px;}
.above-post-widget .Image {background: #f7f7f7;}

/* Image Widget */
.above-post-widget .Image {text-align: center;}
.above-post-widget .Image h2 {font-size: 18px;color: #000;margin: 0 0;padding: 10px;font-weight: 500;text-transform: uppercase;}
.above-post-widget .Image span.caption {padding: 15px 10px 20px 10px;display: block;font-size: 18px;line-height: 1.8;}
.above-post-widget .Image img {width: auto;max-width: 100%;}

/* POST WRAPPER */
#post-wrapper {background: transparent;width: 100%;margin: 0 0 10px;}
.breadcrumbs{text-align: center;line-height:1.2em;width:auto;overflow:hidden;margin:0;padding:20px 0 0 0;font-size:80%;color:#888;font-weight:400;text-overflow:ellipsis;-webkit-text-overflow:ellipsis;white-space:nowrap}
.breadcrumbs a{display:inline-block;text-decoration:none;transition:all .3s ease-in-out;color:#666;font-weight:400}
.breadcrumbs a:hover{color:#11589D}
.breadcrumbs svg{width:16px;height:16px;vertical-align:-4px}
.breadcrumbs svg path{fill:#666}
.post {position: relative;}
.post-info {font-size: 15px;color: #999;}
.post-body {line-height: 1.6em;text-align: left;}
h2.post-title, h1.post-title {font: normal 15px Roboto, Arial, sans-serif;}
h1.post-title {font-size: 28px;text-transform: uppercase;}
h2.post-title {margin-bottom: 5px;}
h2.post-title a, h1.post-title a, h2.post-title, h1.post-title {color: #555;}
h2.post-title a:hover, h1.post-title a:hover {color: #333;}
.img-thumbnail {position: relative;height: auto;transition: transform .2s;}
.img-thumbnail img {height: auto;width: 100%;display: block;border-radius: 7px;}
.img-thumbnail:hover, .img-thumbnail-popular:hover {opacity: 0.9;transform: scale(0.93);}
.widget ul {line-height:inherit;}
#Label1 {width: 100%;overflow: hidden;}
#labelbottom {width: 100%;overflow: hidden;margin: auto;transition: all .3s }
#Label1 .cloud-label-widget-content {white-space: nowrap;overflow: hidden;padding-bottom: 10px;}
.labelbottom.scrolled {position: fixed;z-index: 9999;background: #fff;top: 54px;margin-top: 0!important;box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);}
.label-bawah-menu {transition: all 0.25s;-moz-transition: all 0.25s;-webkit-transition: all 0.25s;line-height: 1.2;}
.label-bawah-menu a {font-weight: 600;color: #333;display: inline-block;background: #fff;padding: 7px;font-size: 12px;box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);text-transform: uppercase;margin: 3px;border-radius: 5px;}
.cloud-label-widget-content{text-align: left;font-weight: 500;}
.label-size {transition: all 0.25s;-moz-transition: all 0.25s;-webkit-transition: all 0.25s;line-height :1.2;margin: 0 3px 3px 0;color: $(link.color);font-size: 12px;text-transform: uppercase;border: 2px solid #444444;border-radius: 3px;}
.label-size a, .label-size span{display: inline-block;color: $(widget.link.color);padding: 6px 8px;}
.label-size:hover {border: 2px solid $(widget.hover.color);}
.label-size:hover a, .label-size:hover .label-count {color: $(widget.hover.color);}
.label-count {margin-left: -16px;}
#Label1 .cloud-label-widget-content::-webkit-scrollbar {background: transparent;width: 8px;height: 8px;}
#Label1 .cloud-label-widget-content::-webkit-scrollbar-button {width: 0;height: 0;}
#Label1 .cloud-label-widget-content::-webkit-scrollbar-thumb {min-height: 48px;min-width: 48px;background-color: rgba(0,0,0,0.26);}
.PopularPosts ul, .PopularPosts ul li, .PopularPosts ul li img, .PopularPosts ul li a, .PopularPosts ul li a img {margin:0 0;padding:0 0;list-style:none;border:none;outline:none;border-radius: 10px;}
.PopularPosts ul {margin: 0;}
.PopularPosts ul li img {display: block;}
.PopularPosts ul li {margin: 0 10px 10px 0;display: inline-block;vertical-align: top;}
.PopularPosts ul li .item-title a {	font-weight: 500;display: block;padding: 5px 3px;}
.PopularPosts ul li > a {padding: 2px 6px;margin: -3px 0;display: block;border: 2px solid $(widget.link.color);border-radius: 3px;font-size: 12px;text-transform: uppercase;}
.PopularPosts ul li > a:hover {border: 2px solid $(widget.hover.color);}
.PopularPosts .item-content {position: relative;width: 80px;margin-right: 10px;}
.PopularPosts .item-title {line-height: 1.3;font-size: 13px;text-align: center;overflow: hidden;}
.PopularPosts .item-thumbnail {float: none;margin: 0 0;}
.PopularPosts .item-thumbnail:hover {opacity: 0.9;}
.PopularPosts .item-snippet {display: none;}
.Profile .widget-content {text-align: center;background: #c5c5c5;padding: 30px;border-radius: 10px;}
.Profile .profile-img {border-radius: 50%;float: none;}
.Profile .profile-name-link {
font-size: .9em;opacity: .87;overflow: hidden;}
.Profile .profile-link {border-style: solid;border-width: 2px;cursor: pointer;font-size: 13px;font-weight: 500;padding: 6px 22px;display: inline-block;line-height: normal;border-radius: 3px;}
.profile-textblock {margin: .8em 0;font-size: 14px;}
.profile-img {float: left;display:inline;opacity:10;margin:0 6px 3px 0;}
.profile-data {margin: 0;}
.profile-datablock {margin: .5em 0;}
.profile-name-link {background: no-repeat left top;box-sizing: border-box;display: inline-block;max-width: 100%;min-height: 20px;padding-left: 20px;}

/* Archive */
#ArchiveList .toggle {cursor: pointer;font-family: Arial, sans-serif;}
#ArchiveList .toggle-open {_font-size: 1.7em;line-height: .6em;}
#ArchiveList {text-align: left;}
#ArchiveList a.post-count-link, #ArchiveList a.post-count-link:link, #ArchiveList a.post-count-link:visited {
	text-decoration: none;
}
#ArchiveList a.toggle, #ArchiveList a.toggle:link, #ArchiveList a.toggle:visited, #ArchiveList a.toggle:hover {color: inherit;text-decoration: none;}
.BlogArchive #ArchiveList ul li {background: none;list-style: none;list-style-image: none;list-style-position: outside;border-width: 0;padding-left: 15px;text-indent: -15px;margin: .25em 0;background-image: none;}
.BlogArchive #ArchiveList ul ul li {padding-left: 1.2em;}
.article-more {overflow: hidden;}
.BlogArchive #ArchiveList ul {margin: 0;padding: 0;list-style: none;list-style-image: none;border-width: 0;}
.BlogArchive #ArchiveList ul.posts li {padding-left: 1.3em;}
#ArchiveList .collapsed ul {display: none;}
.postwrapper-artikel {background-color: #fff;-webkit-backdrop-filter: saturate(180%) blur(20px);backdrop-filter: saturate(180%) blur(20px);padding: 15px;max-width: 500px;margin: 0 auto;border-radius:0 0 10px 10px;color: #333;box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);overflow: hidden;margin-top: -7px;}
.postwrapper-artikel h2, .postwrapper-artikel h3, .postwrapper-artikel h4, .postwrapper-artikel h5 {margin: 15px 0;}
/* Post Feat */
.firstimage-- img {
width: 530px;border-radius:5px;}
.firstimage-- {box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);margin-bottom: 10px;border-radius: 10px 10px 0 0;}
.maxwidht-- {max-width: 530px;margin: 0 auto;}
.dlbtn svg path {fill: #444;}
.dlbtn-- {text-align: center;margin: 0 auto;align-items: center;padding-top: 10px;}
.dlbtn-- a {box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);border-radius: 10px;text-align: center;margin: 0 auto;color: #fff;padding: 10px;background: #43ce8e;align-items: center;}
.dlbtn-- svg {margin: -6px 1px;}
.label-post-- {margin: 5px 0;}
.label-post-- a {color: #555;background: #eee;padding: 3px;border: 1px solid #ddd;border-radius: 5px;text-transform: capitalize;font-size: 14px;}

/* Status Msg */
.status-msg-wrap {font-size: 110%;margin: 20px 10px;position: relative;text-align: center;}
.status-msg-border {display: none;}
.status-msg-bg {background-color: transparent;opacity: .8;filter: alpha(opacity=30);-moz-opacity: .8;width: 100%;position: relative;z-index: 1;}
.status-msg-body {padding: 15px;z-index: 4;border-radius: 5px;border: 1px solid #eee;}
.status-msg-hidden {visibility: hidden;padding: .3em 0;}
.status-msg-wrap a {padding-left: .4em;}

/* FOOTER WIDGET */
#widget-footer-container {    background: linear-gradient(-45deg, #EE7752, #E73C7E, #23A6D5, #23D5AB);background-size: 400% 400%;-webkit-animation: Gradient 15s ease infinite;-moz-animation: Gradient 15s ease infinite;animation: Gradient 15s ease infinite;padding: 0 30px;overflow: hidden;line-height: 1.6em;}
#widget-footer-wrapper {margin: 0 auto;max-width: 900px;color: $(widget.color);}
#widget-footer-wrapper .widget {margin: 30px 0;}
#widget-footer-wrapper .widget a {color: #444444;}
#widget-footer-wrapper .widget a:hover {color: $(widget.hover.color);}
#widget-footer-wrapper .widget ul, #widget-footer-wrapper .widget ol {list-style: none;margin: 0 0;}
#widget-footer-wrapper .widget ul li, #widget-footer-wrapper .widget ol li {font-weight: 500;margin: 0.3em 0;}
#widget-footer-wrapper h2 {font-size: 16px;color: #fff;font-weight: 600;text-align: center;text-transform: uppercase;margin-bottom: 20px;}
#widget-footer {width: 100%;float: left;}
.popular-posts {columns: 14rem;gap: 1rem;}
/* FOOTER */
#footer-container {background: $(footer.background.color);padding: 20px 30px;overflow: hidden;color: $(footer.color);font-size: 13px;text-align: center;}
#footer-wrapper {max-width: 900px;margin: 0 auto;overflow: hidden;}
#footer-wrapper .footer-right {float: right;}
#footer-wrapper .footer-left {float: left;}
#footer-wrapper a {color: $(footer.link.color);}
#footer-wrapper a:hover {color: $(footer.hover.color);}

/* MEDIA QUERY */
@media only screen and (max-width:1080px){
	#wrapper {
		margin: 0 auto;
	}
	#header-wrapper {
		padding-left: 30px;
		padding-right: 30px;
	}
}
@media only screen and (max-width:800px){
.breadcrumbs-outer{
margin: 20px 0 30px 0;

}
	#header-wrapper {
		padding-left: 0px;
		padding-right: 0px;
		position: relative;
	}
	#widget-footer-container {
		padding: 0 20px;
	}
	#widget-footer1 {
		width: 100%;
		float: none;
		padding-right: 0;
	}
	#footer-container {
		padding: 20px 20px;
	}
	#cssmenu > ul > li > a {
		padding: 0 15px;
	}
	.button {
		margin-right: 20px;
	}
}


@media only screen and (max-width:480px){
	#widget-footer-container {
		padding: 0 15px;
	}
	.post-body a > img {
		width: 100%;
	}
	h1{font-size:170%
	}
	h2{font-size:150%
	}
	h3{font-size:130%
	}
	h4{font-size:120%
	}
	h5{font-size:110%
	}
	h6{font-size:100%
	}
	.comments .comments-content .comment-replies{
		margin-left:20px !important;
	}
	.comments .comment-block {
		padding: 15px !important;
	}
	.comment .comment-thread.inline-thread .comment {
		margin: 0 0 0 0 !important;
	}
	iframe#comment-editor {
		min-height: 270px;
	}
	h1.post-title {
		font-size: 22px;
		padding: 0;
	}
}
/* Infinite Scroll Navigation */
#blog-pager a.home-link {display:none}
#blog-pager {padding:0;margin:20px auto; text-align:center;}
#blog-pager-older-link {float:none; display:block}
#blog-pager-older-link img {max-height:50px}
#blog-pager-older-link a {background:#fff; color:#555; font-size:14px; font-weight:600; border-radius:3px; padding:10px 20px; display:inline-block; position:relative; transition:0.3s;background: #eee;}
/*--- navheader ---*/
.check {display:none;}
.Navigationbottom label {cursor:pointer;display:block;padding:8px;background-position:center;transition:all .5s linear;position: fixed;top: 17px;right: 10px;}
.Navigationbottom .check:checked ~ .NavMenu {opacity:1;visibility:visible;right: 35px;transition:all .3s ease;z-index:2;}
.Navigationbottom .NavMenu {opacity:0;visibility:hidden;position:absolute;right:0;top:-40px;background-color:#fff;color:#3c4043;
transition:all .3s ease;}
.Navigationbottom .check:checked ~ .icon .open {display:none;}
.Navigationbottom .icon .open {display:block;}
.Navigationbottom {position:absolute;right:50px;bottom:27px;}
.Navigationbottom .icon .close {display:none;}
.Navigationbottom .check:checked ~ .icon .close {display:block;}
.Navigationbottom .NavMenu ul {margin:0;padding:0;}
.Navigationbottom .NavMenu:before,.Navigationbottom .NavMenu:after {content:'';top:-5px;right:11px;border-color:transparent;border-bottom-color:#fff;border-style:dashed dashed solid;border-width:8.5px 0px 8.5px 8.5px;position:absolute;z-index:1;height:0;width:0;}
.Navigationbottom .NavMenu ul li.xprofil {background-color:#e6e6e6;display:-webkit-box;display:-webkit-flex;display:-moz-box;display:-ms-flexbox;display:flex;margin:0;align-items:center;padding:10px 16px;border-bottom:1px solid #fff;}
.Navigationbottom .NavMenu ul li {list-style-type:none;transition:all .3s ease;margin:0;}
.Navigationbottom .NavMenu img {max-width:50px;max-height:50px;border-radius:100px;border:1px solid #fff;margin:0;}
.Navigationbottom .NavMenu ul li.xprofil ul {line-height:24px;margin-left:3px;}
.Navigationbottom .NavMenu ul li.xprofil ul li.name {font-weight:700;font-size:17px;margin-bottom:5px;}
.Navigationbottom .NavMenu ul li.xprofil ul li {padding:0;font-size:17px;line-height:normal;white-space:nowrap;}
.Navigationbottom .NavMenu ul li.xprofil ul li.follow a {background-color:#4285F4;color:#fff;font-size:10px;padding:3px 7px;border-radius:25px;display:inline-block;}
.Navigationbottom .NavMenu ul li a {color:#3c4043;display:block;padding:10px 16px;margin:0;}
.Navigationbottom .NavMenu ul li a span {font-size:14px;}
.Navigationbottom .NavMenu ul li.xprofil ul li.follow a:before {content:'';display:inline-block;width:15px;height:15px;margin-right:3px;margin-left:-3px;vertical-align:-4px;background:url("data:image/svg+xml,%3Csvg viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M12,20C7.59,20 4,16.41 4,12C4,7.59 7.59,4 12,4C16.41,4 20,7.59 20,12C20,16.41 16.41,20 12,20M12,2A10,10 0 0,0 2,12A10,10 0 0,0 12,22A10,10 0 0,0 22,12A10,10 0 0,0 12,2M13,7H11V11H7V13H11V17H13V13H17V11H13V7Z' fill='%23fff'/%3E%3C/svg%3E") center no-repeat;}
.Navigationbottom .NavMenu ul li:hover {background:#e6e6e6;}
.Navigationbottom .NavMenu ul li.social {background-color:#fff;display:-webkit-box;display:-webkit-flex;display:-moz-box;display:-ms-flexbox;display:flex;justify-content:space-between;padding:0 15px;border-top:1px solid #fff;}
.Navigationbottom .NavMenu ul li.social a {padding:15px 7px;z-index:1;position:relative;}
.Navigationbottom .NavMenu ul li.social button {margin:0;font-size:unset;}
.Navigationbottom label:hover {border-radius:100px;background:rgba(253, 253, 253, 0.2) radial-gradient(circle,transparent 2%,rgba(255, 1, 1, 0.2) 2%) center/15000%;}
.Navigationbottom label:active {border-radius:100px;background-color:rgba(0,0,0,.1);background-size:100%;transition:background 0s;}
.Navigationbottom .NavMenu ul li.xprofil ul li.follow a:hover {
background-color:#ff9800;}
.Navigationbottom .NavMenu ul li.social a:hover:before {content:'';position:absolute;z-index:-1;margin:auto;background:rgba(0,0,0,.1);border-radius:100px;width:36px;height:36px;top:0;bottom:0;left:0;right:0;transition:opacity .3s linear;}
@media only screen and (max-width:480px) {
.Navigationbottom .NavMenu ul li a, .Navigationbottom .NavMenu ul li.xprofil {
padding: 8px 13px;}}
.nav-menu2{background-color:#eee;list-style:none;margin:0;width:100%;float:left;padding:0;border-top: solid 1px #E0E0E0;}
.nav-menu2:before,.nav-menu2:after{content:" ";display:table}
.nav-menu2:after{clear:both}.sub-menu{transition:all .5s ease-in-out}
.nav-menu2 ul{list-style:none;margin:0;width:auto}
.nav-menu2 a{display:block;padding:0 15px}
.nav-menu2 li{position:relative;margin:0}
.nav-menu2 > li {background: #fff;}
.nav-menu2 > li > a {text-transform: uppercase;display: block;line-height: 48px;color: #444;font-weight: 600;white-space: nowrap;overflow: hidden;text-overflow: ellipsis;}
.nav-menu2 > li:hover > a{background:rgb(238 238 238 / 52%)}
.nav-menu2 li ul{background:#fff;display:none;-webkit-transition:all .25s ease-out;-moz-transition:all .25s ease-out;-ms-transition:all .25s ease-out;-o-transition:all .25s ease-out;transition:all .25s ease-out;padding:0}
.nav-menu2 li li ul{left:100%;top:-1px}
.nav-menu2 li li a.click ul{visibility:visible;opacity:10}
.nav-menu2 li li a{display:block;color:#666;position:relative;line-height:40px}
.nav-menu2 li li a:hover{background:#f0f0f0}
.nav-menu2 li li li a{background:#fff;z-index:20;color:#333}
.nav-menu2 li .dropdown:after{content:"\f105";font-family:FontAwesome;font-style:normal;font-weight:400;text-decoration:inherit;position:absolute;top:0;right:20px;color:#444}
.nav-menu2 li .dropdown.open:after{content:"\f107";font-family:FontAwesome;font-style:normal;font-weight:400;text-decoration:inherit}
.nav-menu2 li .dropdown:hover:after{color:#000}
.nav-menu2 li i{font-size:18px;width:35px}.nav li a.click{opacity:1}
.nav-menu2 h2{font-size:14px;font-weight:normal!important;padding:0 20px;margin:0;overflow:hidden;border-top:1px solid #ddd;color:#999;display: none;}
.nav-menu2 p{font-size:13px}
.media-left {z-index: 9;float: left;display: flex;width: 100%;margin-top: -10px;}
.media-left .image img {width: 20px;height: 20px;border-radius: 100%;max-width: inherit;}
.is-4 {font-size: 11px;line-height: 20px;margin: 0 5px;color: #000;width: 100%;}
.dlbtn {margin-top: 1px;margin-left: 5px;}
.item-thumbnail-only .img-thumbnail-popular {border-radius: 10px;box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);}
.img-thumbnail-popular {position: relative;height: auto;transition: transform .2s;overflow: hidden;}
.hidden,.noness {display:none;}
.menubottom{display:none}
@media screen and (max-width:800px){.menubottom{position:relative/*fixed*/;right:0;left:0;z-index:5;bottom:0}.menubottom nav ul{display:flex!important;width:100%!important;padding-left:0;justify-content:space-between!important;margin-bottom:0;flex-direction:row!important;list-style:none}.menubottom nav ul li{width:100%!important;list-style:none;}.menubottom nav ul li a{display:block;text-decoration:none;padding:.4rem 1rem}.menubottom nav ul li a svg{width:25px;height:25px;fill:#444;}.menubottom nav ul li a span{color:#4b4f56;position:relative;font-size:8px;display:block;top:0}#openShare{display:block}#closeShare{display:none}#jpthemeFooter{padding-bottom:55px;position:relative;}}
@media screen and (max-width:768px){.menurekom .buka-tutup {display: none;}.menubottom{left:0;text-align:center;width:100%;position:fixed;display:block}
.menubottom nav {background-color: rgb(255,255,255);display: block!important;position: relative;display: flex;flex-wrap: wrap;align-items: center;justify-content: space-between;box-shadow: 0 2px 3px 2px rgba(0,0,0,0.1);background: #fff;text-align: center;font-weight: bold;border-radius: 10px 10px 0 0;text-decoration: none;transition: ease all 0.3s;}
.menubottom ul li{top: 0;float:left;width:100px;height:100%;transition:transition:all .5s linear;background-position:center;display:block;position: relative;right: 0;font-size: inherit;margin: auto;}
.float_wrapper_menubottom{position:fixed;left:0;bottom:0;right:0;transition:all .3s ease-out;-webkit-transform:translateZ(0);transform:translateZ(0);font-family: &#39;Quicksand&#39;, -apple-system, BlinkMacSystemFont, &#39;Segoe UI&#39;, &#39;Oxygen-Sans&#39;, &#39;Helvetica Neue&#39;, Arial, sans-serif;}}
.menubottom.scroll-1 {bottom: -90px;}
.menubottom.scroll-bottom {bottom: 0;}
.menubottom {transition: bottom 0.2s ease-in-out;}
.head-pop:before {content: '';display: block;position: absolute;z-index: -1;width: 100px;height: 100px;border-radius: 2000px;background: rgb(71 195 251 / 45%);left: -35px;top: -30px;}
.pop-area{display:flex!important;width:100%;height:100%;position:fixed;top:0;left:0;background:rgb(0 0 0 / 51%);visibility:hidden;opacity:0;transition:all 0.25s ease-in-out;z-index:999999;overflow-y:scroll}
.pop-area.open{opacity:1;visibility:visible}
.pop-html{background:#fff;padding-bottom:10px;display:block;margin:auto;margin-top:10px;width:calc(100% - 20px);max-width:500px;visibility:hidden;opacity:0;overflow:hidden;transition:all 0.5s ease-in-out;transform:scale(.5);border-radius:7px;box-shadow:0 9px 46px 8px rgba(0,0,0,.14),0 11px 15px -7px rgba(0,0,0,.12),0 24px 38px 3px rgba(0,0,0,.2)}
.pop-area.open .pop-html{opacity:1;transform:scale(1);visibility:visible}
.head-pop {width: -webkit-fill-available;padding: 10px;overflow: hidden;display: flex;}
.head-pop span {font-weight: 600;width: 100%;margin: 3px 5px;}
.close-btn{float:right;cursor:pointer;fill:#7e7e7e}
.table-bookmark {padding: 10px;}
.text-center{display:grid;text-align:center;grid-gap:15px}
.text-center svg{margin:0 auto}
.btn.btn-outline-info{width:fit-content;margin:0 auto;text-decoration:none}
.table {width: 100%;border-radius: 7px;padding: 5px;break-inside: avoid;}
.table img {border-radius: 7px;width: auto;box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);}
.table a {text-decoration: none;color: #333;font-size: 12px;width: 100%;display: -webkit-box;-webkit-box-orient: vertical;text-overflow: ellipsis;overflow: hidden;-webkit-line-clamp: 2;}
.img-left{width:100%;display: flex;}
.item-left {float: left;width: 100%;padding: 10px 0;margin-bottom: 10px;}
td.item-remove {position: absolute;margin-top: -35px;margin-left: 5px;}
.btn-remove svg {padding: 5px;border-radius: 100px;box-shadow: 0 0px 5px 2px rgba(0,0,0,0.10);background: #0000003d;}
.btn-remove{cursor:pointer}
.show-bookmark{color:#fff;background-color:#007bff;position:relative;top:-20px;right:10px;font-size:50%;padding:.15em .3em;display:inline-block;padding:.25em .4em;font-size:75%;font-weight:700;line-height:1;text-align:center;white-space:nowrap;vertical-align:baseline;border-radius:50%;transition:color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out}
.hartomy-bookmark-btn, .btn-outline-info {position: relative;display: inline-block;box-sizing: border-box;border: none;outline: none;cursor: pointer;transition: box-shadow 0.2s;background: none;}
.hartomy-bookmark-btn::-moz-focus-inner{border:none}
.hartomy-bookmark-btn svg{vertical-align:middle}
.buka-tutup.menubookmark {margin: 0;cursor: pointer;fill: #333;}
.lang-iklanpost .widget-content {margin: 30px 0;}
.ads-here {background: radial-gradient(transparent, #c2afb1);display: flex;align-items: center;justify-content: center;padding: 20px 0;border: 1px solid #ebeced;border-radius: 3px;color: #767676;font-size: 12px;}
.ads-here:before {content: 'IKLAN DISINI!';}
.menubtm {height: 55px;display: block;transition: top .3s ease;bottom: 0;left: 0;padding: 10px;position: relative;z-index: 99;width: -webkit-fill-available;border-radius: 10px 10px 0 0;margin: -15px -15px 15px -15px;}
.btnlook{background:#f1f1f1;display:block;text-align:center;font-weight:700;-webkit-border-radius:10px;padding:10px;transition:ease all .3s;float:left;margin-top:8px;margin-right:10px}
.btndwnld{background:#d11313;display:block;text-align:center;font-weight:700;-webkit-border-radius:10px;transition:ease all .3s;float:left;padding:10px;margin-top:8px}
.title-image-popular {background: linear-gradient(transparent,rgba(0, 0, 0, 0.8));position: absolute;left: 0;right: 0;bottom: 0;padding-top: 30px;}
.title-image {display: flex;margin: 10px 0;}
.title-image-popular h3 {overflow: hidden;line-height: 35px;margin: 0 10px!important;color: #ffffff;font-size: 12px;white-space: nowrap;text-overflow: ellipsis;}
.title-image h1 {color: #333;font-size: 12px;width: 100%;display: -webkit-box;-webkit-box-orient: vertical;text-overflow: ellipsis;overflow: hidden;-webkit-line-clamp: 2;}
.title-image-popular h3 a {color: #ffffff!important;}
.postwrapper-artikel .title-wrapper h1 {text-align: center;margin: 0;}
.bckbtn {box-shadow: 0 0px 5px 2px rgba(0,0,0,0.10);background:#0000003d;display: block;width: 40px;height: 40px;line-height: 40px;text-align: center;color: white;font-size: 35px;font-weight: bold;border-radius: 50px;-webkit-border-radius: 50px;text-decoration: none;transition: ease all 0.3s;position: fixed;left: 15px;top:70px;z-index: 9;}
.bckbtn:hover{background: black}
.lock, .locked{overflow:hidden!important}
#cookieChoiceInfo{background-color:#222;padding:10px 10px 40px;top:unset;font-family:"Helvetica Neue Light",HelveticaNeue-Light,"Helvetica Neue",Calibri,Helvetica,Arial;width:300px;left:10px;bottom:10px;border-radius:5px;overflow:hidden}
#cookieChoiceInfo .cookie-choices-text{margin:0 0 5px;font-size:16px;color:#fff;text-align:left;}
#cookieChoiceInfo .cookie-choices-inner{position:static}
#cookieChoiceInfo .cookie-choices-buttons{margin:0;display:block}
#cookieChoiceInfo .cookie-choices-button{color:#f1d600;text-transform:none;transition:all .2s linear;font-weight:400;display:block;text-align:left;margin:0 0 10px;padding:0}
#cookieChoiceInfo .cookie-choices-button:nth-child(2){color:#000;text-align:center;background-color:#f1d600;padding:8px 18px;position:absolute;bottom:0;left:0;right:0;margin:0}
#cookieChoiceInfo .cookie-choices-button:hover{color:#e9eef0}
#cookieChoiceInfo .cookie-choices-button:nth-child(2):hover{background-color:#e9eef0;color:#000}
@media only screen and (max-width:640px){#BlogSearch1 {position: absolute;left: 55px;}}
@media screen and (max-width:425px){#cookieChoiceInfo{width:calc(100% - 20px)}}
.FollowByEmail {position: relative;border-radius: 10px;background: #ffffff;padding: 20px;}
.FollowByEmail .widget-content{position:relative;z-index:2}
.FollowByEmail h3 {color: #393939;text-align: center;}
.FollowByEmail .follow-text{display:block;margin-bottom:15px;font-size:13px;color:#989b9f}
.FollowByEmail form{display:flex;display:-webkit-flex;justify-content:space-between;-webkit-justify-content:space-between;}
.FollowByEmail input[type=email]{display:block;width:100%;padding:11px 18px;outline:0;border:1px solid #ebeced;border-radius:7px;font-size:13px;box-shadow:none;-webkit-transition:all .25s ease-in-out;transition:all .25s ease-in-out;background-color:#f7f7fc}
.FollowByEmail input[type=email]:focus, .ContactForm input[type=text]:focus, .ContactForm textarea:focus{box-shadow:0 2px 4px 0 rgba(9,32,76,.05);}
.FollowByEmail input[type=submit], .ContactForm input[type=button]{display:none;width:100%;margin-top:12px;padding:12px 18px;border:0;font-size:13px;border-radius:7px;color:#fff;cursor:pointer;}
.FollowByEmail label.email-label {border-radius: 7px;padding: 8.5px 0;display: inline-block;width: 30px;height: 30px;text-align: center;position: absolute;right: 5px;top: -4px;}
.FollowByEmail label.email-label svg {fill: #333;background: #f7f7fc;border-radius: 5px;}
#BlogSearch1 {float: right;margin-top: 12px;margin-right: 60px;}
.bg_Se {line-height: 30px;position: relative;}
form.gb_Se {display: inline-block;position: relative;width: 100%;background-color: white;border: 1px solid rgb(230, 236, 240);-webkit-border-radius: 4px;border-radius: 5px;min-width: 100px;}
button.Se {width: 40px;border: 0;background: transparent;cursor: pointer;position: absolute;top: 0;line-height: 32px;outline: none;}
.bg_Se button svg {vertical-align: -7px;height: 22px;width: 22px;min-width: 22px;}
.bg_Se input {background: transparent;font-family: Roboto,Arial,sans-serif;font-size: 15px;line-height: 30px;padding-left: 35px;width: 65%;color: #3c4043;border: 0;outline: none;}
#Header1 {float: left;margin-left: 45px;width: 150px;overflow: hidden;height: 50px;}
#Header1 img {width: 100px;}	
.blog-posts {padding: 10px;}
.menurekom {width: 100%;z-index: 9999;background: transparent;position: fixed;transition: all .3s ease;top: 0;padding-bottom: 15px;margin: auto;height: 40px;overflow: hidden}
.menurekom .header-inner {padding: 10px;text-align: center;line-height: 35px;}
.menurekom .header-inner h1 {color: #333;font-weight: 500;}
.menurekom.scrolled {background: #fff;}
#search-box{margin: 0 auto;animation:fadeInDown 1s;width:100%;/*height:35px*/;float:none;padding:0;/*margin:0 0 -55px*/;position:relative;padding-top: 80px;}#search-box form{border:0px solid #4a86e8;line-height:35px;padding: 10px 10px 0 10px;}.search-form{text-transform: capitalize;border:none;color:#9E9E9E;width:100%;height:45px;line-height:35px;font-size:14px;font-weight:400;margin:0;-moz-box-sizing:border-box;box-sizing:border-box;padding: 10px 20px 10px 20px;border-radius: 100px;    box-shadow: 0 2px 2px 0 rgba(0,0,0,0.11), 0 0 0 1px rgba(0, 0, 0, 0.05);transition: box-shadow 200ms cubic-bezier(0.4, 0.0, 0.2, 1);background: #fff url() no-repeat 50px 13px !important;background-size: 100px!important;}.search-button{background:0 0;width:30px;height:38px;line-height:39px;padding:0;text-align:center;margin:0;top:0;right:0;font-size:16px;color:#333333e3;position:absolute;border:none;border-radius:0;cursor:text}.search-form:focus{border:none;outline:0;background: #fff!important;color:#9E9E9E;box-shadow: 0 3px 8px 0 rgba(0,0,0,0.2), 0 0 0 1px rgba(0,0,0,0.08);}
.menurekom .header-inner h1 a {color: #333;}
.dropdowns {-webkit-transition: all 500ms cubic-bezier(0.165, 0.84, 0.44, 1);-moz-transition: all 500ms cubic-bezier(0.165, 0.84, 0.44, 1);-o-transition: all 500ms cubic-bezier(0.165, 0.84, 0.44, 1);transition: all 500ms cubic-bezier(0.165, 0.84, 0.44, 1);-webkit-transition-timing-function: cubic-bezier(0.165, 0.84, 0.44, 1);-moz-transition-timing-function: cubic-bezier(0.165, 0.84, 0.44, 1);-o-transition-timing-function: cubic-bezier(0.165, 0.84, 0.44, 1);transition-timing-function: cubic-bezier(0.165, 0.84, 0.44, 1);}
.scroll{top:-90px}
.no-scroll{top:0;z-index:99}
.dropdowns {min-width: 200px;width: 60%;max-width: 251px;font: normal normal 14px Roboto,Arial,sans-serif;background: #fff;margin-top: 60px;overflow: auto;overflow-x: hidden;position: fixed;z-index: 10000;bottom: 0;left: -400px;line-height:48px;box-shadow: 0 5px 5px 0 rgba(0,0,0,0.16), 0 2px 10px 0 rgba(0,0,0,0.12);top: -60px;}
.dropdowns h3,.dropdowns p{padding:0;margin:0;font-weight:400!important}
.dropdowns h3 {text-align: center;font-size: 20px;text-transform: uppercase;}
.dropdowns img{width:70px;height:70px;}
#nav-menu1{visibility:hidden;position:absolute;background:#a4c639;list-style:none;right:30px;top:15px;padding:0;width:0;height:0;transition:all .5s cubic-bezier(0.07, 0.68, 0.35, 1.04);z-index:9;overflow:hidden;box-shadow:0 5px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12)}
#nav-menu1 li{width:100%}
#nav-menu1 li a{padding:8px 15px;width:100%;font-weight:400;color:#eee;text-overflow: ellipsis;overflow: hidden;white-space: nowrap;}
#nav-menu1.shows{visibility:visible;width:90px;height:auto}
.dropdowns.shows{left:0;opacity:1}
.darkshadow{visibility:hidden;opacity:0;position:fixed;top:0;background:rgba(0, 0, 0, 0.59);left:0;right:0;bottom:0;margin:0;z-index:10000;transition:all .4s ease-in-out}
.darkshadow.shows{visibility:visible;opacity:1}
.menu-btn {padding: 13px 0;width: 45px;position: relative;cursor: pointer;}
.menu-btn-close .bar_1 {-webkit-transform: translateY(8px) rotate(-45deg);-ms-transform: translateY(8px) rotate(-45deg);transform: translateY(8px) rotate(-45deg);background-color: #555;}
.menu-btn .bar_1 {margin-top: 0;}
.menu-btn-close .bar_2 {opacity: 0;}
.menu-btn-close .bar_3 {-webkit-transform: translateY(-8px) rotate(45deg);-ms-transform: translateY(-8px) rotate(45deg);transform: translateY(-8px) rotate(45deg);background-color: #555;}
.menu-btn .bar_3 {margin-bottom: 0;}
.menu-btn .bar_1, .menu-btn .bar_2, .menu-btn .bar_3 {position: relative;display: block;width: 21px;height: 3px;margin: 5px auto;background-color: #555;border-radius: 10px;}
.penjudul {text-align: center;font-size: 20px;text-transform: uppercase;}
.ikonme {font-size: 20px;color: gray;cursor: pointer;fill : #333;}
.menu-icons {position: absolute;float: left;margin: 0;top: 15px;left: 20px;font-size: 20px;}
.buka-tutup {position: absolute;float: left;margin: 0;top: 8px;right: 10px;font-size: 20px;}
.dropdowns.shows{left:0;opacity:1}
.darkshadow{visibility:hidden;opacity:0;position:fixed;top:0;background:rgba(0, 0, 0, 0.59);left:0;right:0;bottom:0;margin:0;z-index:10000;transition:all .4s ease-in-out}
.darkshadow.shows{visibility:visible;opacity:1}
#page {width: 100%;display: block;background-position: center;margin: auto;position: relative;background: #eee}
.lazyloaded {opacity: 1;-webkit-transition: opacity .5s cubic-bezier(0, 0.76, 0.44, 0.95);-moz-transition: opacity .5s cubic-bezier(0, 0.76, 0.44, 0.95);-o-transition: opacity .5s cubic-bezier(0, 0.76, 0.44, 0.95);transition: opacity .5s cubic-bezier(0, 0.76, 0.44, 0.95);will-change: opacity;}
.left-btn {float: left;}
.right-btn {float: right;}
button#left-button,button#right-button {cursor: pointer;outline: none;border: none;width: 35px;height: 43px;background: transparent;}
.jwpopup-head {font-size: 11px;padding: 0px 5px;color: #161617;margin: 10px;}
.jwpopup {display: none;z-index: 9999999999;background-color: rgba(11,14,18,.8);position: fixed;width: 100%;max-height: 100%;transition: all .1s linear;margin: 0 auto;height: 100%;top: 0;}
.jwpopup-content {background-color: #fefefe;margin: auto;padding: 0;-webkit-animation-name: animatetop;-webkit-animation-duration: 0.4s;animation-name: animatetop;animation-duration: 0.4s;width: 100%;max-width: 500px;border-radius: 10px;}
.jwpopup-head h2 {white-space: nowrap;text-overflow: ellipsis;overflow: hidden;font-weight: 500;font-size: 15px;padding: 0 40px 0 0;}
a.closee {color: #fff;font-weight: 400;text-transform: uppercase;padding: 10px;margin-top: -50px;float: right;margin-right: -15px;}
.wp-jwpopup {display: flex;width: 100%;text-align: center;}
.wp-jwpopup span {text-align: center;margin: auto;}
#wp-btn {border: 1px solid #ddd;margin: auto;
}
.iklan-download {padding: 10px;}
@-webkit-keyframes animatetop {from {top:-300px; opacity:0}to {top:0; opacity:1}}
@keyframes animatetop {from {top:-300px; opacity:0}to {top:0; opacity:1}}
.navDark i{display:flex;align-items:center; width:26px;height:18px; border-radius:10px;border:1px solid #000; opacity:.8}
.navDark i:before{content:'';display:block;position:relative;left:3px; width:10px;height:10px; border-radius:50%;background-color:#000;transition: all .1s ease);}
.navDark:before {content: attr(data-text);opacity: 0;transition: all .2s ease;white-space: nowrap;position: absolute;left: 0;}
.navDark {position: absolute;float: left;margin: 0;top: 18px;right: 65px;font-size: 20px;}
.darkMode .navDark i:before {left: 10px;background-color: #fefefe;}
.darkMode #page, .darkMode .penjudul, .darkMode .pop-html, .darkMode .menubottom nav {background:#18191a;}
.darkMode #page .menurekom.scrolled, .darkMode #page .labelbottom.scrolled, .darkMode .nav-menu2, .darkMode .jwpopup-content {background: #242526;}
.darkMode .menurekom .header-inner h1, .darkMode .label-bawah-menu a,.darkMode, .darkMode .title-image h1, .darkMode .is-4, .darkMode .menurekom .header-inner h1 a, .darkMode .nav-menu2 > li > a, .darkMode .table a, .darkMode #widget-footer-wrapper h2, .darkMode h1.post-title, .darkMode .wp-jwpopup span, .darkMode .jwpopup-head h2, .darkMode .menubottom nav ul li a span, .darkMode .breadcrumbs a {color:#fefefe}
.darkMode .ikonme, .darkMode .buka-tutup.menubookmark, .darkMode #left-button svg path, .darkMode #right-button svg path, .darkMode .bg_Se button svg, .darkMode .massgEmpty svg, .darkMode .Navigationbottom .icon .open path, .darkMode .menubottom nav ul li a svg, .darkMode .searchbtn svg, .darkMode .close-searchbtn svg{fill: #fefefe;}
.darkMode .label-bawah-menu a, .darkMode .gb_Se {background:#333}
.darkMode .gb_Se {border: 1px solid rgb(51 51 51);}
.darkMode, .darkMode #wrapper{background-color: #2c2c2c;}
.darkMode .nav-menu2 {border-top: 1px solid rgb(51 51 51);}
.darkMode .nav-menu2 > li {background: #121212;}
.darkMode #blog-pager-older-link a {background: #525252;color: #fff;}
.darkMode .postwrapper-artikel {background-color: rgb(7 7 7 / 66%);color: #fefefe;}
.darkMode .navDark i, .darkMode .navMenu .ham i, .darkMode .navMenu .ham span:before, .darkMode .navMenu .ham span:after{border-color: #fefefe;}

.bagikan{width: 100%;border:0!important;margin-right: 20px;margin-top: 0;text-align: center;}
.bagikan a,.bagikan span{font-size:90%}.bagikan a{font-weight:400;border-radius:3px}.bagikan a,.bagikan img{transition:all .1s ease}.bagikan{display:block;margin:10px 0 10px;border:1px solid #ddd}.bagikan img{border-radius:3px}.bagikan img:hover{opacity:.6}.bagikan a{display:inline-block;background:#8d8d8d;padding:2px 10px 2px 10px!important;font-size: 70%;color:#fefefe;border-radius: 5px;box-shadow: 0 2px 2px 0 rgba(0,0,0,0.16), 0 0 0 1px rgba(0,0,0,0.08);transition: box-shadow 200ms cubic-bezier(0.4, 0.0, 0.2, 1);text-shadow:0 -1px 2px rgba(0,0,0,.14)}.bagikan a.fb{background:#4d68a1}.bagikan a.twitter{background:#39aee7}.bagikan a.gplus{background:#f65543}.bagikan a.email{background:#fd9f4e}.bagikan span{display:block}.bagikan a{text-align:center;margin:0 2px;font-size: 80%;padding:5px 10px 5px 10px!important}.bagikan a.line,.bagikan a.whatsapp{display:inline-block!important}.bagikan a.whatsapp{background:#009688}.bagikan a.line{background:#00c300}.bagikan a.fb{background:#4d68a1}.bagikan a.twitter{background:#39aee7}.bagikan a.gplus{background:#f65543}.bagikan a.email{display:none}
.bagikan a svg {height: 20px;width: 20px;vertical-align: middle;fill: #fff;}a.pinterest {background: #d11313;}
.iklan-pop {width: 100%;}
@media screen and (max-width:768px){.navDark {right: 20px;}}
.live-wp {width: 100%;border-radius: 10px 10px 0 0;}
.PyenC .Live:before {content: 'Live';z-index: 1;color: #fff;position: absolute;top: 0;background: #333;padding: 5px;border-radius: 5px;font-size: 11px;margin: 5px;text-transform: uppercase;}
.PyenC .Video:before {content: 'Video';z-index: 1;color: #fff;position: absolute;top: 0;background: #333;padding: 5px;border-radius: 5px;font-size: 11px;margin: 5px;text-transform: uppercase;}
.iklantext {background: #eee;min-height: 70px;display: flex;align-items: center;justify-content: center;font-size: 13px;border: 1px solid #ddd;border-radius: 3px;}
.iklantext:before {content: 'ADS';font-weight: bold;}
.searchbtn,.close-searchbtn{display:none;}
@media screen and (max-width:768px){.navDark {right: 20px;}#BlogSearch1 {display: none;}.searchbtn {display: block;float: right;margin: 0;margin-right: 55px;font-size: 20px;margin-top: 20px;}.close-searchbtn {display: block;position: absolute;float: left;margin: 0;top: 3px;right: 5px;}}
.menubtm .js-share {float: right;margin: 15px 0;}
.darkMode .js-share svg {fill: #fff!important;}
.darkMode svg {fill: #fff;}
#HTML5 {padding: 0 15px;margin: 20px 0;}
#HTML4 {padding: 0 15px;margin-top: -15px;margin-bottom: 15px;}
.darkMode .iklantext {background: #333;border: 1px solid #444;}
#Label3 .nav-menu2 > li > a svg {width: 20px;height: 20px;vertical-align: middle;margin: 0 5px 3px 0;fill: #444;}
.darkMode #Label3 .nav-menu2 > li > a svg {fill: #fff;}
@-webkit-keyframes Gradient{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}}@-moz-keyframes Gradient{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}}@keyframes Gradient{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}}
.post-dates {text-align: center;font-size: 12px;}
.post-dates abbr {border: none!important;text-decoration: none;text-align: center;}
]]></b:skin>
<b:if cond='data:blog.pageType == &quot;index&quot;'>
<style>
.blog-posts {display: block;columns: 14rem;gap: 1rem;}
.post-outer {break-inside: avoid}
.post-outer .post {margin-bottom: 1rem;}
.post {position: relative;}
.post-snippet {font-weight: normal;display: none;}
@media only screen and (max-width:480px){
.blog-posts,.popular-posts {columns: 8rem;}}
</style>
<b:else/>
<style>
@media only screen and (max-width:480px){.popular-posts {columns: 8rem;}}
#wrapper{padding-top:70px!important;}
.blog-posts {padding:0px!important}
.post-body .separator:nth-of-type(1){clear:both;display:none}
.post-body&gt;.separator:nth-child(1){display:none}
.post-label- {text-align: center;margin: 15px 0;white-space: nowrap;overflow-x: auto;overflow-y: hidden;}
a.post-label-- {margin: 0 3px;background: rgba(0, 0, 0, 0.59);padding: 5px;border-radius:5px;box-shadow: 0 2px 5px 0 rgba(0,0,0,0.1);color: #fff;}
#widget-footer-container {margin-bottom: 70px;}
</style>
</b:if>
<b:if cond='data:view.isPage'>
  <style>
    .post-outer {
    padding: 20px;
}
</style>
  </b:if>
<b:template-skin>
<![CDATA[
/* CSS FOR LAYOUT */
body#layout, body#layout div.section {font-family: Arial, sans-serif;}
body#layout {max-width: 1040px;}
body#layout #wrapper {overflow: unset;}
body#layout ul li {display:none}
body#layout:before {content: "v.1";position: absolute;top: 20px;right: 20px;z-index: 1;padding: 10px 20px;font-size: 18px;color: #333;background: #fff;border-radius: 20px;border: 1pxsolid #333;}
body#layout div.widget {float: none;margin: 0;padding: 0;position: relative;width: 100%;height: 100%}
body#layout #labelbottom {width: auto;}
body#layout #widget-footer-wrapper {max-width: 100%;}
body#layout .visibility .editlink.icon, body#layout .editlink {background-image: url(https://www.gstatic.com/images/icons/material/system/1x/mode_edit_grey600_24dp.png)!important;background-color: #eee!important;padding: 11px!important;font-size: 0 !important;background-position: center!important;background-repeat: no-repeat!important;height: 24px;width: 24px;}
body#layout #wrapper, body#layout #widget-footer-container, body#layout nav.dropdowns, body#layout #widget-footer {margin: 0!important;padding: 0!important;}
body#layout #widget-footer-container {margin-bottom: 36px;padding: 10px;}
body#layout #widget-footer-container {margin-bottom: 15px!important;padding: 10px!important;}
body#layout .add_widget {margin: 5px 10px;}
body#layout #PopularPosts1 {padding: 10px;}
body#layout .widget-wrap1 {width: 100%;}
body#layout .widget-content {box-shadow: none;}
body#layout #navbar {display: block;margin: 0;max-width: 100%;padding: 0 20px;margin-bottom: 12px;}
body#layout .header {width: auto;}
body#layout #navbar:before {content: "Untuk mempercepat loading blog, klik edit dan nonaktifkan Navbar ==>>";position: absolute;bottom: 18px;z-index: 999;right: 80px;color: #999;font-size: 12px;}
body#layout #wrapper, body#layout #header-wrapper, body#layout #footer-container, body#layout #widget-footer-container, body#layout nav.dropdowns {margin: 0 0;padding: 0 20px;}
body#layout #footer-container {padding-bottom: 20px;}
body#layout #widget-footer1 {width: 32%;float: left;padding-right: 2%;box-sizing: border-box;}
body#layout #widget-footer2 {width: 32%;float: left;}
body#layout #widget-footer3 {width: 32%;float: right;padding-left: 2%;box-sizing: border-box;}
body#layout #cssmenu {display: block;padding: 20px;margin: 8px 0;width: 500px;font-size: 14px;color: #fff;background: #bbbbbb;font-weight: bold;float: right;}
body#layout #cssmenu:after {content: "Menu navigasi harus diedit melalui Edit HTML";color: #fff;position: absolute;top: 30px;left: 20px;visibility: visible;}
body#layout #searchfs, body#layout .section h4 {display: none;}
body#layout div.section { background: transparent;margin: 0px 0px 15px 0px;padding: 0px;border: none;-webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;}
body#layout .above-post-widget:before {content: "Widget di Atas Post (Hanya Homepage)";}
body#layout .Blog:before {content: "Posting Blog";margin-bottom: 8px;}
body#layout .bellow-header-widget:before {content: "Widget di Bawah Header/Menu Navigasi";}
body#layout #widget-footer-container:before {content: "Widget di Atas Footer";}
body#layout .above-post-widget:before, body#layout .Blog:before, body#layout .bellow-header-widget:before, body#layout #widget-footer-container:before {padding: 10px;display: block;font-size: 15px;color: #fff;background: #e64a19;box-shadow: rgba(0,0,0,0.12) 0 0 2px 0, rgba(0,0,0,0.24) 0 2px 2px 0;}
body#layout .add_widget, body#layout .widget-content {padding: 12px;}
body#layout .add_widget a {margin-left: 0px;font-size: 14px;}
body#layout div.layout-title {font-size: 14px;}
body#layout div.layout-widget-description {font-size: 12px;}
body#layout .editlink {color: #FFFFFF !important;background: #bbbbbb;border-radius: 15px;padding: 4px 6px;}
body#layout #footer-wrapper {position: relative;background: #fff;height: 40px;border: 1px solid #ddd;}
body#layout #footer-wrapper:after {content:"Footer";color:#999;position:absolute;top:12px;}
]]></b:template-skin>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
<style>
/* ERROR PAGE */
.status-msg-body:after, .status-msg-hidden:after {content: &quot;404&quot;;font-size: 140px;display: block;margin: 30px 0;color: #e86e6e;font-weight: 500;text-shadow: 6px 6px #efefef;}
#post-wrapper {width: 100%;max-width: 100%;}
.status-msg-body {padding: 30px 0;}
</style>
</b:if>
<script>//<![CDATA[
/*! jQuery v2.1.3 | (c) 2005, 2014 jQuery Foundation, Inc. | jquery.org/license */
!function(e,t){"use strict";"object"==typeof module&&"object"==typeof module.exports?module.exports=e.document?t(e,!0):function(e){if(!e.document)throw new Error("jQuery requires a window with a document");return t(e)}:t(e)}("undefined"!=typeof window?window:this,function(C,e){"use strict";var t=[],r=Object.getPrototypeOf,s=t.slice,g=t.flat?function(e){return t.flat.call(e)}:function(e){return t.concat.apply([],e)},u=t.push,i=t.indexOf,n={},o=n.toString,v=n.hasOwnProperty,a=v.toString,l=a.call(Object),y={},m=function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},x=function(e){return null!=e&&e===e.window},E=C.document,c={type:!0,src:!0,nonce:!0,noModule:!0};function b(e,t,n){var r,i,o=(n=n||E).createElement("script");if(o.text=e,t)for(r in c)(i=t[r]||t.getAttribute&&t.getAttribute(r))&&o.setAttribute(r,i);n.head.appendChild(o).parentNode.removeChild(o)}function w(e){return null==e?e+"":"object"==typeof e||"function"==typeof e?n[o.call(e)]||"object":typeof e}var f="3.5.1",S=function(e,t){return new S.fn.init(e,t)};function p(e){var t=!!e&&"length"in e&&e.length,n=w(e);return!m(e)&&!x(e)&&("array"===n||0===t||"number"==typeof t&&0<t&&t-1 in e)}S.fn=S.prototype={jquery:f,constructor:S,length:0,toArray:function(){return s.call(this)},get:function(e){return null==e?s.call(this):e<0?this[e+this.length]:this[e]},pushStack:function(e){var t=S.merge(this.constructor(),e);return t.prevObject=this,t},each:function(e){return S.each(this,e)},map:function(n){return this.pushStack(S.map(this,function(e,t){return n.call(e,t,e)}))},slice:function(){return this.pushStack(s.apply(this,arguments))},first:function(){return this.eq(0)},last:function(){return this.eq(-1)},even:function(){return this.pushStack(S.grep(this,function(e,t){return(t+1)%2}))},odd:function(){return this.pushStack(S.grep(this,function(e,t){return t%2}))},eq:function(e){var t=this.length,n=+e+(e<0?t:0);return this.pushStack(0<=n&&n<t?[this[n]]:[])},end:function(){return this.prevObject||this.constructor()},push:u,sort:t.sort,splice:t.splice},S.extend=S.fn.extend=function(){var e,t,n,r,i,o,a=arguments[0]||{},s=1,u=arguments.length,l=!1;for("boolean"==typeof a&&(l=a,a=arguments[s]||{},s++),"object"==typeof a||m(a)||(a={}),s===u&&(a=this,s--);s<u;s++)if(null!=(e=arguments[s]))for(t in e)r=e[t],"__proto__"!==t&&a!==r&&(l&&r&&(S.isPlainObject(r)||(i=Array.isArray(r)))?(n=a[t],o=i&&!Array.isArray(n)?[]:i||S.isPlainObject(n)?n:{},i=!1,a[t]=S.extend(l,o,r)):void 0!==r&&(a[t]=r));return a},S.extend({expando:"jQuery"+(f+Math.random()).replace(/\D/g,""),isReady:!0,error:function(e){throw new Error(e)},noop:function(){},isPlainObject:function(e){var t,n;return!(!e||"[object Object]"!==o.call(e))&&(!(t=r(e))||"function"==typeof(n=v.call(t,"constructor")&&t.constructor)&&a.call(n)===l)},isEmptyObject:function(e){var t;for(t in e)return!1;return!0},globalEval:function(e,t,n){b(e,{nonce:t&&t.nonce},n)},each:function(e,t){var n,r=0;if(p(e)){for(n=e.length;r<n;r++)if(!1===t.call(e[r],r,e[r]))break}else for(r in e)if(!1===t.call(e[r],r,e[r]))break;return e},makeArray:function(e,t){var n=t||[];return null!=e&&(p(Object(e))?S.merge(n,"string"==typeof e?[e]:e):u.call(n,e)),n},inArray:function(e,t,n){return null==t?-1:i.call(t,e,n)},merge:function(e,t){for(var n=+t.length,r=0,i=e.length;r<n;r++)e[i++]=t[r];return e.length=i,e},grep:function(e,t,n){for(var r=[],i=0,o=e.length,a=!n;i<o;i++)!t(e[i],i)!==a&&r.push(e[i]);return r},map:function(e,t,n){var r,i,o=0,a=[];if(p(e))for(r=e.length;o<r;o++)null!=(i=t(e[o],o,n))&&a.push(i);else for(o in e)null!=(i=t(e[o],o,n))&&a.push(i);return g(a)},guid:1,support:y}),"function"==typeof Symbol&&(S.fn[Symbol.iterator]=t[Symbol.iterator]),S.each("Boolean Number String Function Array Date RegExp Object Error Symbol".split(" "),function(e,t){n["[object "+t+"]"]=t.toLowerCase()});var d=function(n){var e,d,b,o,i,h,f,g,w,u,l,T,C,a,E,v,s,c,y,S="sizzle"+1*new Date,p=n.document,k=0,r=0,m=ue(),x=ue(),A=ue(),N=ue(),D=function(e,t){return e===t&&(l=!0),0},j={}.hasOwnProperty,t=[],q=t.pop,L=t.push,H=t.push,O=t.slice,P=function(e,t){for(var n=0,r=e.length;n<r;n++)if(e[n]===t)return n;return-1},R="checked|selected|async|autofocus|autoplay|controls|defer|disabled|hidden|ismap|loop|multiple|open|readonly|required|scoped",M="[\\x20\\t\\r\\n\\f]",I="(?:\\\\[\\da-fA-F]{1,6}"+M+"?|\\\\[^\\r\\n\\f]|[\\w-]|[^\0-\\x7f])+",W="\\["+M+"*("+I+")(?:"+M+"*([*^$|!~]?=)"+M+"*(?:'((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\"|("+I+"))|)"+M+"*\\]",F=":("+I+")(?:\\((('((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\")|((?:\\\\.|[^\\\\()[\\]]|"+W+")*)|.*)\\)|)",B=new RegExp(M+"+","g"),$=new RegExp("^"+M+"+|((?:^|[^\\\\])(?:\\\\.)*)"+M+"+$","g"),_=new RegExp("^"+M+"*,"+M+"*"),z=new RegExp("^"+M+"*([>+~]|"+M+")"+M+"*"),U=new RegExp(M+"|>"),X=new RegExp(F),V=new RegExp("^"+I+"$"),G={ID:new RegExp("^#("+I+")"),CLASS:new RegExp("^\\.("+I+")"),TAG:new RegExp("^("+I+"|[*])"),ATTR:new RegExp("^"+W),PSEUDO:new RegExp("^"+F),CHILD:new RegExp("^:(only|first|last|nth|nth-last)-(child|of-type)(?:\\("+M+"*(even|odd|(([+-]|)(\\d*)n|)"+M+"*(?:([+-]|)"+M+"*(\\d+)|))"+M+"*\\)|)","i"),bool:new RegExp("^(?:"+R+")$","i"),needsContext:new RegExp("^"+M+"*[>+~]|:(even|odd|eq|gt|lt|nth|first|last)(?:\\("+M+"*((?:-\\d)?\\d*)"+M+"*\\)|)(?=[^-]|$)","i")},Y=/HTML$/i,Q=/^(?:input|select|textarea|button)$/i,J=/^h\d$/i,K=/^[^{]+\{\s*\[native \w/,Z=/^(?:#([\w-]+)|(\w+)|\.([\w-]+))$/,ee=/[+~]/,te=new RegExp("\\\\[\\da-fA-F]{1,6}"+M+"?|\\\\([^\\r\\n\\f])","g"),ne=function(e,t){var n="0x"+e.slice(1)-65536;return t||(n<0?String.fromCharCode(n+65536):String.fromCharCode(n>>10|55296,1023&n|56320))},re=/([\0-\x1f\x7f]|^-?\d)|^-$|[^\0-\x1f\x7f-\uFFFF\w-]/g,ie=function(e,t){return t?"\0"===e?"\ufffd":e.slice(0,-1)+"\\"+e.charCodeAt(e.length-1).toString(16)+" ":"\\"+e},oe=function(){T()},ae=be(function(e){return!0===e.disabled&&"fieldset"===e.nodeName.toLowerCase()},{dir:"parentNode",next:"legend"});try{H.apply(t=O.call(p.childNodes),p.childNodes),t[p.childNodes.length].nodeType}catch(e){H={apply:t.length?function(e,t){L.apply(e,O.call(t))}:function(e,t){var n=e.length,r=0;while(e[n++]=t[r++]);e.length=n-1}}}function se(t,e,n,r){var i,o,a,s,u,l,c,f=e&&e.ownerDocument,p=e?e.nodeType:9;if(n=n||[],"string"!=typeof t||!t||1!==p&&9!==p&&11!==p)return n;if(!r&&(T(e),e=e||C,E)){if(11!==p&&(u=Z.exec(t)))if(i=u[1]){if(9===p){if(!(a=e.getElementById(i)))return n;if(a.id===i)return n.push(a),n}else if(f&&(a=f.getElementById(i))&&y(e,a)&&a.id===i)return n.push(a),n}else{if(u[2])return H.apply(n,e.getElementsByTagName(t)),n;if((i=u[3])&&d.getElementsByClassName&&e.getElementsByClassName)return H.apply(n,e.getElementsByClassName(i)),n}if(d.qsa&&!N[t+" "]&&(!v||!v.test(t))&&(1!==p||"object"!==e.nodeName.toLowerCase())){if(c=t,f=e,1===p&&(U.test(t)||z.test(t))){(f=ee.test(t)&&ye(e.parentNode)||e)===e&&d.scope||((s=e.getAttribute("id"))?s=s.replace(re,ie):e.setAttribute("id",s=S)),o=(l=h(t)).length;while(o--)l[o]=(s?"#"+s:":scope")+" "+xe(l[o]);c=l.join(",")}try{return H.apply(n,f.querySelectorAll(c)),n}catch(e){N(t,!0)}finally{s===S&&e.removeAttribute("id")}}}return g(t.replace($,"$1"),e,n,r)}function ue(){var r=[];return function e(t,n){return r.push(t+" ")>b.cacheLength&&delete e[r.shift()],e[t+" "]=n}}function le(e){return e[S]=!0,e}function ce(e){var t=C.createElement("fieldset");try{return!!e(t)}catch(e){return!1}finally{t.parentNode&&t.parentNode.removeChild(t),t=null}}function fe(e,t){var n=e.split("|"),r=n.length;while(r--)b.attrHandle[n[r]]=t}function pe(e,t){var n=t&&e,r=n&&1===e.nodeType&&1===t.nodeType&&e.sourceIndex-t.sourceIndex;if(r)return r;if(n)while(n=n.nextSibling)if(n===t)return-1;return e?1:-1}function de(t){return function(e){return"input"===e.nodeName.toLowerCase()&&e.type===t}}function he(n){return function(e){var t=e.nodeName.toLowerCase();return("input"===t||"button"===t)&&e.type===n}}function ge(t){return function(e){return"form"in e?e.parentNode&&!1===e.disabled?"label"in e?"label"in e.parentNode?e.parentNode.disabled===t:e.disabled===t:e.isDisabled===t||e.isDisabled!==!t&&ae(e)===t:e.disabled===t:"label"in e&&e.disabled===t}}function ve(a){return le(function(o){return o=+o,le(function(e,t){var n,r=a([],e.length,o),i=r.length;while(i--)e[n=r[i]]&&(e[n]=!(t[n]=e[n]))})})}function ye(e){return e&&"undefined"!=typeof e.getElementsByTagName&&e}for(e in d=se.support={},i=se.isXML=function(e){var t=e.namespaceURI,n=(e.ownerDocument||e).documentElement;return!Y.test(t||n&&n.nodeName||"HTML")},T=se.setDocument=function(e){var t,n,r=e?e.ownerDocument||e:p;return r!=C&&9===r.nodeType&&r.documentElement&&(a=(C=r).documentElement,E=!i(C),p!=C&&(n=C.defaultView)&&n.top!==n&&(n.addEventListener?n.addEventListener("unload",oe,!1):n.attachEvent&&n.attachEvent("onunload",oe)),d.scope=ce(function(e){return a.appendChild(e).appendChild(C.createElement("div")),"undefined"!=typeof e.querySelectorAll&&!e.querySelectorAll(":scope fieldset div").length}),d.attributes=ce(function(e){return e.className="i",!e.getAttribute("className")}),d.getElementsByTagName=ce(function(e){return e.appendChild(C.createComment("")),!e.getElementsByTagName("*").length}),d.getElementsByClassName=K.test(C.getElementsByClassName),d.getById=ce(function(e){return a.appendChild(e).id=S,!C.getElementsByName||!C.getElementsByName(S).length}),d.getById?(b.filter.ID=function(e){var t=e.replace(te,ne);return function(e){return e.getAttribute("id")===t}},b.find.ID=function(e,t){if("undefined"!=typeof t.getElementById&&E){var n=t.getElementById(e);return n?[n]:[]}}):(b.filter.ID=function(e){var n=e.replace(te,ne);return function(e){var t="undefined"!=typeof e.getAttributeNode&&e.getAttributeNode("id");return t&&t.value===n}},b.find.ID=function(e,t){if("undefined"!=typeof t.getElementById&&E){var n,r,i,o=t.getElementById(e);if(o){if((n=o.getAttributeNode("id"))&&n.value===e)return[o];i=t.getElementsByName(e),r=0;while(o=i[r++])if((n=o.getAttributeNode("id"))&&n.value===e)return[o]}return[]}}),b.find.TAG=d.getElementsByTagName?function(e,t){return"undefined"!=typeof t.getElementsByTagName?t.getElementsByTagName(e):d.qsa?t.querySelectorAll(e):void 0}:function(e,t){var n,r=[],i=0,o=t.getElementsByTagName(e);if("*"===e){while(n=o[i++])1===n.nodeType&&r.push(n);return r}return o},b.find.CLASS=d.getElementsByClassName&&function(e,t){if("undefined"!=typeof t.getElementsByClassName&&E)return t.getElementsByClassName(e)},s=[],v=[],(d.qsa=K.test(C.querySelectorAll))&&(ce(function(e){var t;a.appendChild(e).innerHTML="<a id='"+S+"'></a><select id='"+S+"-\r\\' msallowcapture=''><option selected=''></option></select>",e.querySelectorAll("[msallowcapture^='']").length&&v.push("[*^$]="+M+"*(?:''|\"\")"),e.querySelectorAll("[selected]").length||v.push("\\["+M+"*(?:value|"+R+")"),e.querySelectorAll("[id~="+S+"-]").length||v.push("~="),(t=C.createElement("input")).setAttribute("name",""),e.appendChild(t),e.querySelectorAll("[name='']").length||v.push("\\["+M+"*name"+M+"*="+M+"*(?:''|\"\")"),e.querySelectorAll(":checked").length||v.push(":checked"),e.querySelectorAll("a#"+S+"+*").length||v.push(".#.+[+~]"),e.querySelectorAll("\\\f"),v.push("[\\r\\n\\f]")}),ce(function(e){e.innerHTML="<a href='' disabled='disabled'></a><select disabled='disabled'><option/></select>";var t=C.createElement("input");t.setAttribute("type","hidden"),e.appendChild(t).setAttribute("name","D"),e.querySelectorAll("[name=d]").length&&v.push("name"+M+"*[*^$|!~]?="),2!==e.querySelectorAll(":enabled").length&&v.push(":enabled",":disabled"),a.appendChild(e).disabled=!0,2!==e.querySelectorAll(":disabled").length&&v.push(":enabled",":disabled"),e.querySelectorAll("*,:x"),v.push(",.*:")})),(d.matchesSelector=K.test(c=a.matches||a.webkitMatchesSelector||a.mozMatchesSelector||a.oMatchesSelector||a.msMatchesSelector))&&ce(function(e){d.disconnectedMatch=c.call(e,"*"),c.call(e,"[s!='']:x"),s.push("!=",F)}),v=v.length&&new RegExp(v.join("|")),s=s.length&&new RegExp(s.join("|")),t=K.test(a.compareDocumentPosition),y=t||K.test(a.contains)?function(e,t){var n=9===e.nodeType?e.documentElement:e,r=t&&t.parentNode;return e===r||!(!r||1!==r.nodeType||!(n.contains?n.contains(r):e.compareDocumentPosition&&16&e.compareDocumentPosition(r)))}:function(e,t){if(t)while(t=t.parentNode)if(t===e)return!0;return!1},D=t?function(e,t){if(e===t)return l=!0,0;var n=!e.compareDocumentPosition-!t.compareDocumentPosition;return n||(1&(n=(e.ownerDocument||e)==(t.ownerDocument||t)?e.compareDocumentPosition(t):1)||!d.sortDetached&&t.compareDocumentPosition(e)===n?e==C||e.ownerDocument==p&&y(p,e)?-1:t==C||t.ownerDocument==p&&y(p,t)?1:u?P(u,e)-P(u,t):0:4&n?-1:1)}:function(e,t){if(e===t)return l=!0,0;var n,r=0,i=e.parentNode,o=t.parentNode,a=[e],s=[t];if(!i||!o)return e==C?-1:t==C?1:i?-1:o?1:u?P(u,e)-P(u,t):0;if(i===o)return pe(e,t);n=e;while(n=n.parentNode)a.unshift(n);n=t;while(n=n.parentNode)s.unshift(n);while(a[r]===s[r])r++;return r?pe(a[r],s[r]):a[r]==p?-1:s[r]==p?1:0}),C},se.matches=function(e,t){return se(e,null,null,t)},se.matchesSelector=function(e,t){if(T(e),d.matchesSelector&&E&&!N[t+" "]&&(!s||!s.test(t))&&(!v||!v.test(t)))try{var n=c.call(e,t);if(n||d.disconnectedMatch||e.document&&11!==e.document.nodeType)return n}catch(e){N(t,!0)}return 0<se(t,C,null,[e]).length},se.contains=function(e,t){return(e.ownerDocument||e)!=C&&T(e),y(e,t)},se.attr=function(e,t){(e.ownerDocument||e)!=C&&T(e);var n=b.attrHandle[t.toLowerCase()],r=n&&j.call(b.attrHandle,t.toLowerCase())?n(e,t,!E):void 0;return void 0!==r?r:d.attributes||!E?e.getAttribute(t):(r=e.getAttributeNode(t))&&r.specified?r.value:null},se.escape=function(e){return(e+"").replace(re,ie)},se.error=function(e){throw new Error("Syntax error, unrecognized expression: "+e)},se.uniqueSort=function(e){var t,n=[],r=0,i=0;if(l=!d.detectDuplicates,u=!d.sortStable&&e.slice(0),e.sort(D),l){while(t=e[i++])t===e[i]&&(r=n.push(i));while(r--)e.splice(n[r],1)}return u=null,e},o=se.getText=function(e){var t,n="",r=0,i=e.nodeType;if(i){if(1===i||9===i||11===i){if("string"==typeof e.textContent)return e.textContent;for(e=e.firstChild;e;e=e.nextSibling)n+=o(e)}else if(3===i||4===i)return e.nodeValue}else while(t=e[r++])n+=o(t);return n},(b=se.selectors={cacheLength:50,createPseudo:le,match:G,attrHandle:{},find:{},relative:{">":{dir:"parentNode",first:!0}," ":{dir:"parentNode"},"+":{dir:"previousSibling",first:!0},"~":{dir:"previousSibling"}},preFilter:{ATTR:function(e){return e[1]=e[1].replace(te,ne),e[3]=(e[3]||e[4]||e[5]||"").replace(te,ne),"~="===e[2]&&(e[3]=" "+e[3]+" "),e.slice(0,4)},CHILD:function(e){return e[1]=e[1].toLowerCase(),"nth"===e[1].slice(0,3)?(e[3]||se.error(e[0]),e[4]=+(e[4]?e[5]+(e[6]||1):2*("even"===e[3]||"odd"===e[3])),e[5]=+(e[7]+e[8]||"odd"===e[3])):e[3]&&se.error(e[0]),e},PSEUDO:function(e){var t,n=!e[6]&&e[2];return G.CHILD.test(e[0])?null:(e[3]?e[2]=e[4]||e[5]||"":n&&X.test(n)&&(t=h(n,!0))&&(t=n.indexOf(")",n.length-t)-n.length)&&(e[0]=e[0].slice(0,t),e[2]=n.slice(0,t)),e.slice(0,3))}},filter:{TAG:function(e){var t=e.replace(te,ne).toLowerCase();return"*"===e?function(){return!0}:function(e){return e.nodeName&&e.nodeName.toLowerCase()===t}},CLASS:function(e){var t=m[e+" "];return t||(t=new RegExp("(^|"+M+")"+e+"("+M+"|$)"))&&m(e,function(e){return t.test("string"==typeof e.className&&e.className||"undefined"!=typeof e.getAttribute&&e.getAttribute("class")||"")})},ATTR:function(n,r,i){return function(e){var t=se.attr(e,n);return null==t?"!="===r:!r||(t+="","="===r?t===i:"!="===r?t!==i:"^="===r?i&&0===t.indexOf(i):"*="===r?i&&-1<t.indexOf(i):"$="===r?i&&t.slice(-i.length)===i:"~="===r?-1<(" "+t.replace(B," ")+" ").indexOf(i):"|="===r&&(t===i||t.slice(0,i.length+1)===i+"-"))}},CHILD:function(h,e,t,g,v){var y="nth"!==h.slice(0,3),m="last"!==h.slice(-4),x="of-type"===e;return 1===g&&0===v?function(e){return!!e.parentNode}:function(e,t,n){var r,i,o,a,s,u,l=y!==m?"nextSibling":"previousSibling",c=e.parentNode,f=x&&e.nodeName.toLowerCase(),p=!n&&!x,d=!1;if(c){if(y){while(l){a=e;while(a=a[l])if(x?a.nodeName.toLowerCase()===f:1===a.nodeType)return!1;u=l="only"===h&&!u&&"nextSibling"}return!0}if(u=[m?c.firstChild:c.lastChild],m&&p){d=(s=(r=(i=(o=(a=c)[S]||(a[S]={}))[a.uniqueID]||(o[a.uniqueID]={}))[h]||[])[0]===k&&r[1])&&r[2],a=s&&c.childNodes[s];while(a=++s&&a&&a[l]||(d=s=0)||u.pop())if(1===a.nodeType&&++d&&a===e){i[h]=[k,s,d];break}}else if(p&&(d=s=(r=(i=(o=(a=e)[S]||(a[S]={}))[a.uniqueID]||(o[a.uniqueID]={}))[h]||[])[0]===k&&r[1]),!1===d)while(a=++s&&a&&a[l]||(d=s=0)||u.pop())if((x?a.nodeName.toLowerCase()===f:1===a.nodeType)&&++d&&(p&&((i=(o=a[S]||(a[S]={}))[a.uniqueID]||(o[a.uniqueID]={}))[h]=[k,d]),a===e))break;return(d-=v)===g||d%g==0&&0<=d/g}}},PSEUDO:function(e,o){var t,a=b.pseudos[e]||b.setFilters[e.toLowerCase()]||se.error("unsupported pseudo: "+e);return a[S]?a(o):1<a.length?(t=[e,e,"",o],b.setFilters.hasOwnProperty(e.toLowerCase())?le(function(e,t){var n,r=a(e,o),i=r.length;while(i--)e[n=P(e,r[i])]=!(t[n]=r[i])}):function(e){return a(e,0,t)}):a}},pseudos:{not:le(function(e){var r=[],i=[],s=f(e.replace($,"$1"));return s[S]?le(function(e,t,n,r){var i,o=s(e,null,r,[]),a=e.length;while(a--)(i=o[a])&&(e[a]=!(t[a]=i))}):function(e,t,n){return r[0]=e,s(r,null,n,i),r[0]=null,!i.pop()}}),has:le(function(t){return function(e){return 0<se(t,e).length}}),contains:le(function(t){return t=t.replace(te,ne),function(e){return-1<(e.textContent||o(e)).indexOf(t)}}),lang:le(function(n){return V.test(n||"")||se.error("unsupported lang: "+n),n=n.replace(te,ne).toLowerCase(),function(e){var t;do{if(t=E?e.lang:e.getAttribute("xml:lang")||e.getAttribute("lang"))return(t=t.toLowerCase())===n||0===t.indexOf(n+"-")}while((e=e.parentNode)&&1===e.nodeType);return!1}}),target:function(e){var t=n.location&&n.location.hash;return t&&t.slice(1)===e.id},root:function(e){return e===a},focus:function(e){return e===C.activeElement&&(!C.hasFocus||C.hasFocus())&&!!(e.type||e.href||~e.tabIndex)},enabled:ge(!1),disabled:ge(!0),checked:function(e){var t=e.nodeName.toLowerCase();return"input"===t&&!!e.checked||"option"===t&&!!e.selected},selected:function(e){return e.parentNode&&e.parentNode.selectedIndex,!0===e.selected},empty:function(e){for(e=e.firstChild;e;e=e.nextSibling)if(e.nodeType<6)return!1;return!0},parent:function(e){return!b.pseudos.empty(e)},header:function(e){return J.test(e.nodeName)},input:function(e){return Q.test(e.nodeName)},button:function(e){var t=e.nodeName.toLowerCase();return"input"===t&&"button"===e.type||"button"===t},text:function(e){var t;return"input"===e.nodeName.toLowerCase()&&"text"===e.type&&(null==(t=e.getAttribute("type"))||"text"===t.toLowerCase())},first:ve(function(){return[0]}),last:ve(function(e,t){return[t-1]}),eq:ve(function(e,t,n){return[n<0?n+t:n]}),even:ve(function(e,t){for(var n=0;n<t;n+=2)e.push(n);return e}),odd:ve(function(e,t){for(var n=1;n<t;n+=2)e.push(n);return e}),lt:ve(function(e,t,n){for(var r=n<0?n+t:t<n?t:n;0<=--r;)e.push(r);return e}),gt:ve(function(e,t,n){for(var r=n<0?n+t:n;++r<t;)e.push(r);return e})}}).pseudos.nth=b.pseudos.eq,{radio:!0,checkbox:!0,file:!0,password:!0,image:!0})b.pseudos[e]=de(e);for(e in{submit:!0,reset:!0})b.pseudos[e]=he(e);function me(){}function xe(e){for(var t=0,n=e.length,r="";t<n;t++)r+=e[t].value;return r}function be(s,e,t){var u=e.dir,l=e.next,c=l||u,f=t&&"parentNode"===c,p=r++;return e.first?function(e,t,n){while(e=e[u])if(1===e.nodeType||f)return s(e,t,n);return!1}:function(e,t,n){var r,i,o,a=[k,p];if(n){while(e=e[u])if((1===e.nodeType||f)&&s(e,t,n))return!0}else while(e=e[u])if(1===e.nodeType||f)if(i=(o=e[S]||(e[S]={}))[e.uniqueID]||(o[e.uniqueID]={}),l&&l===e.nodeName.toLowerCase())e=e[u]||e;else{if((r=i[c])&&r[0]===k&&r[1]===p)return a[2]=r[2];if((i[c]=a)[2]=s(e,t,n))return!0}return!1}}function we(i){return 1<i.length?function(e,t,n){var r=i.length;while(r--)if(!i[r](e,t,n))return!1;return!0}:i[0]}function Te(e,t,n,r,i){for(var o,a=[],s=0,u=e.length,l=null!=t;s<u;s++)(o=e[s])&&(n&&!n(o,r,i)||(a.push(o),l&&t.push(s)));return a}function Ce(d,h,g,v,y,e){return v&&!v[S]&&(v=Ce(v)),y&&!y[S]&&(y=Ce(y,e)),le(function(e,t,n,r){var i,o,a,s=[],u=[],l=t.length,c=e||function(e,t,n){for(var r=0,i=t.length;r<i;r++)se(e,t[r],n);return n}(h||"*",n.nodeType?[n]:n,[]),f=!d||!e&&h?c:Te(c,s,d,n,r),p=g?y||(e?d:l||v)?[]:t:f;if(g&&g(f,p,n,r),v){i=Te(p,u),v(i,[],n,r),o=i.length;while(o--)(a=i[o])&&(p[u[o]]=!(f[u[o]]=a))}if(e){if(y||d){if(y){i=[],o=p.length;while(o--)(a=p[o])&&i.push(f[o]=a);y(null,p=[],i,r)}o=p.length;while(o--)(a=p[o])&&-1<(i=y?P(e,a):s[o])&&(e[i]=!(t[i]=a))}}else p=Te(p===t?p.splice(l,p.length):p),y?y(null,t,p,r):H.apply(t,p)})}function Ee(e){for(var i,t,n,r=e.length,o=b.relative[e[0].type],a=o||b.relative[" "],s=o?1:0,u=be(function(e){return e===i},a,!0),l=be(function(e){return-1<P(i,e)},a,!0),c=[function(e,t,n){var r=!o&&(n||t!==w)||((i=t).nodeType?u(e,t,n):l(e,t,n));return i=null,r}];s<r;s++)if(t=b.relative[e[s].type])c=[be(we(c),t)];else{if((t=b.filter[e[s].type].apply(null,e[s].matches))[S]){for(n=++s;n<r;n++)if(b.relative[e[n].type])break;return Ce(1<s&&we(c),1<s&&xe(e.slice(0,s-1).concat({value:" "===e[s-2].type?"*":""})).replace($,"$1"),t,s<n&&Ee(e.slice(s,n)),n<r&&Ee(e=e.slice(n)),n<r&&xe(e))}c.push(t)}return we(c)}return me.prototype=b.filters=b.pseudos,b.setFilters=new me,h=se.tokenize=function(e,t){var n,r,i,o,a,s,u,l=x[e+" "];if(l)return t?0:l.slice(0);a=e,s=[],u=b.preFilter;while(a){for(o in n&&!(r=_.exec(a))||(r&&(a=a.slice(r[0].length)||a),s.push(i=[])),n=!1,(r=z.exec(a))&&(n=r.shift(),i.push({value:n,type:r[0].replace($," ")}),a=a.slice(n.length)),b.filter)!(r=G[o].exec(a))||u[o]&&!(r=u[o](r))||(n=r.shift(),i.push({value:n,type:o,matches:r}),a=a.slice(n.length));if(!n)break}return t?a.length:a?se.error(e):x(e,s).slice(0)},f=se.compile=function(e,t){var n,v,y,m,x,r,i=[],o=[],a=A[e+" "];if(!a){t||(t=h(e)),n=t.length;while(n--)(a=Ee(t[n]))[S]?i.push(a):o.push(a);(a=A(e,(v=o,m=0<(y=i).length,x=0<v.length,r=function(e,t,n,r,i){var o,a,s,u=0,l="0",c=e&&[],f=[],p=w,d=e||x&&b.find.TAG("*",i),h=k+=null==p?1:Math.random()||.1,g=d.length;for(i&&(w=t==C||t||i);l!==g&&null!=(o=d[l]);l++){if(x&&o){a=0,t||o.ownerDocument==C||(T(o),n=!E);while(s=v[a++])if(s(o,t||C,n)){r.push(o);break}i&&(k=h)}m&&((o=!s&&o)&&u--,e&&c.push(o))}if(u+=l,m&&l!==u){a=0;while(s=y[a++])s(c,f,t,n);if(e){if(0<u)while(l--)c[l]||f[l]||(f[l]=q.call(r));f=Te(f)}H.apply(r,f),i&&!e&&0<f.length&&1<u+y.length&&se.uniqueSort(r)}return i&&(k=h,w=p),c},m?le(r):r))).selector=e}return a},g=se.select=function(e,t,n,r){var i,o,a,s,u,l="function"==typeof e&&e,c=!r&&h(e=l.selector||e);if(n=n||[],1===c.length){if(2<(o=c[0]=c[0].slice(0)).length&&"ID"===(a=o[0]).type&&9===t.nodeType&&E&&b.relative[o[1].type]){if(!(t=(b.find.ID(a.matches[0].replace(te,ne),t)||[])[0]))return n;l&&(t=t.parentNode),e=e.slice(o.shift().value.length)}i=G.needsContext.test(e)?0:o.length;while(i--){if(a=o[i],b.relative[s=a.type])break;if((u=b.find[s])&&(r=u(a.matches[0].replace(te,ne),ee.test(o[0].type)&&ye(t.parentNode)||t))){if(o.splice(i,1),!(e=r.length&&xe(o)))return H.apply(n,r),n;break}}}return(l||f(e,c))(r,t,!E,n,!t||ee.test(e)&&ye(t.parentNode)||t),n},d.sortStable=S.split("").sort(D).join("")===S,d.detectDuplicates=!!l,T(),d.sortDetached=ce(function(e){return 1&e.compareDocumentPosition(C.createElement("fieldset"))}),ce(function(e){return e.innerHTML="<a href='#'></a>","#"===e.firstChild.getAttribute("href")})||fe("type|href|height|width",function(e,t,n){if(!n)return e.getAttribute(t,"type"===t.toLowerCase()?1:2)}),d.attributes&&ce(function(e){return e.innerHTML="<input/>",e.firstChild.setAttribute("value",""),""===e.firstChild.getAttribute("value")})||fe("value",function(e,t,n){if(!n&&"input"===e.nodeName.toLowerCase())return e.defaultValue}),ce(function(e){return null==e.getAttribute("disabled")})||fe(R,function(e,t,n){var r;if(!n)return!0===e[t]?t.toLowerCase():(r=e.getAttributeNode(t))&&r.specified?r.value:null}),se}(C);S.find=d,S.expr=d.selectors,S.expr[":"]=S.expr.pseudos,S.uniqueSort=S.unique=d.uniqueSort,S.text=d.getText,S.isXMLDoc=d.isXML,S.contains=d.contains,S.escapeSelector=d.escape;var h=function(e,t,n){var r=[],i=void 0!==n;while((e=e[t])&&9!==e.nodeType)if(1===e.nodeType){if(i&&S(e).is(n))break;r.push(e)}return r},T=function(e,t){for(var n=[];e;e=e.nextSibling)1===e.nodeType&&e!==t&&n.push(e);return n},k=S.expr.match.needsContext;function A(e,t){return e.nodeName&&e.nodeName.toLowerCase()===t.toLowerCase()}var N=/^<([a-z][^\/\0>:\x20\t\r\n\f]*)[\x20\t\r\n\f]*\/?>(?:<\/\1>|)$/i;function D(e,n,r){return m(n)?S.grep(e,function(e,t){return!!n.call(e,t,e)!==r}):n.nodeType?S.grep(e,function(e){return e===n!==r}):"string"!=typeof n?S.grep(e,function(e){return-1<i.call(n,e)!==r}):S.filter(n,e,r)}S.filter=function(e,t,n){var r=t[0];return n&&(e=":not("+e+")"),1===t.length&&1===r.nodeType?S.find.matchesSelector(r,e)?[r]:[]:S.find.matches(e,S.grep(t,function(e){return 1===e.nodeType}))},S.fn.extend({find:function(e){var t,n,r=this.length,i=this;if("string"!=typeof e)return this.pushStack(S(e).filter(function(){for(t=0;t<r;t++)if(S.contains(i[t],this))return!0}));for(n=this.pushStack([]),t=0;t<r;t++)S.find(e,i[t],n);return 1<r?S.uniqueSort(n):n},filter:function(e){return this.pushStack(D(this,e||[],!1))},not:function(e){return this.pushStack(D(this,e||[],!0))},is:function(e){return!!D(this,"string"==typeof e&&k.test(e)?S(e):e||[],!1).length}});var j,q=/^(?:\s*(<[\w\W]+>)[^>]*|#([\w-]+))$/;(S.fn.init=function(e,t,n){var r,i;if(!e)return this;if(n=n||j,"string"==typeof e){if(!(r="<"===e[0]&&">"===e[e.length-1]&&3<=e.length?[null,e,null]:q.exec(e))||!r[1]&&t)return!t||t.jquery?(t||n).find(e):this.constructor(t).find(e);if(r[1]){if(t=t instanceof S?t[0]:t,S.merge(this,S.parseHTML(r[1],t&&t.nodeType?t.ownerDocument||t:E,!0)),N.test(r[1])&&S.isPlainObject(t))for(r in t)m(this[r])?this[r](t[r]):this.attr(r,t[r]);return this}return(i=E.getElementById(r[2]))&&(this[0]=i,this.length=1),this}return e.nodeType?(this[0]=e,this.length=1,this):m(e)?void 0!==n.ready?n.ready(e):e(S):S.makeArray(e,this)}).prototype=S.fn,j=S(E);var L=/^(?:parents|prev(?:Until|All))/,H={children:!0,contents:!0,next:!0,prev:!0};function O(e,t){while((e=e[t])&&1!==e.nodeType);return e}S.fn.extend({has:function(e){var t=S(e,this),n=t.length;return this.filter(function(){for(var e=0;e<n;e++)if(S.contains(this,t[e]))return!0})},closest:function(e,t){var n,r=0,i=this.length,o=[],a="string"!=typeof e&&S(e);if(!k.test(e))for(;r<i;r++)for(n=this[r];n&&n!==t;n=n.parentNode)if(n.nodeType<11&&(a?-1<a.index(n):1===n.nodeType&&S.find.matchesSelector(n,e))){o.push(n);break}return this.pushStack(1<o.length?S.uniqueSort(o):o)},index:function(e){return e?"string"==typeof e?i.call(S(e),this[0]):i.call(this,e.jquery?e[0]:e):this[0]&&this[0].parentNode?this.first().prevAll().length:-1},add:function(e,t){return this.pushStack(S.uniqueSort(S.merge(this.get(),S(e,t))))},addBack:function(e){return this.add(null==e?this.prevObject:this.prevObject.filter(e))}}),S.each({parent:function(e){var t=e.parentNode;return t&&11!==t.nodeType?t:null},parents:function(e){return h(e,"parentNode")},parentsUntil:function(e,t,n){return h(e,"parentNode",n)},next:function(e){return O(e,"nextSibling")},prev:function(e){return O(e,"previousSibling")},nextAll:function(e){return h(e,"nextSibling")},prevAll:function(e){return h(e,"previousSibling")},nextUntil:function(e,t,n){return h(e,"nextSibling",n)},prevUntil:function(e,t,n){return h(e,"previousSibling",n)},siblings:function(e){return T((e.parentNode||{}).firstChild,e)},children:function(e){return T(e.firstChild)},contents:function(e){return null!=e.contentDocument&&r(e.contentDocument)?e.contentDocument:(A(e,"template")&&(e=e.content||e),S.merge([],e.childNodes))}},function(r,i){S.fn[r]=function(e,t){var n=S.map(this,i,e);return"Until"!==r.slice(-5)&&(t=e),t&&"string"==typeof t&&(n=S.filter(t,n)),1<this.length&&(H[r]||S.uniqueSort(n),L.test(r)&&n.reverse()),this.pushStack(n)}});var P=/[^\x20\t\r\n\f]+/g;function R(e){return e}function M(e){throw e}function I(e,t,n,r){var i;try{e&&m(i=e.promise)?i.call(e).done(t).fail(n):e&&m(i=e.then)?i.call(e,t,n):t.apply(void 0,[e].slice(r))}catch(e){n.apply(void 0,[e])}}S.Callbacks=function(r){var e,n;r="string"==typeof r?(e=r,n={},S.each(e.match(P)||[],function(e,t){n[t]=!0}),n):S.extend({},r);var i,t,o,a,s=[],u=[],l=-1,c=function(){for(a=a||r.once,o=i=!0;u.length;l=-1){t=u.shift();while(++l<s.length)!1===s[l].apply(t[0],t[1])&&r.stopOnFalse&&(l=s.length,t=!1)}r.memory||(t=!1),i=!1,a&&(s=t?[]:"")},f={add:function(){return s&&(t&&!i&&(l=s.length-1,u.push(t)),function n(e){S.each(e,function(e,t){m(t)?r.unique&&f.has(t)||s.push(t):t&&t.length&&"string"!==w(t)&&n(t)})}(arguments),t&&!i&&c()),this},remove:function(){return S.each(arguments,function(e,t){var n;while(-1<(n=S.inArray(t,s,n)))s.splice(n,1),n<=l&&l--}),this},has:function(e){return e?-1<S.inArray(e,s):0<s.length},empty:function(){return s&&(s=[]),this},disable:function(){return a=u=[],s=t="",this},disabled:function(){return!s},lock:function(){return a=u=[],t||i||(s=t=""),this},locked:function(){return!!a},fireWith:function(e,t){return a||(t=[e,(t=t||[]).slice?t.slice():t],u.push(t),i||c()),this},fire:function(){return f.fireWith(this,arguments),this},fired:function(){return!!o}};return f},S.extend({Deferred:function(e){var o=[["notify","progress",S.Callbacks("memory"),S.Callbacks("memory"),2],["resolve","done",S.Callbacks("once memory"),S.Callbacks("once memory"),0,"resolved"],["reject","fail",S.Callbacks("once memory"),S.Callbacks("once memory"),1,"rejected"]],i="pending",a={state:function(){return i},always:function(){return s.done(arguments).fail(arguments),this},"catch":function(e){return a.then(null,e)},pipe:function(){var i=arguments;return S.Deferred(function(r){S.each(o,function(e,t){var n=m(i[t[4]])&&i[t[4]];s[t[1]](function(){var e=n&&n.apply(this,arguments);e&&m(e.promise)?e.promise().progress(r.notify).done(r.resolve).fail(r.reject):r[t[0]+"With"](this,n?[e]:arguments)})}),i=null}).promise()},then:function(t,n,r){var u=0;function l(i,o,a,s){return function(){var n=this,r=arguments,e=function(){var e,t;if(!(i<u)){if((e=a.apply(n,r))===o.promise())throw new TypeError("Thenable self-resolution");t=e&&("object"==typeof e||"function"==typeof e)&&e.then,m(t)?s?t.call(e,l(u,o,R,s),l(u,o,M,s)):(u++,t.call(e,l(u,o,R,s),l(u,o,M,s),l(u,o,R,o.notifyWith))):(a!==R&&(n=void 0,r=[e]),(s||o.resolveWith)(n,r))}},t=s?e:function(){try{e()}catch(e){S.Deferred.exceptionHook&&S.Deferred.exceptionHook(e,t.stackTrace),u<=i+1&&(a!==M&&(n=void 0,r=[e]),o.rejectWith(n,r))}};i?t():(S.Deferred.getStackHook&&(t.stackTrace=S.Deferred.getStackHook()),C.setTimeout(t))}}return S.Deferred(function(e){o[0][3].add(l(0,e,m(r)?r:R,e.notifyWith)),o[1][3].add(l(0,e,m(t)?t:R)),o[2][3].add(l(0,e,m(n)?n:M))}).promise()},promise:function(e){return null!=e?S.extend(e,a):a}},s={};return S.each(o,function(e,t){var n=t[2],r=t[5];a[t[1]]=n.add,r&&n.add(function(){i=r},o[3-e][2].disable,o[3-e][3].disable,o[0][2].lock,o[0][3].lock),n.add(t[3].fire),s[t[0]]=function(){return s[t[0]+"With"](this===s?void 0:this,arguments),this},s[t[0]+"With"]=n.fireWith}),a.promise(s),e&&e.call(s,s),s},when:function(e){var n=arguments.length,t=n,r=Array(t),i=s.call(arguments),o=S.Deferred(),a=function(t){return function(e){r[t]=this,i[t]=1<arguments.length?s.call(arguments):e,--n||o.resolveWith(r,i)}};if(n<=1&&(I(e,o.done(a(t)).resolve,o.reject,!n),"pending"===o.state()||m(i[t]&&i[t].then)))return o.then();while(t--)I(i[t],a(t),o.reject);return o.promise()}});var W=/^(Eval|Internal|Range|Reference|Syntax|Type|URI)Error$/;S.Deferred.exceptionHook=function(e,t){C.console&&C.console.warn&&e&&W.test(e.name)&&C.console.warn("jQuery.Deferred exception: "+e.message,e.stack,t)},S.readyException=function(e){C.setTimeout(function(){throw e})};var F=S.Deferred();function B(){E.removeEventListener("DOMContentLoaded",B),C.removeEventListener("load",B),S.ready()}S.fn.ready=function(e){return F.then(e)["catch"](function(e){S.readyException(e)}),this},S.extend({isReady:!1,readyWait:1,ready:function(e){(!0===e?--S.readyWait:S.isReady)||(S.isReady=!0)!==e&&0<--S.readyWait||F.resolveWith(E,[S])}}),S.ready.then=F.then,"complete"===E.readyState||"loading"!==E.readyState&&!E.documentElement.doScroll?C.setTimeout(S.ready):(E.addEventListener("DOMContentLoaded",B),C.addEventListener("load",B));var $=function(e,t,n,r,i,o,a){var s=0,u=e.length,l=null==n;if("object"===w(n))for(s in i=!0,n)$(e,t,s,n[s],!0,o,a);else if(void 0!==r&&(i=!0,m(r)||(a=!0),l&&(a?(t.call(e,r),t=null):(l=t,t=function(e,t,n){return l.call(S(e),n)})),t))for(;s<u;s++)t(e[s],n,a?r:r.call(e[s],s,t(e[s],n)));return i?e:l?t.call(e):u?t(e[0],n):o},_=/^-ms-/,z=/-([a-z])/g;function U(e,t){return t.toUpperCase()}function X(e){return e.replace(_,"ms-").replace(z,U)}var V=function(e){return 1===e.nodeType||9===e.nodeType||!+e.nodeType};function G(){this.expando=S.expando+G.uid++}G.uid=1,G.prototype={cache:function(e){var t=e[this.expando];return t||(t={},V(e)&&(e.nodeType?e[this.expando]=t:Object.defineProperty(e,this.expando,{value:t,configurable:!0}))),t},set:function(e,t,n){var r,i=this.cache(e);if("string"==typeof t)i[X(t)]=n;else for(r in t)i[X(r)]=t[r];return i},get:function(e,t){return void 0===t?this.cache(e):e[this.expando]&&e[this.expando][X(t)]},access:function(e,t,n){return void 0===t||t&&"string"==typeof t&&void 0===n?this.get(e,t):(this.set(e,t,n),void 0!==n?n:t)},remove:function(e,t){var n,r=e[this.expando];if(void 0!==r){if(void 0!==t){n=(t=Array.isArray(t)?t.map(X):(t=X(t))in r?[t]:t.match(P)||[]).length;while(n--)delete r[t[n]]}(void 0===t||S.isEmptyObject(r))&&(e.nodeType?e[this.expando]=void 0:delete e[this.expando])}},hasData:function(e){var t=e[this.expando];return void 0!==t&&!S.isEmptyObject(t)}};var Y=new G,Q=new G,J=/^(?:\{[\w\W]*\}|\[[\w\W]*\])$/,K=/[A-Z]/g;function Z(e,t,n){var r,i;if(void 0===n&&1===e.nodeType)if(r="data-"+t.replace(K,"-$&").toLowerCase(),"string"==typeof(n=e.getAttribute(r))){try{n="true"===(i=n)||"false"!==i&&("null"===i?null:i===+i+""?+i:J.test(i)?JSON.parse(i):i)}catch(e){}Q.set(e,t,n)}else n=void 0;return n}S.extend({hasData:function(e){return Q.hasData(e)||Y.hasData(e)},data:function(e,t,n){return Q.access(e,t,n)},removeData:function(e,t){Q.remove(e,t)},_data:function(e,t,n){return Y.access(e,t,n)},_removeData:function(e,t){Y.remove(e,t)}}),S.fn.extend({data:function(n,e){var t,r,i,o=this[0],a=o&&o.attributes;if(void 0===n){if(this.length&&(i=Q.get(o),1===o.nodeType&&!Y.get(o,"hasDataAttrs"))){t=a.length;while(t--)a[t]&&0===(r=a[t].name).indexOf("data-")&&(r=X(r.slice(5)),Z(o,r,i[r]));Y.set(o,"hasDataAttrs",!0)}return i}return"object"==typeof n?this.each(function(){Q.set(this,n)}):$(this,function(e){var t;if(o&&void 0===e)return void 0!==(t=Q.get(o,n))?t:void 0!==(t=Z(o,n))?t:void 0;this.each(function(){Q.set(this,n,e)})},null,e,1<arguments.length,null,!0)},removeData:function(e){return this.each(function(){Q.remove(this,e)})}}),S.extend({queue:function(e,t,n){var r;if(e)return t=(t||"fx")+"queue",r=Y.get(e,t),n&&(!r||Array.isArray(n)?r=Y.access(e,t,S.makeArray(n)):r.push(n)),r||[]},dequeue:function(e,t){t=t||"fx";var n=S.queue(e,t),r=n.length,i=n.shift(),o=S._queueHooks(e,t);"inprogress"===i&&(i=n.shift(),r--),i&&("fx"===t&&n.unshift("inprogress"),delete o.stop,i.call(e,function(){S.dequeue(e,t)},o)),!r&&o&&o.empty.fire()},_queueHooks:function(e,t){var n=t+"queueHooks";return Y.get(e,n)||Y.access(e,n,{empty:S.Callbacks("once memory").add(function(){Y.remove(e,[t+"queue",n])})})}}),S.fn.extend({queue:function(t,n){var e=2;return"string"!=typeof t&&(n=t,t="fx",e--),arguments.length<e?S.queue(this[0],t):void 0===n?this:this.each(function(){var e=S.queue(this,t,n);S._queueHooks(this,t),"fx"===t&&"inprogress"!==e[0]&&S.dequeue(this,t)})},dequeue:function(e){return this.each(function(){S.dequeue(this,e)})},clearQueue:function(e){return this.queue(e||"fx",[])},promise:function(e,t){var n,r=1,i=S.Deferred(),o=this,a=this.length,s=function(){--r||i.resolveWith(o,[o])};"string"!=typeof e&&(t=e,e=void 0),e=e||"fx";while(a--)(n=Y.get(o[a],e+"queueHooks"))&&n.empty&&(r++,n.empty.add(s));return s(),i.promise(t)}});var ee=/[+-]?(?:\d*\.|)\d+(?:[eE][+-]?\d+|)/.source,te=new RegExp("^(?:([+-])=|)("+ee+")([a-z%]*)$","i"),ne=["Top","Right","Bottom","Left"],re=E.documentElement,ie=function(e){return S.contains(e.ownerDocument,e)},oe={composed:!0};re.getRootNode&&(ie=function(e){return S.contains(e.ownerDocument,e)||e.getRootNode(oe)===e.ownerDocument});var ae=function(e,t){return"none"===(e=t||e).style.display||""===e.style.display&&ie(e)&&"none"===S.css(e,"display")};function se(e,t,n,r){var i,o,a=20,s=r?function(){return r.cur()}:function(){return S.css(e,t,"")},u=s(),l=n&&n[3]||(S.cssNumber[t]?"":"px"),c=e.nodeType&&(S.cssNumber[t]||"px"!==l&&+u)&&te.exec(S.css(e,t));if(c&&c[3]!==l){u/=2,l=l||c[3],c=+u||1;while(a--)S.style(e,t,c+l),(1-o)*(1-(o=s()/u||.5))<=0&&(a=0),c/=o;c*=2,S.style(e,t,c+l),n=n||[]}return n&&(c=+c||+u||0,i=n[1]?c+(n[1]+1)*n[2]:+n[2],r&&(r.unit=l,r.start=c,r.end=i)),i}var ue={};function le(e,t){for(var n,r,i,o,a,s,u,l=[],c=0,f=e.length;c<f;c++)(r=e[c]).style&&(n=r.style.display,t?("none"===n&&(l[c]=Y.get(r,"display")||null,l[c]||(r.style.display="")),""===r.style.display&&ae(r)&&(l[c]=(u=a=o=void 0,a=(i=r).ownerDocument,s=i.nodeName,(u=ue[s])||(o=a.body.appendChild(a.createElement(s)),u=S.css(o,"display"),o.parentNode.removeChild(o),"none"===u&&(u="block"),ue[s]=u)))):"none"!==n&&(l[c]="none",Y.set(r,"display",n)));for(c=0;c<f;c++)null!=l[c]&&(e[c].style.display=l[c]);return e}S.fn.extend({show:function(){return le(this,!0)},hide:function(){return le(this)},toggle:function(e){return"boolean"==typeof e?e?this.show():this.hide():this.each(function(){ae(this)?S(this).show():S(this).hide()})}});var ce,fe,pe=/^(?:checkbox|radio)$/i,de=/<([a-z][^\/\0>\x20\t\r\n\f]*)/i,he=/^$|^module$|\/(?:java|ecma)script/i;ce=E.createDocumentFragment().appendChild(E.createElement("div")),(fe=E.createElement("input")).setAttribute("type","radio"),fe.setAttribute("checked","checked"),fe.setAttribute("name","t"),ce.appendChild(fe),y.checkClone=ce.cloneNode(!0).cloneNode(!0).lastChild.checked,ce.innerHTML="<textarea>x</textarea>",y.noCloneChecked=!!ce.cloneNode(!0).lastChild.defaultValue,ce.innerHTML="<option></option>",y.option=!!ce.lastChild;var ge={thead:[1,"<table>","</table>"],col:[2,"<table><colgroup>","</colgroup></table>"],tr:[2,"<table><tbody>","</tbody></table>"],td:[3,"<table><tbody><tr>","</tr></tbody></table>"],_default:[0,"",""]};function ve(e,t){var n;return n="undefined"!=typeof e.getElementsByTagName?e.getElementsByTagName(t||"*"):"undefined"!=typeof e.querySelectorAll?e.querySelectorAll(t||"*"):[],void 0===t||t&&A(e,t)?S.merge([e],n):n}function ye(e,t){for(var n=0,r=e.length;n<r;n++)Y.set(e[n],"globalEval",!t||Y.get(t[n],"globalEval"))}ge.tbody=ge.tfoot=ge.colgroup=ge.caption=ge.thead,ge.th=ge.td,y.option||(ge.optgroup=ge.option=[1,"<select multiple='multiple'>","</select>"]);var me=/<|&#?\w+;/;function xe(e,t,n,r,i){for(var o,a,s,u,l,c,f=t.createDocumentFragment(),p=[],d=0,h=e.length;d<h;d++)if((o=e[d])||0===o)if("object"===w(o))S.merge(p,o.nodeType?[o]:o);else if(me.test(o)){a=a||f.appendChild(t.createElement("div")),s=(de.exec(o)||["",""])[1].toLowerCase(),u=ge[s]||ge._default,a.innerHTML=u[1]+S.htmlPrefilter(o)+u[2],c=u[0];while(c--)a=a.lastChild;S.merge(p,a.childNodes),(a=f.firstChild).textContent=""}else p.push(t.createTextNode(o));f.textContent="",d=0;while(o=p[d++])if(r&&-1<S.inArray(o,r))i&&i.push(o);else if(l=ie(o),a=ve(f.appendChild(o),"script"),l&&ye(a),n){c=0;while(o=a[c++])he.test(o.type||"")&&n.push(o)}return f}var be=/^key/,we=/^(?:mouse|pointer|contextmenu|drag|drop)|click/,Te=/^([^.]*)(?:\.(.+)|)/;function Ce(){return!0}function Ee(){return!1}function Se(e,t){return e===function(){try{return E.activeElement}catch(e){}}()==("focus"===t)}function ke(e,t,n,r,i,o){var a,s;if("object"==typeof t){for(s in"string"!=typeof n&&(r=r||n,n=void 0),t)ke(e,s,n,r,t[s],o);return e}if(null==r&&null==i?(i=n,r=n=void 0):null==i&&("string"==typeof n?(i=r,r=void 0):(i=r,r=n,n=void 0)),!1===i)i=Ee;else if(!i)return e;return 1===o&&(a=i,(i=function(e){return S().off(e),a.apply(this,arguments)}).guid=a.guid||(a.guid=S.guid++)),e.each(function(){S.event.add(this,t,i,r,n)})}function Ae(e,i,o){o?(Y.set(e,i,!1),S.event.add(e,i,{namespace:!1,handler:function(e){var t,n,r=Y.get(this,i);if(1&e.isTrigger&&this[i]){if(r.length)(S.event.special[i]||{}).delegateType&&e.stopPropagation();else if(r=s.call(arguments),Y.set(this,i,r),t=o(this,i),this[i](),r!==(n=Y.get(this,i))||t?Y.set(this,i,!1):n={},r!==n)return e.stopImmediatePropagation(),e.preventDefault(),n.value}else r.length&&(Y.set(this,i,{value:S.event.trigger(S.extend(r[0],S.Event.prototype),r.slice(1),this)}),e.stopImmediatePropagation())}})):void 0===Y.get(e,i)&&S.event.add(e,i,Ce)}S.event={global:{},add:function(t,e,n,r,i){var o,a,s,u,l,c,f,p,d,h,g,v=Y.get(t);if(V(t)){n.handler&&(n=(o=n).handler,i=o.selector),i&&S.find.matchesSelector(re,i),n.guid||(n.guid=S.guid++),(u=v.events)||(u=v.events=Object.create(null)),(a=v.handle)||(a=v.handle=function(e){return"undefined"!=typeof S&&S.event.triggered!==e.type?S.event.dispatch.apply(t,arguments):void 0}),l=(e=(e||"").match(P)||[""]).length;while(l--)d=g=(s=Te.exec(e[l])||[])[1],h=(s[2]||"").split(".").sort(),d&&(f=S.event.special[d]||{},d=(i?f.delegateType:f.bindType)||d,f=S.event.special[d]||{},c=S.extend({type:d,origType:g,data:r,handler:n,guid:n.guid,selector:i,needsContext:i&&S.expr.match.needsContext.test(i),namespace:h.join(".")},o),(p=u[d])||((p=u[d]=[]).delegateCount=0,f.setup&&!1!==f.setup.call(t,r,h,a)||t.addEventListener&&t.addEventListener(d,a)),f.add&&(f.add.call(t,c),c.handler.guid||(c.handler.guid=n.guid)),i?p.splice(p.delegateCount++,0,c):p.push(c),S.event.global[d]=!0)}},remove:function(e,t,n,r,i){var o,a,s,u,l,c,f,p,d,h,g,v=Y.hasData(e)&&Y.get(e);if(v&&(u=v.events)){l=(t=(t||"").match(P)||[""]).length;while(l--)if(d=g=(s=Te.exec(t[l])||[])[1],h=(s[2]||"").split(".").sort(),d){f=S.event.special[d]||{},p=u[d=(r?f.delegateType:f.bindType)||d]||[],s=s[2]&&new RegExp("(^|\\.)"+h.join("\\.(?:.*\\.|)")+"(\\.|$)"),a=o=p.length;while(o--)c=p[o],!i&&g!==c.origType||n&&n.guid!==c.guid||s&&!s.test(c.namespace)||r&&r!==c.selector&&("**"!==r||!c.selector)||(p.splice(o,1),c.selector&&p.delegateCount--,f.remove&&f.remove.call(e,c));a&&!p.length&&(f.teardown&&!1!==f.teardown.call(e,h,v.handle)||S.removeEvent(e,d,v.handle),delete u[d])}else for(d in u)S.event.remove(e,d+t[l],n,r,!0);S.isEmptyObject(u)&&Y.remove(e,"handle events")}},dispatch:function(e){var t,n,r,i,o,a,s=new Array(arguments.length),u=S.event.fix(e),l=(Y.get(this,"events")||Object.create(null))[u.type]||[],c=S.event.special[u.type]||{};for(s[0]=u,t=1;t<arguments.length;t++)s[t]=arguments[t];if(u.delegateTarget=this,!c.preDispatch||!1!==c.preDispatch.call(this,u)){a=S.event.handlers.call(this,u,l),t=0;while((i=a[t++])&&!u.isPropagationStopped()){u.currentTarget=i.elem,n=0;while((o=i.handlers[n++])&&!u.isImmediatePropagationStopped())u.rnamespace&&!1!==o.namespace&&!u.rnamespace.test(o.namespace)||(u.handleObj=o,u.data=o.data,void 0!==(r=((S.event.special[o.origType]||{}).handle||o.handler).apply(i.elem,s))&&!1===(u.result=r)&&(u.preventDefault(),u.stopPropagation()))}return c.postDispatch&&c.postDispatch.call(this,u),u.result}},handlers:function(e,t){var n,r,i,o,a,s=[],u=t.delegateCount,l=e.target;if(u&&l.nodeType&&!("click"===e.type&&1<=e.button))for(;l!==this;l=l.parentNode||this)if(1===l.nodeType&&("click"!==e.type||!0!==l.disabled)){for(o=[],a={},n=0;n<u;n++)void 0===a[i=(r=t[n]).selector+" "]&&(a[i]=r.needsContext?-1<S(i,this).index(l):S.find(i,this,null,[l]).length),a[i]&&o.push(r);o.length&&s.push({elem:l,handlers:o})}return l=this,u<t.length&&s.push({elem:l,handlers:t.slice(u)}),s},addProp:function(t,e){Object.defineProperty(S.Event.prototype,t,{enumerable:!0,configurable:!0,get:m(e)?function(){if(this.originalEvent)return e(this.originalEvent)}:function(){if(this.originalEvent)return this.originalEvent[t]},set:function(e){Object.defineProperty(this,t,{enumerable:!0,configurable:!0,writable:!0,value:e})}})},fix:function(e){return e[S.expando]?e:new S.Event(e)},special:{load:{noBubble:!0},click:{setup:function(e){var t=this||e;return pe.test(t.type)&&t.click&&A(t,"input")&&Ae(t,"click",Ce),!1},trigger:function(e){var t=this||e;return pe.test(t.type)&&t.click&&A(t,"input")&&Ae(t,"click"),!0},_default:function(e){var t=e.target;return pe.test(t.type)&&t.click&&A(t,"input")&&Y.get(t,"click")||A(t,"a")}},beforeunload:{postDispatch:function(e){void 0!==e.result&&e.originalEvent&&(e.originalEvent.returnValue=e.result)}}}},S.removeEvent=function(e,t,n){e.removeEventListener&&e.removeEventListener(t,n)},S.Event=function(e,t){if(!(this instanceof S.Event))return new S.Event(e,t);e&&e.type?(this.originalEvent=e,this.type=e.type,this.isDefaultPrevented=e.defaultPrevented||void 0===e.defaultPrevented&&!1===e.returnValue?Ce:Ee,this.target=e.target&&3===e.target.nodeType?e.target.parentNode:e.target,this.currentTarget=e.currentTarget,this.relatedTarget=e.relatedTarget):this.type=e,t&&S.extend(this,t),this.timeStamp=e&&e.timeStamp||Date.now(),this[S.expando]=!0},S.Event.prototype={constructor:S.Event,isDefaultPrevented:Ee,isPropagationStopped:Ee,isImmediatePropagationStopped:Ee,isSimulated:!1,preventDefault:function(){var e=this.originalEvent;this.isDefaultPrevented=Ce,e&&!this.isSimulated&&e.preventDefault()},stopPropagation:function(){var e=this.originalEvent;this.isPropagationStopped=Ce,e&&!this.isSimulated&&e.stopPropagation()},stopImmediatePropagation:function(){var e=this.originalEvent;this.isImmediatePropagationStopped=Ce,e&&!this.isSimulated&&e.stopImmediatePropagation(),this.stopPropagation()}},S.each({altKey:!0,bubbles:!0,cancelable:!0,changedTouches:!0,ctrlKey:!0,detail:!0,eventPhase:!0,metaKey:!0,pageX:!0,pageY:!0,shiftKey:!0,view:!0,"char":!0,code:!0,charCode:!0,key:!0,keyCode:!0,button:!0,buttons:!0,clientX:!0,clientY:!0,offsetX:!0,offsetY:!0,pointerId:!0,pointerType:!0,screenX:!0,screenY:!0,targetTouches:!0,toElement:!0,touches:!0,which:function(e){var t=e.button;return null==e.which&&be.test(e.type)?null!=e.charCode?e.charCode:e.keyCode:!e.which&&void 0!==t&&we.test(e.type)?1&t?1:2&t?3:4&t?2:0:e.which}},S.event.addProp),S.each({focus:"focusin",blur:"focusout"},function(e,t){S.event.special[e]={setup:function(){return Ae(this,e,Se),!1},trigger:function(){return Ae(this,e),!0},delegateType:t}}),S.each({mouseenter:"mouseover",mouseleave:"mouseout",pointerenter:"pointerover",pointerleave:"pointerout"},function(e,i){S.event.special[e]={delegateType:i,bindType:i,handle:function(e){var t,n=e.relatedTarget,r=e.handleObj;return n&&(n===this||S.contains(this,n))||(e.type=r.origType,t=r.handler.apply(this,arguments),e.type=i),t}}}),S.fn.extend({on:function(e,t,n,r){return ke(this,e,t,n,r)},one:function(e,t,n,r){return ke(this,e,t,n,r,1)},off:function(e,t,n){var r,i;if(e&&e.preventDefault&&e.handleObj)return r=e.handleObj,S(e.delegateTarget).off(r.namespace?r.origType+"."+r.namespace:r.origType,r.selector,r.handler),this;if("object"==typeof e){for(i in e)this.off(i,t,e[i]);return this}return!1!==t&&"function"!=typeof t||(n=t,t=void 0),!1===n&&(n=Ee),this.each(function(){S.event.remove(this,e,n,t)})}});var Ne=/<script|<style|<link/i,De=/checked\s*(?:[^=]|=\s*.checked.)/i,je=/^\s*<!(?:\[CDATA\[|--)|(?:\]\]|--)>\s*$/g;function qe(e,t){return A(e,"table")&&A(11!==t.nodeType?t:t.firstChild,"tr")&&S(e).children("tbody")[0]||e}function Le(e){return e.type=(null!==e.getAttribute("type"))+"/"+e.type,e}function He(e){return"true/"===(e.type||"").slice(0,5)?e.type=e.type.slice(5):e.removeAttribute("type"),e}function Oe(e,t){var n,r,i,o,a,s;if(1===t.nodeType){if(Y.hasData(e)&&(s=Y.get(e).events))for(i in Y.remove(t,"handle events"),s)for(n=0,r=s[i].length;n<r;n++)S.event.add(t,i,s[i][n]);Q.hasData(e)&&(o=Q.access(e),a=S.extend({},o),Q.set(t,a))}}function Pe(n,r,i,o){r=g(r);var e,t,a,s,u,l,c=0,f=n.length,p=f-1,d=r[0],h=m(d);if(h||1<f&&"string"==typeof d&&!y.checkClone&&De.test(d))return n.each(function(e){var t=n.eq(e);h&&(r[0]=d.call(this,e,t.html())),Pe(t,r,i,o)});if(f&&(t=(e=xe(r,n[0].ownerDocument,!1,n,o)).firstChild,1===e.childNodes.length&&(e=t),t||o)){for(s=(a=S.map(ve(e,"script"),Le)).length;c<f;c++)u=e,c!==p&&(u=S.clone(u,!0,!0),s&&S.merge(a,ve(u,"script"))),i.call(n[c],u,c);if(s)for(l=a[a.length-1].ownerDocument,S.map(a,He),c=0;c<s;c++)u=a[c],he.test(u.type||"")&&!Y.access(u,"globalEval")&&S.contains(l,u)&&(u.src&&"module"!==(u.type||"").toLowerCase()?S._evalUrl&&!u.noModule&&S._evalUrl(u.src,{nonce:u.nonce||u.getAttribute("nonce")},l):b(u.textContent.replace(je,""),u,l))}return n}function Re(e,t,n){for(var r,i=t?S.filter(t,e):e,o=0;null!=(r=i[o]);o++)n||1!==r.nodeType||S.cleanData(ve(r)),r.parentNode&&(n&&ie(r)&&ye(ve(r,"script")),r.parentNode.removeChild(r));return e}S.extend({htmlPrefilter:function(e){return e},clone:function(e,t,n){var r,i,o,a,s,u,l,c=e.cloneNode(!0),f=ie(e);if(!(y.noCloneChecked||1!==e.nodeType&&11!==e.nodeType||S.isXMLDoc(e)))for(a=ve(c),r=0,i=(o=ve(e)).length;r<i;r++)s=o[r],u=a[r],void 0,"input"===(l=u.nodeName.toLowerCase())&&pe.test(s.type)?u.checked=s.checked:"input"!==l&&"textarea"!==l||(u.defaultValue=s.defaultValue);if(t)if(n)for(o=o||ve(e),a=a||ve(c),r=0,i=o.length;r<i;r++)Oe(o[r],a[r]);else Oe(e,c);return 0<(a=ve(c,"script")).length&&ye(a,!f&&ve(e,"script")),c},cleanData:function(e){for(var t,n,r,i=S.event.special,o=0;void 0!==(n=e[o]);o++)if(V(n)){if(t=n[Y.expando]){if(t.events)for(r in t.events)i[r]?S.event.remove(n,r):S.removeEvent(n,r,t.handle);n[Y.expando]=void 0}n[Q.expando]&&(n[Q.expando]=void 0)}}}),S.fn.extend({detach:function(e){return Re(this,e,!0)},remove:function(e){return Re(this,e)},text:function(e){return $(this,function(e){return void 0===e?S.text(this):this.empty().each(function(){1!==this.nodeType&&11!==this.nodeType&&9!==this.nodeType||(this.textContent=e)})},null,e,arguments.length)},append:function(){return Pe(this,arguments,function(e){1!==this.nodeType&&11!==this.nodeType&&9!==this.nodeType||qe(this,e).appendChild(e)})},prepend:function(){return Pe(this,arguments,function(e){if(1===this.nodeType||11===this.nodeType||9===this.nodeType){var t=qe(this,e);t.insertBefore(e,t.firstChild)}})},before:function(){return Pe(this,arguments,function(e){this.parentNode&&this.parentNode.insertBefore(e,this)})},after:function(){return Pe(this,arguments,function(e){this.parentNode&&this.parentNode.insertBefore(e,this.nextSibling)})},empty:function(){for(var e,t=0;null!=(e=this[t]);t++)1===e.nodeType&&(S.cleanData(ve(e,!1)),e.textContent="");return this},clone:function(e,t){return e=null!=e&&e,t=null==t?e:t,this.map(function(){return S.clone(this,e,t)})},html:function(e){return $(this,function(e){var t=this[0]||{},n=0,r=this.length;if(void 0===e&&1===t.nodeType)return t.innerHTML;if("string"==typeof e&&!Ne.test(e)&&!ge[(de.exec(e)||["",""])[1].toLowerCase()]){e=S.htmlPrefilter(e);try{for(;n<r;n++)1===(t=this[n]||{}).nodeType&&(S.cleanData(ve(t,!1)),t.innerHTML=e);t=0}catch(e){}}t&&this.empty().append(e)},null,e,arguments.length)},replaceWith:function(){var n=[];return Pe(this,arguments,function(e){var t=this.parentNode;S.inArray(this,n)<0&&(S.cleanData(ve(this)),t&&t.replaceChild(e,this))},n)}}),S.each({appendTo:"append",prependTo:"prepend",insertBefore:"before",insertAfter:"after",replaceAll:"replaceWith"},function(e,a){S.fn[e]=function(e){for(var t,n=[],r=S(e),i=r.length-1,o=0;o<=i;o++)t=o===i?this:this.clone(!0),S(r[o])[a](t),u.apply(n,t.get());return this.pushStack(n)}});var Me=new RegExp("^("+ee+")(?!px)[a-z%]+$","i"),Ie=function(e){var t=e.ownerDocument.defaultView;return t&&t.opener||(t=C),t.getComputedStyle(e)},We=function(e,t,n){var r,i,o={};for(i in t)o[i]=e.style[i],e.style[i]=t[i];for(i in r=n.call(e),t)e.style[i]=o[i];return r},Fe=new RegExp(ne.join("|"),"i");function Be(e,t,n){var r,i,o,a,s=e.style;return(n=n||Ie(e))&&(""!==(a=n.getPropertyValue(t)||n[t])||ie(e)||(a=S.style(e,t)),!y.pixelBoxStyles()&&Me.test(a)&&Fe.test(t)&&(r=s.width,i=s.minWidth,o=s.maxWidth,s.minWidth=s.maxWidth=s.width=a,a=n.width,s.width=r,s.minWidth=i,s.maxWidth=o)),void 0!==a?a+"":a}function $e(e,t){return{get:function(){if(!e())return(this.get=t).apply(this,arguments);delete this.get}}}!function(){function e(){if(l){u.style.cssText="position:absolute;left:-11111px;width:60px;margin-top:1px;padding:0;border:0",l.style.cssText="position:relative;display:block;box-sizing:border-box;overflow:scroll;margin:auto;border:1px;padding:1px;width:60%;top:1%",re.appendChild(u).appendChild(l);var e=C.getComputedStyle(l);n="1%"!==e.top,s=12===t(e.marginLeft),l.style.right="60%",o=36===t(e.right),r=36===t(e.width),l.style.position="absolute",i=12===t(l.offsetWidth/3),re.removeChild(u),l=null}}function t(e){return Math.round(parseFloat(e))}var n,r,i,o,a,s,u=E.createElement("div"),l=E.createElement("div");l.style&&(l.style.backgroundClip="content-box",l.cloneNode(!0).style.backgroundClip="",y.clearCloneStyle="content-box"===l.style.backgroundClip,S.extend(y,{boxSizingReliable:function(){return e(),r},pixelBoxStyles:function(){return e(),o},pixelPosition:function(){return e(),n},reliableMarginLeft:function(){return e(),s},scrollboxSize:function(){return e(),i},reliableTrDimensions:function(){var e,t,n,r;return null==a&&(e=E.createElement("table"),t=E.createElement("tr"),n=E.createElement("div"),e.style.cssText="position:absolute;left:-11111px",t.style.height="1px",n.style.height="9px",re.appendChild(e).appendChild(t).appendChild(n),r=C.getComputedStyle(t),a=3<parseInt(r.height),re.removeChild(e)),a}}))}();var _e=["Webkit","Moz","ms"],ze=E.createElement("div").style,Ue={};function Xe(e){var t=S.cssProps[e]||Ue[e];return t||(e in ze?e:Ue[e]=function(e){var t=e[0].toUpperCase()+e.slice(1),n=_e.length;while(n--)if((e=_e[n]+t)in ze)return e}(e)||e)}var Ve=/^(none|table(?!-c[ea]).+)/,Ge=/^--/,Ye={position:"absolute",visibility:"hidden",display:"block"},Qe={letterSpacing:"0",fontWeight:"400"};function Je(e,t,n){var r=te.exec(t);return r?Math.max(0,r[2]-(n||0))+(r[3]||"px"):t}function Ke(e,t,n,r,i,o){var a="width"===t?1:0,s=0,u=0;if(n===(r?"border":"content"))return 0;for(;a<4;a+=2)"margin"===n&&(u+=S.css(e,n+ne[a],!0,i)),r?("content"===n&&(u-=S.css(e,"padding"+ne[a],!0,i)),"margin"!==n&&(u-=S.css(e,"border"+ne[a]+"Width",!0,i))):(u+=S.css(e,"padding"+ne[a],!0,i),"padding"!==n?u+=S.css(e,"border"+ne[a]+"Width",!0,i):s+=S.css(e,"border"+ne[a]+"Width",!0,i));return!r&&0<=o&&(u+=Math.max(0,Math.ceil(e["offset"+t[0].toUpperCase()+t.slice(1)]-o-u-s-.5))||0),u}function Ze(e,t,n){var r=Ie(e),i=(!y.boxSizingReliable()||n)&&"border-box"===S.css(e,"boxSizing",!1,r),o=i,a=Be(e,t,r),s="offset"+t[0].toUpperCase()+t.slice(1);if(Me.test(a)){if(!n)return a;a="auto"}return(!y.boxSizingReliable()&&i||!y.reliableTrDimensions()&&A(e,"tr")||"auto"===a||!parseFloat(a)&&"inline"===S.css(e,"display",!1,r))&&e.getClientRects().length&&(i="border-box"===S.css(e,"boxSizing",!1,r),(o=s in e)&&(a=e[s])),(a=parseFloat(a)||0)+Ke(e,t,n||(i?"border":"content"),o,r,a)+"px"}function et(e,t,n,r,i){return new et.prototype.init(e,t,n,r,i)}S.extend({cssHooks:{opacity:{get:function(e,t){if(t){var n=Be(e,"opacity");return""===n?"1":n}}}},cssNumber:{animationIterationCount:!0,columnCount:!0,fillOpacity:!0,flexGrow:!0,flexShrink:!0,fontWeight:!0,gridArea:!0,gridColumn:!0,gridColumnEnd:!0,gridColumnStart:!0,gridRow:!0,gridRowEnd:!0,gridRowStart:!0,lineHeight:!0,opacity:!0,order:!0,orphans:!0,widows:!0,zIndex:!0,zoom:!0},cssProps:{},style:function(e,t,n,r){if(e&&3!==e.nodeType&&8!==e.nodeType&&e.style){var i,o,a,s=X(t),u=Ge.test(t),l=e.style;if(u||(t=Xe(s)),a=S.cssHooks[t]||S.cssHooks[s],void 0===n)return a&&"get"in a&&void 0!==(i=a.get(e,!1,r))?i:l[t];"string"===(o=typeof n)&&(i=te.exec(n))&&i[1]&&(n=se(e,t,i),o="number"),null!=n&&n==n&&("number"!==o||u||(n+=i&&i[3]||(S.cssNumber[s]?"":"px")),y.clearCloneStyle||""!==n||0!==t.indexOf("background")||(l[t]="inherit"),a&&"set"in a&&void 0===(n=a.set(e,n,r))||(u?l.setProperty(t,n):l[t]=n))}},css:function(e,t,n,r){var i,o,a,s=X(t);return Ge.test(t)||(t=Xe(s)),(a=S.cssHooks[t]||S.cssHooks[s])&&"get"in a&&(i=a.get(e,!0,n)),void 0===i&&(i=Be(e,t,r)),"normal"===i&&t in Qe&&(i=Qe[t]),""===n||n?(o=parseFloat(i),!0===n||isFinite(o)?o||0:i):i}}),S.each(["height","width"],function(e,u){S.cssHooks[u]={get:function(e,t,n){if(t)return!Ve.test(S.css(e,"display"))||e.getClientRects().length&&e.getBoundingClientRect().width?Ze(e,u,n):We(e,Ye,function(){return Ze(e,u,n)})},set:function(e,t,n){var r,i=Ie(e),o=!y.scrollboxSize()&&"absolute"===i.position,a=(o||n)&&"border-box"===S.css(e,"boxSizing",!1,i),s=n?Ke(e,u,n,a,i):0;return a&&o&&(s-=Math.ceil(e["offset"+u[0].toUpperCase()+u.slice(1)]-parseFloat(i[u])-Ke(e,u,"border",!1,i)-.5)),s&&(r=te.exec(t))&&"px"!==(r[3]||"px")&&(e.style[u]=t,t=S.css(e,u)),Je(0,t,s)}}}),S.cssHooks.marginLeft=$e(y.reliableMarginLeft,function(e,t){if(t)return(parseFloat(Be(e,"marginLeft"))||e.getBoundingClientRect().left-We(e,{marginLeft:0},function(){return e.getBoundingClientRect().left}))+"px"}),S.each({margin:"",padding:"",border:"Width"},function(i,o){S.cssHooks[i+o]={expand:function(e){for(var t=0,n={},r="string"==typeof e?e.split(" "):[e];t<4;t++)n[i+ne[t]+o]=r[t]||r[t-2]||r[0];return n}},"margin"!==i&&(S.cssHooks[i+o].set=Je)}),S.fn.extend({css:function(e,t){return $(this,function(e,t,n){var r,i,o={},a=0;if(Array.isArray(t)){for(r=Ie(e),i=t.length;a<i;a++)o[t[a]]=S.css(e,t[a],!1,r);return o}return void 0!==n?S.style(e,t,n):S.css(e,t)},e,t,1<arguments.length)}}),((S.Tween=et).prototype={constructor:et,init:function(e,t,n,r,i,o){this.elem=e,this.prop=n,this.easing=i||S.easing._default,this.options=t,this.start=this.now=this.cur(),this.end=r,this.unit=o||(S.cssNumber[n]?"":"px")},cur:function(){var e=et.propHooks[this.prop];return e&&e.get?e.get(this):et.propHooks._default.get(this)},run:function(e){var t,n=et.propHooks[this.prop];return this.options.duration?this.pos=t=S.easing[this.easing](e,this.options.duration*e,0,1,this.options.duration):this.pos=t=e,this.now=(this.end-this.start)*t+this.start,this.options.step&&this.options.step.call(this.elem,this.now,this),n&&n.set?n.set(this):et.propHooks._default.set(this),this}}).init.prototype=et.prototype,(et.propHooks={_default:{get:function(e){var t;return 1!==e.elem.nodeType||null!=e.elem[e.prop]&&null==e.elem.style[e.prop]?e.elem[e.prop]:(t=S.css(e.elem,e.prop,""))&&"auto"!==t?t:0},set:function(e){S.fx.step[e.prop]?S.fx.step[e.prop](e):1!==e.elem.nodeType||!S.cssHooks[e.prop]&&null==e.elem.style[Xe(e.prop)]?e.elem[e.prop]=e.now:S.style(e.elem,e.prop,e.now+e.unit)}}}).scrollTop=et.propHooks.scrollLeft={set:function(e){e.elem.nodeType&&e.elem.parentNode&&(e.elem[e.prop]=e.now)}},S.easing={linear:function(e){return e},swing:function(e){return.5-Math.cos(e*Math.PI)/2},_default:"swing"},S.fx=et.prototype.init,S.fx.step={};var tt,nt,rt,it,ot=/^(?:toggle|show|hide)$/,at=/queueHooks$/;function st(){nt&&(!1===E.hidden&&C.requestAnimationFrame?C.requestAnimationFrame(st):C.setTimeout(st,S.fx.interval),S.fx.tick())}function ut(){return C.setTimeout(function(){tt=void 0}),tt=Date.now()}function lt(e,t){var n,r=0,i={height:e};for(t=t?1:0;r<4;r+=2-t)i["margin"+(n=ne[r])]=i["padding"+n]=e;return t&&(i.opacity=i.width=e),i}function ct(e,t,n){for(var r,i=(ft.tweeners[t]||[]).concat(ft.tweeners["*"]),o=0,a=i.length;o<a;o++)if(r=i[o].call(n,t,e))return r}function ft(o,e,t){var n,a,r=0,i=ft.prefilters.length,s=S.Deferred().always(function(){delete u.elem}),u=function(){if(a)return!1;for(var e=tt||ut(),t=Math.max(0,l.startTime+l.duration-e),n=1-(t/l.duration||0),r=0,i=l.tweens.length;r<i;r++)l.tweens[r].run(n);return s.notifyWith(o,[l,n,t]),n<1&&i?t:(i||s.notifyWith(o,[l,1,0]),s.resolveWith(o,[l]),!1)},l=s.promise({elem:o,props:S.extend({},e),opts:S.extend(!0,{specialEasing:{},easing:S.easing._default},t),originalProperties:e,originalOptions:t,startTime:tt||ut(),duration:t.duration,tweens:[],createTween:function(e,t){var n=S.Tween(o,l.opts,e,t,l.opts.specialEasing[e]||l.opts.easing);return l.tweens.push(n),n},stop:function(e){var t=0,n=e?l.tweens.length:0;if(a)return this;for(a=!0;t<n;t++)l.tweens[t].run(1);return e?(s.notifyWith(o,[l,1,0]),s.resolveWith(o,[l,e])):s.rejectWith(o,[l,e]),this}}),c=l.props;for(!function(e,t){var n,r,i,o,a;for(n in e)if(i=t[r=X(n)],o=e[n],Array.isArray(o)&&(i=o[1],o=e[n]=o[0]),n!==r&&(e[r]=o,delete e[n]),(a=S.cssHooks[r])&&"expand"in a)for(n in o=a.expand(o),delete e[r],o)n in e||(e[n]=o[n],t[n]=i);else t[r]=i}(c,l.opts.specialEasing);r<i;r++)if(n=ft.prefilters[r].call(l,o,c,l.opts))return m(n.stop)&&(S._queueHooks(l.elem,l.opts.queue).stop=n.stop.bind(n)),n;return S.map(c,ct,l),m(l.opts.start)&&l.opts.start.call(o,l),l.progress(l.opts.progress).done(l.opts.done,l.opts.complete).fail(l.opts.fail).always(l.opts.always),S.fx.timer(S.extend(u,{elem:o,anim:l,queue:l.opts.queue})),l}S.Animation=S.extend(ft,{tweeners:{"*":[function(e,t){var n=this.createTween(e,t);return se(n.elem,e,te.exec(t),n),n}]},tweener:function(e,t){m(e)?(t=e,e=["*"]):e=e.match(P);for(var n,r=0,i=e.length;r<i;r++)n=e[r],ft.tweeners[n]=ft.tweeners[n]||[],ft.tweeners[n].unshift(t)},prefilters:[function(e,t,n){var r,i,o,a,s,u,l,c,f="width"in t||"height"in t,p=this,d={},h=e.style,g=e.nodeType&&ae(e),v=Y.get(e,"fxshow");for(r in n.queue||(null==(a=S._queueHooks(e,"fx")).unqueued&&(a.unqueued=0,s=a.empty.fire,a.empty.fire=function(){a.unqueued||s()}),a.unqueued++,p.always(function(){p.always(function(){a.unqueued--,S.queue(e,"fx").length||a.empty.fire()})})),t)if(i=t[r],ot.test(i)){if(delete t[r],o=o||"toggle"===i,i===(g?"hide":"show")){if("show"!==i||!v||void 0===v[r])continue;g=!0}d[r]=v&&v[r]||S.style(e,r)}if((u=!S.isEmptyObject(t))||!S.isEmptyObject(d))for(r in f&&1===e.nodeType&&(n.overflow=[h.overflow,h.overflowX,h.overflowY],null==(l=v&&v.display)&&(l=Y.get(e,"display")),"none"===(c=S.css(e,"display"))&&(l?c=l:(le([e],!0),l=e.style.display||l,c=S.css(e,"display"),le([e]))),("inline"===c||"inline-block"===c&&null!=l)&&"none"===S.css(e,"float")&&(u||(p.done(function(){h.display=l}),null==l&&(c=h.display,l="none"===c?"":c)),h.display="inline-block")),n.overflow&&(h.overflow="hidden",p.always(function(){h.overflow=n.overflow[0],h.overflowX=n.overflow[1],h.overflowY=n.overflow[2]})),u=!1,d)u||(v?"hidden"in v&&(g=v.hidden):v=Y.access(e,"fxshow",{display:l}),o&&(v.hidden=!g),g&&le([e],!0),p.done(function(){for(r in g||le([e]),Y.remove(e,"fxshow"),d)S.style(e,r,d[r])})),u=ct(g?v[r]:0,r,p),r in v||(v[r]=u.start,g&&(u.end=u.start,u.start=0))}],prefilter:function(e,t){t?ft.prefilters.unshift(e):ft.prefilters.push(e)}}),S.speed=function(e,t,n){var r=e&&"object"==typeof e?S.extend({},e):{complete:n||!n&&t||m(e)&&e,duration:e,easing:n&&t||t&&!m(t)&&t};return S.fx.off?r.duration=0:"number"!=typeof r.duration&&(r.duration in S.fx.speeds?r.duration=S.fx.speeds[r.duration]:r.duration=S.fx.speeds._default),null!=r.queue&&!0!==r.queue||(r.queue="fx"),r.old=r.complete,r.complete=function(){m(r.old)&&r.old.call(this),r.queue&&S.dequeue(this,r.queue)},r},S.fn.extend({fadeTo:function(e,t,n,r){return this.filter(ae).css("opacity",0).show().end().animate({opacity:t},e,n,r)},animate:function(t,e,n,r){var i=S.isEmptyObject(t),o=S.speed(e,n,r),a=function(){var e=ft(this,S.extend({},t),o);(i||Y.get(this,"finish"))&&e.stop(!0)};return a.finish=a,i||!1===o.queue?this.each(a):this.queue(o.queue,a)},stop:function(i,e,o){var a=function(e){var t=e.stop;delete e.stop,t(o)};return"string"!=typeof i&&(o=e,e=i,i=void 0),e&&this.queue(i||"fx",[]),this.each(function(){var e=!0,t=null!=i&&i+"queueHooks",n=S.timers,r=Y.get(this);if(t)r[t]&&r[t].stop&&a(r[t]);else for(t in r)r[t]&&r[t].stop&&at.test(t)&&a(r[t]);for(t=n.length;t--;)n[t].elem!==this||null!=i&&n[t].queue!==i||(n[t].anim.stop(o),e=!1,n.splice(t,1));!e&&o||S.dequeue(this,i)})},finish:function(a){return!1!==a&&(a=a||"fx"),this.each(function(){var e,t=Y.get(this),n=t[a+"queue"],r=t[a+"queueHooks"],i=S.timers,o=n?n.length:0;for(t.finish=!0,S.queue(this,a,[]),r&&r.stop&&r.stop.call(this,!0),e=i.length;e--;)i[e].elem===this&&i[e].queue===a&&(i[e].anim.stop(!0),i.splice(e,1));for(e=0;e<o;e++)n[e]&&n[e].finish&&n[e].finish.call(this);delete t.finish})}}),S.each(["toggle","show","hide"],function(e,r){var i=S.fn[r];S.fn[r]=function(e,t,n){return null==e||"boolean"==typeof e?i.apply(this,arguments):this.animate(lt(r,!0),e,t,n)}}),S.each({slideDown:lt("show"),slideUp:lt("hide"),slideToggle:lt("toggle"),fadeIn:{opacity:"show"},fadeOut:{opacity:"hide"},fadeToggle:{opacity:"toggle"}},function(e,r){S.fn[e]=function(e,t,n){return this.animate(r,e,t,n)}}),S.timers=[],S.fx.tick=function(){var e,t=0,n=S.timers;for(tt=Date.now();t<n.length;t++)(e=n[t])()||n[t]!==e||n.splice(t--,1);n.length||S.fx.stop(),tt=void 0},S.fx.timer=function(e){S.timers.push(e),S.fx.start()},S.fx.interval=13,S.fx.start=function(){nt||(nt=!0,st())},S.fx.stop=function(){nt=null},S.fx.speeds={slow:600,fast:200,_default:400},S.fn.delay=function(r,e){return r=S.fx&&S.fx.speeds[r]||r,e=e||"fx",this.queue(e,function(e,t){var n=C.setTimeout(e,r);t.stop=function(){C.clearTimeout(n)}})},rt=E.createElement("input"),it=E.createElement("select").appendChild(E.createElement("option")),rt.type="checkbox",y.checkOn=""!==rt.value,y.optSelected=it.selected,(rt=E.createElement("input")).value="t",rt.type="radio",y.radioValue="t"===rt.value;var pt,dt=S.expr.attrHandle;S.fn.extend({attr:function(e,t){return $(this,S.attr,e,t,1<arguments.length)},removeAttr:function(e){return this.each(function(){S.removeAttr(this,e)})}}),S.extend({attr:function(e,t,n){var r,i,o=e.nodeType;if(3!==o&&8!==o&&2!==o)return"undefined"==typeof e.getAttribute?S.prop(e,t,n):(1===o&&S.isXMLDoc(e)||(i=S.attrHooks[t.toLowerCase()]||(S.expr.match.bool.test(t)?pt:void 0)),void 0!==n?null===n?void S.removeAttr(e,t):i&&"set"in i&&void 0!==(r=i.set(e,n,t))?r:(e.setAttribute(t,n+""),n):i&&"get"in i&&null!==(r=i.get(e,t))?r:null==(r=S.find.attr(e,t))?void 0:r)},attrHooks:{type:{set:function(e,t){if(!y.radioValue&&"radio"===t&&A(e,"input")){var n=e.value;return e.setAttribute("type",t),n&&(e.value=n),t}}}},removeAttr:function(e,t){var n,r=0,i=t&&t.match(P);if(i&&1===e.nodeType)while(n=i[r++])e.removeAttribute(n)}}),pt={set:function(e,t,n){return!1===t?S.removeAttr(e,n):e.setAttribute(n,n),n}},S.each(S.expr.match.bool.source.match(/\w+/g),function(e,t){var a=dt[t]||S.find.attr;dt[t]=function(e,t,n){var r,i,o=t.toLowerCase();return n||(i=dt[o],dt[o]=r,r=null!=a(e,t,n)?o:null,dt[o]=i),r}});var ht=/^(?:input|select|textarea|button)$/i,gt=/^(?:a|area)$/i;function vt(e){return(e.match(P)||[]).join(" ")}function yt(e){return e.getAttribute&&e.getAttribute("class")||""}function mt(e){return Array.isArray(e)?e:"string"==typeof e&&e.match(P)||[]}S.fn.extend({prop:function(e,t){return $(this,S.prop,e,t,1<arguments.length)},removeProp:function(e){return this.each(function(){delete this[S.propFix[e]||e]})}}),S.extend({prop:function(e,t,n){var r,i,o=e.nodeType;if(3!==o&&8!==o&&2!==o)return 1===o&&S.isXMLDoc(e)||(t=S.propFix[t]||t,i=S.propHooks[t]),void 0!==n?i&&"set"in i&&void 0!==(r=i.set(e,n,t))?r:e[t]=n:i&&"get"in i&&null!==(r=i.get(e,t))?r:e[t]},propHooks:{tabIndex:{get:function(e){var t=S.find.attr(e,"tabindex");return t?parseInt(t,10):ht.test(e.nodeName)||gt.test(e.nodeName)&&e.href?0:-1}}},propFix:{"for":"htmlFor","class":"className"}}),y.optSelected||(S.propHooks.selected={get:function(e){var t=e.parentNode;return t&&t.parentNode&&t.parentNode.selectedIndex,null},set:function(e){var t=e.parentNode;t&&(t.selectedIndex,t.parentNode&&t.parentNode.selectedIndex)}}),S.each(["tabIndex","readOnly","maxLength","cellSpacing","cellPadding","rowSpan","colSpan","useMap","frameBorder","contentEditable"],function(){S.propFix[this.toLowerCase()]=this}),S.fn.extend({addClass:function(t){var e,n,r,i,o,a,s,u=0;if(m(t))return this.each(function(e){S(this).addClass(t.call(this,e,yt(this)))});if((e=mt(t)).length)while(n=this[u++])if(i=yt(n),r=1===n.nodeType&&" "+vt(i)+" "){a=0;while(o=e[a++])r.indexOf(" "+o+" ")<0&&(r+=o+" ");i!==(s=vt(r))&&n.setAttribute("class",s)}return this},removeClass:function(t){var e,n,r,i,o,a,s,u=0;if(m(t))return this.each(function(e){S(this).removeClass(t.call(this,e,yt(this)))});if(!arguments.length)return this.attr("class","");if((e=mt(t)).length)while(n=this[u++])if(i=yt(n),r=1===n.nodeType&&" "+vt(i)+" "){a=0;while(o=e[a++])while(-1<r.indexOf(" "+o+" "))r=r.replace(" "+o+" "," ");i!==(s=vt(r))&&n.setAttribute("class",s)}return this},toggleClass:function(i,t){var o=typeof i,a="string"===o||Array.isArray(i);return"boolean"==typeof t&&a?t?this.addClass(i):this.removeClass(i):m(i)?this.each(function(e){S(this).toggleClass(i.call(this,e,yt(this),t),t)}):this.each(function(){var e,t,n,r;if(a){t=0,n=S(this),r=mt(i);while(e=r[t++])n.hasClass(e)?n.removeClass(e):n.addClass(e)}else void 0!==i&&"boolean"!==o||((e=yt(this))&&Y.set(this,"__className__",e),this.setAttribute&&this.setAttribute("class",e||!1===i?"":Y.get(this,"__className__")||""))})},hasClass:function(e){var t,n,r=0;t=" "+e+" ";while(n=this[r++])if(1===n.nodeType&&-1<(" "+vt(yt(n))+" ").indexOf(t))return!0;return!1}});var xt=/\r/g;S.fn.extend({val:function(n){var r,e,i,t=this[0];return arguments.length?(i=m(n),this.each(function(e){var t;1===this.nodeType&&(null==(t=i?n.call(this,e,S(this).val()):n)?t="":"number"==typeof t?t+="":Array.isArray(t)&&(t=S.map(t,function(e){return null==e?"":e+""})),(r=S.valHooks[this.type]||S.valHooks[this.nodeName.toLowerCase()])&&"set"in r&&void 0!==r.set(this,t,"value")||(this.value=t))})):t?(r=S.valHooks[t.type]||S.valHooks[t.nodeName.toLowerCase()])&&"get"in r&&void 0!==(e=r.get(t,"value"))?e:"string"==typeof(e=t.value)?e.replace(xt,""):null==e?"":e:void 0}}),S.extend({valHooks:{option:{get:function(e){var t=S.find.attr(e,"value");return null!=t?t:vt(S.text(e))}},select:{get:function(e){var t,n,r,i=e.options,o=e.selectedIndex,a="select-one"===e.type,s=a?null:[],u=a?o+1:i.length;for(r=o<0?u:a?o:0;r<u;r++)if(((n=i[r]).selected||r===o)&&!n.disabled&&(!n.parentNode.disabled||!A(n.parentNode,"optgroup"))){if(t=S(n).val(),a)return t;s.push(t)}return s},set:function(e,t){var n,r,i=e.options,o=S.makeArray(t),a=i.length;while(a--)((r=i[a]).selected=-1<S.inArray(S.valHooks.option.get(r),o))&&(n=!0);return n||(e.selectedIndex=-1),o}}}}),S.each(["radio","checkbox"],function(){S.valHooks[this]={set:function(e,t){if(Array.isArray(t))return e.checked=-1<S.inArray(S(e).val(),t)}},y.checkOn||(S.valHooks[this].get=function(e){return null===e.getAttribute("value")?"on":e.value})}),y.focusin="onfocusin"in C;var bt=/^(?:focusinfocus|focusoutblur)$/,wt=function(e){e.stopPropagation()};S.extend(S.event,{trigger:function(e,t,n,r){var i,o,a,s,u,l,c,f,p=[n||E],d=v.call(e,"type")?e.type:e,h=v.call(e,"namespace")?e.namespace.split("."):[];if(o=f=a=n=n||E,3!==n.nodeType&&8!==n.nodeType&&!bt.test(d+S.event.triggered)&&(-1<d.indexOf(".")&&(d=(h=d.split(".")).shift(),h.sort()),u=d.indexOf(":")<0&&"on"+d,(e=e[S.expando]?e:new S.Event(d,"object"==typeof e&&e)).isTrigger=r?2:3,e.namespace=h.join("."),e.rnamespace=e.namespace?new RegExp("(^|\\.)"+h.join("\\.(?:.*\\.|)")+"(\\.|$)"):null,e.result=void 0,e.target||(e.target=n),t=null==t?[e]:S.makeArray(t,[e]),c=S.event.special[d]||{},r||!c.trigger||!1!==c.trigger.apply(n,t))){if(!r&&!c.noBubble&&!x(n)){for(s=c.delegateType||d,bt.test(s+d)||(o=o.parentNode);o;o=o.parentNode)p.push(o),a=o;a===(n.ownerDocument||E)&&p.push(a.defaultView||a.parentWindow||C)}i=0;while((o=p[i++])&&!e.isPropagationStopped())f=o,e.type=1<i?s:c.bindType||d,(l=(Y.get(o,"events")||Object.create(null))[e.type]&&Y.get(o,"handle"))&&l.apply(o,t),(l=u&&o[u])&&l.apply&&V(o)&&(e.result=l.apply(o,t),!1===e.result&&e.preventDefault());return e.type=d,r||e.isDefaultPrevented()||c._default&&!1!==c._default.apply(p.pop(),t)||!V(n)||u&&m(n[d])&&!x(n)&&((a=n[u])&&(n[u]=null),S.event.triggered=d,e.isPropagationStopped()&&f.addEventListener(d,wt),n[d](),e.isPropagationStopped()&&f.removeEventListener(d,wt),S.event.triggered=void 0,a&&(n[u]=a)),e.result}},simulate:function(e,t,n){var r=S.extend(new S.Event,n,{type:e,isSimulated:!0});S.event.trigger(r,null,t)}}),S.fn.extend({trigger:function(e,t){return this.each(function(){S.event.trigger(e,t,this)})},triggerHandler:function(e,t){var n=this[0];if(n)return S.event.trigger(e,t,n,!0)}}),y.focusin||S.each({focus:"focusin",blur:"focusout"},function(n,r){var i=function(e){S.event.simulate(r,e.target,S.event.fix(e))};S.event.special[r]={setup:function(){var e=this.ownerDocument||this.document||this,t=Y.access(e,r);t||e.addEventListener(n,i,!0),Y.access(e,r,(t||0)+1)},teardown:function(){var e=this.ownerDocument||this.document||this,t=Y.access(e,r)-1;t?Y.access(e,r,t):(e.removeEventListener(n,i,!0),Y.remove(e,r))}}});var Tt=C.location,Ct={guid:Date.now()},Et=/\?/;S.parseXML=function(e){var t;if(!e||"string"!=typeof e)return null;try{t=(new C.DOMParser).parseFromString(e,"text/xml")}catch(e){t=void 0}return t&&!t.getElementsByTagName("parsererror").length||S.error("Invalid XML: "+e),t};var St=/\[\]$/,kt=/\r?\n/g,At=/^(?:submit|button|image|reset|file)$/i,Nt=/^(?:input|select|textarea|keygen)/i;function Dt(n,e,r,i){var t;if(Array.isArray(e))S.each(e,function(e,t){r||St.test(n)?i(n,t):Dt(n+"["+("object"==typeof t&&null!=t?e:"")+"]",t,r,i)});else if(r||"object"!==w(e))i(n,e);else for(t in e)Dt(n+"["+t+"]",e[t],r,i)}S.param=function(e,t){var n,r=[],i=function(e,t){var n=m(t)?t():t;r[r.length]=encodeURIComponent(e)+"="+encodeURIComponent(null==n?"":n)};if(null==e)return"";if(Array.isArray(e)||e.jquery&&!S.isPlainObject(e))S.each(e,function(){i(this.name,this.value)});else for(n in e)Dt(n,e[n],t,i);return r.join("&")},S.fn.extend({serialize:function(){return S.param(this.serializeArray())},serializeArray:function(){return this.map(function(){var e=S.prop(this,"elements");return e?S.makeArray(e):this}).filter(function(){var e=this.type;return this.name&&!S(this).is(":disabled")&&Nt.test(this.nodeName)&&!At.test(e)&&(this.checked||!pe.test(e))}).map(function(e,t){var n=S(this).val();return null==n?null:Array.isArray(n)?S.map(n,function(e){return{name:t.name,value:e.replace(kt,"\r\n")}}):{name:t.name,value:n.replace(kt,"\r\n")}}).get()}});var jt=/%20/g,qt=/#.*$/,Lt=/([?&])_=[^&]*/,Ht=/^(.*?):[ \t]*([^\r\n]*)$/gm,Ot=/^(?:GET|HEAD)$/,Pt=/^\/\//,Rt={},Mt={},It="*/".concat("*"),Wt=E.createElement("a");function Ft(o){return function(e,t){"string"!=typeof e&&(t=e,e="*");var n,r=0,i=e.toLowerCase().match(P)||[];if(m(t))while(n=i[r++])"+"===n[0]?(n=n.slice(1)||"*",(o[n]=o[n]||[]).unshift(t)):(o[n]=o[n]||[]).push(t)}}function Bt(t,i,o,a){var s={},u=t===Mt;function l(e){var r;return s[e]=!0,S.each(t[e]||[],function(e,t){var n=t(i,o,a);return"string"!=typeof n||u||s[n]?u?!(r=n):void 0:(i.dataTypes.unshift(n),l(n),!1)}),r}return l(i.dataTypes[0])||!s["*"]&&l("*")}function $t(e,t){var n,r,i=S.ajaxSettings.flatOptions||{};for(n in t)void 0!==t[n]&&((i[n]?e:r||(r={}))[n]=t[n]);return r&&S.extend(!0,e,r),e}Wt.href=Tt.href,S.extend({active:0,lastModified:{},etag:{},ajaxSettings:{url:Tt.href,type:"GET",isLocal:/^(?:about|app|app-storage|.+-extension|file|res|widget):$/.test(Tt.protocol),global:!0,processData:!0,async:!0,contentType:"application/x-www-form-urlencoded; charset=UTF-8",accepts:{"*":It,text:"text/plain",html:"text/html",xml:"application/xml, text/xml",json:"application/json, text/javascript"},contents:{xml:/\bxml\b/,html:/\bhtml/,json:/\bjson\b/},responseFields:{xml:"responseXML",text:"responseText",json:"responseJSON"},converters:{"* text":String,"text html":!0,"text json":JSON.parse,"text xml":S.parseXML},flatOptions:{url:!0,context:!0}},ajaxSetup:function(e,t){return t?$t($t(e,S.ajaxSettings),t):$t(S.ajaxSettings,e)},ajaxPrefilter:Ft(Rt),ajaxTransport:Ft(Mt),ajax:function(e,t){"object"==typeof e&&(t=e,e=void 0),t=t||{};var c,f,p,n,d,r,h,g,i,o,v=S.ajaxSetup({},t),y=v.context||v,m=v.context&&(y.nodeType||y.jquery)?S(y):S.event,x=S.Deferred(),b=S.Callbacks("once memory"),w=v.statusCode||{},a={},s={},u="canceled",T={readyState:0,getResponseHeader:function(e){var t;if(h){if(!n){n={};while(t=Ht.exec(p))n[t[1].toLowerCase()+" "]=(n[t[1].toLowerCase()+" "]||[]).concat(t[2])}t=n[e.toLowerCase()+" "]}return null==t?null:t.join(", ")},getAllResponseHeaders:function(){return h?p:null},setRequestHeader:function(e,t){return null==h&&(e=s[e.toLowerCase()]=s[e.toLowerCase()]||e,a[e]=t),this},overrideMimeType:function(e){return null==h&&(v.mimeType=e),this},statusCode:function(e){var t;if(e)if(h)T.always(e[T.status]);else for(t in e)w[t]=[w[t],e[t]];return this},abort:function(e){var t=e||u;return c&&c.abort(t),l(0,t),this}};if(x.promise(T),v.url=((e||v.url||Tt.href)+"").replace(Pt,Tt.protocol+"//"),v.type=t.method||t.type||v.method||v.type,v.dataTypes=(v.dataType||"*").toLowerCase().match(P)||[""],null==v.crossDomain){r=E.createElement("a");try{r.href=v.url,r.href=r.href,v.crossDomain=Wt.protocol+"//"+Wt.host!=r.protocol+"//"+r.host}catch(e){v.crossDomain=!0}}if(v.data&&v.processData&&"string"!=typeof v.data&&(v.data=S.param(v.data,v.traditional)),Bt(Rt,v,t,T),h)return T;for(i in(g=S.event&&v.global)&&0==S.active++&&S.event.trigger("ajaxStart"),v.type=v.type.toUpperCase(),v.hasContent=!Ot.test(v.type),f=v.url.replace(qt,""),v.hasContent?v.data&&v.processData&&0===(v.contentType||"").indexOf("application/x-www-form-urlencoded")&&(v.data=v.data.replace(jt,"+")):(o=v.url.slice(f.length),v.data&&(v.processData||"string"==typeof v.data)&&(f+=(Et.test(f)?"&":"?")+v.data,delete v.data),!1===v.cache&&(f=f.replace(Lt,"$1"),o=(Et.test(f)?"&":"?")+"_="+Ct.guid+++o),v.url=f+o),v.ifModified&&(S.lastModified[f]&&T.setRequestHeader("If-Modified-Since",S.lastModified[f]),S.etag[f]&&T.setRequestHeader("If-None-Match",S.etag[f])),(v.data&&v.hasContent&&!1!==v.contentType||t.contentType)&&T.setRequestHeader("Content-Type",v.contentType),T.setRequestHeader("Accept",v.dataTypes[0]&&v.accepts[v.dataTypes[0]]?v.accepts[v.dataTypes[0]]+("*"!==v.dataTypes[0]?", "+It+"; q=0.01":""):v.accepts["*"]),v.headers)T.setRequestHeader(i,v.headers[i]);if(v.beforeSend&&(!1===v.beforeSend.call(y,T,v)||h))return T.abort();if(u="abort",b.add(v.complete),T.done(v.success),T.fail(v.error),c=Bt(Mt,v,t,T)){if(T.readyState=1,g&&m.trigger("ajaxSend",[T,v]),h)return T;v.async&&0<v.timeout&&(d=C.setTimeout(function(){T.abort("timeout")},v.timeout));try{h=!1,c.send(a,l)}catch(e){if(h)throw e;l(-1,e)}}else l(-1,"No Transport");function l(e,t,n,r){var i,o,a,s,u,l=t;h||(h=!0,d&&C.clearTimeout(d),c=void 0,p=r||"",T.readyState=0<e?4:0,i=200<=e&&e<300||304===e,n&&(s=function(e,t,n){var r,i,o,a,s=e.contents,u=e.dataTypes;while("*"===u[0])u.shift(),void 0===r&&(r=e.mimeType||t.getResponseHeader("Content-Type"));if(r)for(i in s)if(s[i]&&s[i].test(r)){u.unshift(i);break}if(u[0]in n)o=u[0];else{for(i in n){if(!u[0]||e.converters[i+" "+u[0]]){o=i;break}a||(a=i)}o=o||a}if(o)return o!==u[0]&&u.unshift(o),n[o]}(v,T,n)),!i&&-1<S.inArray("script",v.dataTypes)&&(v.converters["text script"]=function(){}),s=function(e,t,n,r){var i,o,a,s,u,l={},c=e.dataTypes.slice();if(c[1])for(a in e.converters)l[a.toLowerCase()]=e.converters[a];o=c.shift();while(o)if(e.responseFields[o]&&(n[e.responseFields[o]]=t),!u&&r&&e.dataFilter&&(t=e.dataFilter(t,e.dataType)),u=o,o=c.shift())if("*"===o)o=u;else if("*"!==u&&u!==o){if(!(a=l[u+" "+o]||l["* "+o]))for(i in l)if((s=i.split(" "))[1]===o&&(a=l[u+" "+s[0]]||l["* "+s[0]])){!0===a?a=l[i]:!0!==l[i]&&(o=s[0],c.unshift(s[1]));break}if(!0!==a)if(a&&e["throws"])t=a(t);else try{t=a(t)}catch(e){return{state:"parsererror",error:a?e:"No conversion from "+u+" to "+o}}}return{state:"success",data:t}}(v,s,T,i),i?(v.ifModified&&((u=T.getResponseHeader("Last-Modified"))&&(S.lastModified[f]=u),(u=T.getResponseHeader("etag"))&&(S.etag[f]=u)),204===e||"HEAD"===v.type?l="nocontent":304===e?l="notmodified":(l=s.state,o=s.data,i=!(a=s.error))):(a=l,!e&&l||(l="error",e<0&&(e=0))),T.status=e,T.statusText=(t||l)+"",i?x.resolveWith(y,[o,l,T]):x.rejectWith(y,[T,l,a]),T.statusCode(w),w=void 0,g&&m.trigger(i?"ajaxSuccess":"ajaxError",[T,v,i?o:a]),b.fireWith(y,[T,l]),g&&(m.trigger("ajaxComplete",[T,v]),--S.active||S.event.trigger("ajaxStop")))}return T},getJSON:function(e,t,n){return S.get(e,t,n,"json")},getScript:function(e,t){return S.get(e,void 0,t,"script")}}),S.each(["get","post"],function(e,i){S[i]=function(e,t,n,r){return m(t)&&(r=r||n,n=t,t=void 0),S.ajax(S.extend({url:e,type:i,dataType:r,data:t,success:n},S.isPlainObject(e)&&e))}}),S.ajaxPrefilter(function(e){var t;for(t in e.headers)"content-type"===t.toLowerCase()&&(e.contentType=e.headers[t]||"")}),S._evalUrl=function(e,t,n){return S.ajax({url:e,type:"GET",dataType:"script",cache:!0,async:!1,global:!1,converters:{"text script":function(){}},dataFilter:function(e){S.globalEval(e,t,n)}})},S.fn.extend({wrapAll:function(e){var t;return this[0]&&(m(e)&&(e=e.call(this[0])),t=S(e,this[0].ownerDocument).eq(0).clone(!0),this[0].parentNode&&t.insertBefore(this[0]),t.map(function(){var e=this;while(e.firstElementChild)e=e.firstElementChild;return e}).append(this)),this},wrapInner:function(n){return m(n)?this.each(function(e){S(this).wrapInner(n.call(this,e))}):this.each(function(){var e=S(this),t=e.contents();t.length?t.wrapAll(n):e.append(n)})},wrap:function(t){var n=m(t);return this.each(function(e){S(this).wrapAll(n?t.call(this,e):t)})},unwrap:function(e){return this.parent(e).not("body").each(function(){S(this).replaceWith(this.childNodes)}),this}}),S.expr.pseudos.hidden=function(e){return!S.expr.pseudos.visible(e)},S.expr.pseudos.visible=function(e){return!!(e.offsetWidth||e.offsetHeight||e.getClientRects().length)},S.ajaxSettings.xhr=function(){try{return new C.XMLHttpRequest}catch(e){}};var _t={0:200,1223:204},zt=S.ajaxSettings.xhr();y.cors=!!zt&&"withCredentials"in zt,y.ajax=zt=!!zt,S.ajaxTransport(function(i){var o,a;if(y.cors||zt&&!i.crossDomain)return{send:function(e,t){var n,r=i.xhr();if(r.open(i.type,i.url,i.async,i.username,i.password),i.xhrFields)for(n in i.xhrFields)r[n]=i.xhrFields[n];for(n in i.mimeType&&r.overrideMimeType&&r.overrideMimeType(i.mimeType),i.crossDomain||e["X-Requested-With"]||(e["X-Requested-With"]="XMLHttpRequest"),e)r.setRequestHeader(n,e[n]);o=function(e){return function(){o&&(o=a=r.onload=r.onerror=r.onabort=r.ontimeout=r.onreadystatechange=null,"abort"===e?r.abort():"error"===e?"number"!=typeof r.status?t(0,"error"):t(r.status,r.statusText):t(_t[r.status]||r.status,r.statusText,"text"!==(r.responseType||"text")||"string"!=typeof r.responseText?{binary:r.response}:{text:r.responseText},r.getAllResponseHeaders()))}},r.onload=o(),a=r.onerror=r.ontimeout=o("error"),void 0!==r.onabort?r.onabort=a:r.onreadystatechange=function(){4===r.readyState&&C.setTimeout(function(){o&&a()})},o=o("abort");try{r.send(i.hasContent&&i.data||null)}catch(e){if(o)throw e}},abort:function(){o&&o()}}}),S.ajaxPrefilter(function(e){e.crossDomain&&(e.contents.script=!1)}),S.ajaxSetup({accepts:{script:"text/javascript, application/javascript, application/ecmascript, application/x-ecmascript"},contents:{script:/\b(?:java|ecma)script\b/},converters:{"text script":function(e){return S.globalEval(e),e}}}),S.ajaxPrefilter("script",function(e){void 0===e.cache&&(e.cache=!1),e.crossDomain&&(e.type="GET")}),S.ajaxTransport("script",function(n){var r,i;if(n.crossDomain||n.scriptAttrs)return{send:function(e,t){r=S("<script>").attr(n.scriptAttrs||{}).prop({charset:n.scriptCharset,src:n.url}).on("load error",i=function(e){r.remove(),i=null,e&&t("error"===e.type?404:200,e.type)}),E.head.appendChild(r[0])},abort:function(){i&&i()}}});var Ut,Xt=[],Vt=/(=)\?(?=&|$)|\?\?/;S.ajaxSetup({jsonp:"callback",jsonpCallback:function(){var e=Xt.pop()||S.expando+"_"+Ct.guid++;return this[e]=!0,e}}),S.ajaxPrefilter("json jsonp",function(e,t,n){var r,i,o,a=!1!==e.jsonp&&(Vt.test(e.url)?"url":"string"==typeof e.data&&0===(e.contentType||"").indexOf("application/x-www-form-urlencoded")&&Vt.test(e.data)&&"data");if(a||"jsonp"===e.dataTypes[0])return r=e.jsonpCallback=m(e.jsonpCallback)?e.jsonpCallback():e.jsonpCallback,a?e[a]=e[a].replace(Vt,"$1"+r):!1!==e.jsonp&&(e.url+=(Et.test(e.url)?"&":"?")+e.jsonp+"="+r),e.converters["script json"]=function(){return o||S.error(r+" was not called"),o[0]},e.dataTypes[0]="json",i=C[r],C[r]=function(){o=arguments},n.always(function(){void 0===i?S(C).removeProp(r):C[r]=i,e[r]&&(e.jsonpCallback=t.jsonpCallback,Xt.push(r)),o&&m(i)&&i(o[0]),o=i=void 0}),"script"}),y.createHTMLDocument=((Ut=E.implementation.createHTMLDocument("").body).innerHTML="<form></form><form></form>",2===Ut.childNodes.length),S.parseHTML=function(e,t,n){return"string"!=typeof e?[]:("boolean"==typeof t&&(n=t,t=!1),t||(y.createHTMLDocument?((r=(t=E.implementation.createHTMLDocument("")).createElement("base")).href=E.location.href,t.head.appendChild(r)):t=E),o=!n&&[],(i=N.exec(e))?[t.createElement(i[1])]:(i=xe([e],t,o),o&&o.length&&S(o).remove(),S.merge([],i.childNodes)));var r,i,o},S.fn.load=function(e,t,n){var r,i,o,a=this,s=e.indexOf(" ");return-1<s&&(r=vt(e.slice(s)),e=e.slice(0,s)),m(t)?(n=t,t=void 0):t&&"object"==typeof t&&(i="POST"),0<a.length&&S.ajax({url:e,type:i||"GET",dataType:"html",data:t}).done(function(e){o=arguments,a.html(r?S("<div>").append(S.parseHTML(e)).find(r):e)}).always(n&&function(e,t){a.each(function(){n.apply(this,o||[e.responseText,t,e])})}),this},S.expr.pseudos.animated=function(t){return S.grep(S.timers,function(e){return t===e.elem}).length},S.offset={setOffset:function(e,t,n){var r,i,o,a,s,u,l=S.css(e,"position"),c=S(e),f={};"static"===l&&(e.style.position="relative"),s=c.offset(),o=S.css(e,"top"),u=S.css(e,"left"),("absolute"===l||"fixed"===l)&&-1<(o+u).indexOf("auto")?(a=(r=c.position()).top,i=r.left):(a=parseFloat(o)||0,i=parseFloat(u)||0),m(t)&&(t=t.call(e,n,S.extend({},s))),null!=t.top&&(f.top=t.top-s.top+a),null!=t.left&&(f.left=t.left-s.left+i),"using"in t?t.using.call(e,f):("number"==typeof f.top&&(f.top+="px"),"number"==typeof f.left&&(f.left+="px"),c.css(f))}},S.fn.extend({offset:function(t){if(arguments.length)return void 0===t?this:this.each(function(e){S.offset.setOffset(this,t,e)});var e,n,r=this[0];return r?r.getClientRects().length?(e=r.getBoundingClientRect(),n=r.ownerDocument.defaultView,{top:e.top+n.pageYOffset,left:e.left+n.pageXOffset}):{top:0,left:0}:void 0},position:function(){if(this[0]){var e,t,n,r=this[0],i={top:0,left:0};if("fixed"===S.css(r,"position"))t=r.getBoundingClientRect();else{t=this.offset(),n=r.ownerDocument,e=r.offsetParent||n.documentElement;while(e&&(e===n.body||e===n.documentElement)&&"static"===S.css(e,"position"))e=e.parentNode;e&&e!==r&&1===e.nodeType&&((i=S(e).offset()).top+=S.css(e,"borderTopWidth",!0),i.left+=S.css(e,"borderLeftWidth",!0))}return{top:t.top-i.top-S.css(r,"marginTop",!0),left:t.left-i.left-S.css(r,"marginLeft",!0)}}},offsetParent:function(){return this.map(function(){var e=this.offsetParent;while(e&&"static"===S.css(e,"position"))e=e.offsetParent;return e||re})}}),S.each({scrollLeft:"pageXOffset",scrollTop:"pageYOffset"},function(t,i){var o="pageYOffset"===i;S.fn[t]=function(e){return $(this,function(e,t,n){var r;if(x(e)?r=e:9===e.nodeType&&(r=e.defaultView),void 0===n)return r?r[i]:e[t];r?r.scrollTo(o?r.pageXOffset:n,o?n:r.pageYOffset):e[t]=n},t,e,arguments.length)}}),S.each(["top","left"],function(e,n){S.cssHooks[n]=$e(y.pixelPosition,function(e,t){if(t)return t=Be(e,n),Me.test(t)?S(e).position()[n]+"px":t})}),S.each({Height:"height",Width:"width"},function(a,s){S.each({padding:"inner"+a,content:s,"":"outer"+a},function(r,o){S.fn[o]=function(e,t){var n=arguments.length&&(r||"boolean"!=typeof e),i=r||(!0===e||!0===t?"margin":"border");return $(this,function(e,t,n){var r;return x(e)?0===o.indexOf("outer")?e["inner"+a]:e.document.documentElement["client"+a]:9===e.nodeType?(r=e.documentElement,Math.max(e.body["scroll"+a],r["scroll"+a],e.body["offset"+a],r["offset"+a],r["client"+a])):void 0===n?S.css(e,t,i):S.style(e,t,n,i)},s,n?e:void 0,n)}})}),S.each(["ajaxStart","ajaxStop","ajaxComplete","ajaxError","ajaxSuccess","ajaxSend"],function(e,t){S.fn[t]=function(e){return this.on(t,e)}}),S.fn.extend({bind:function(e,t,n){return this.on(e,null,t,n)},unbind:function(e,t){return this.off(e,null,t)},delegate:function(e,t,n,r){return this.on(t,e,n,r)},undelegate:function(e,t,n){return 1===arguments.length?this.off(e,"**"):this.off(t,e||"**",n)},hover:function(e,t){return this.mouseenter(e).mouseleave(t||e)}}),S.each("blur focus focusin focusout resize scroll click dblclick mousedown mouseup mousemove mouseover mouseout mouseenter mouseleave change select submit keydown keypress keyup contextmenu".split(" "),function(e,n){S.fn[n]=function(e,t){return 0<arguments.length?this.on(n,null,e,t):this.trigger(n)}});var Gt=/^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g;S.proxy=function(e,t){var n,r,i;if("string"==typeof t&&(n=e[t],t=e,e=n),m(e))return r=s.call(arguments,2),(i=function(){return e.apply(t||this,r.concat(s.call(arguments)))}).guid=e.guid=e.guid||S.guid++,i},S.holdReady=function(e){e?S.readyWait++:S.ready(!0)},S.isArray=Array.isArray,S.parseJSON=JSON.parse,S.nodeName=A,S.isFunction=m,S.isWindow=x,S.camelCase=X,S.type=w,S.now=Date.now,S.isNumeric=function(e){var t=S.type(e);return("number"===t||"string"===t)&&!isNaN(e-parseFloat(e))},S.trim=function(e){return null==e?"":(e+"").replace(Gt,"")},"function"==typeof define&&define.amd&&define("jquery",[],function(){return S});var Yt=C.jQuery,Qt=C.$;return S.noConflict=function(e){return C.$===S&&(C.$=Qt),e&&C.jQuery===S&&(C.jQuery=Yt),S},"undefined"==typeof e&&(C.jQuery=C.$=S),S});

//]]></script> 
  
  <script src='//additionindianscontentment.com/00/a5/c0/00a5c0f74dfd01ca90f82cb0771654c4.js' type='text/javascript'/>
  </head>
  <body id='mainContent'>
    <script>/*<![CDATA[*/ (localStorage.getItem('mode')) === 'darkmode' ? document.querySelector('#mainContent').classList.add('darkMode') : document.querySelector('#mainContent').classList.remove('darkMode') /*]]>*/</script>
<div id='page'>
<header class='menurekom' id='header-outer'> 
<div class='menu-icons'><div class='toggleMenu'><svg class='ikonme' height='24' viewBox='0 0 24 24' width='24'><path d='M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z'/></svg></div></div>
                <b:section class='header' id='header' name='Header' showaddelement='fasle'>
                  <b:widget id='Header1' locked='true' title='image4x (Header)' type='Header' version='2' visible='true'>
                    <b:widget-settings>
                      <b:widget-setting name='displayUrl'/>
                      <b:widget-setting name='displayHeight'>0</b:widget-setting>
                      <b:widget-setting name='sectionWidth'>926</b:widget-setting>
                      <b:widget-setting name='useImage'>false</b:widget-setting>
                      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                      <b:widget-setting name='imagePlacement'>BEHIND</b:widget-setting>
                      <b:widget-setting name='displayWidth'>0</b:widget-setting>
                    </b:widget-settings>
                    <b:includable id='main' var='this'>
                  <b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
                  <b:include cond='data:imagePlacement not in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='title'/>
                  <b:include cond='data:imagePlacement != &quot;REPLACE&quot;' name='description'/>
                  <b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='behindImageStyle'/>
                </b:includable>
                    <b:includable id='behindImageStyle'>
                  <b:if cond='data:sourceUrl'>
                    <b:include cond='data:this.image' data='{image: data:this.image, selector: &quot;#header .widget&quot;}' name='responsiveImageStyle'/>
                  </b:if>
                </b:includable>
                    <b:includable id='description'>
                  <div class='description hidden'><data:this.description/></div>
                </b:includable>
                    <b:includable id='image'>
                  <div class='header-inner'>
                    <a expr:href='data:blog.homepageUrl' expr:title='data:title'><img expr:alt='data:title' expr:src='resizeImage(data:sourceUrl, 300)' expr:title='data:title'/></a>
                    <b:include cond='data:this.imagePlacement == &quot;REPLACE&quot;' name='title'/>
                  </div>
                </b:includable>
                    <b:includable id='title'>
                  <div class='header-inner'>
                    <b:class cond='data:this.imagePlacement == &quot;REPLACE&quot;' name='hidden'/>
                    <b:if cond='data:view.isSingleItem'>
                      <h1><a expr:data-text='data:title' expr:href='data:blog.homepageUrl' expr:title='data:title'><data:title/></a></h1>
                      <b:elseif cond='data:view.isHomepage'/>
                      <h1 expr:data-text='data:title'><data:title/></h1>
                      <b:else/>
                      <h1><a expr:data-text='data:title' expr:href='data:blog.homepageUrl' expr:title='data:title'><data:title/></a></h1>
                    </b:if>
                  </div>
                </b:includable>
                  </b:widget>
                  <b:widget id='BlogSearch1' locked='true' title='Cari' type='BlogSearch' version='2' visible='true'>
                    <b:includable id='main'>
    <b:include name='content'/>
</b:includable>
                    <b:includable id='content'>
    <div class='bg_Se' role='search'>
      <b:include name='searchForm'/>
    </div>
</b:includable>
                    <b:includable id='searchForm'>
    <form class='gb_Se' expr:action='data:blog.searchUrl' method='get'>
      <b:include name='searchSubmit'/>
      <input autocomplete='off' dir='ltr' expr:aria-label='data:messages.searchThisBlog' expr:placeholder='data:messages.search' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q' spellcheck='false' type='text'/>
        <div class='close-searchbtn' onclick='document.getElementById(&apos;BlogSearch1&apos;).style.display = &apos;none&apos;;'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z'/></svg></div>
                      </form>
</b:includable>
                    <b:includable id='searchSubmit'>
    <button class='Se' expr:aria-label='data:messages.search' expr:title='data:messages.search' role='button' type='submit'><svg aria-label='Cari' height='24' viewBox='0 0 65 65' width='24'><path d='M20 40C9 40 0 31 0 20S9 0 20 0s20 9 20 20-9 20-20 20zm0-37C10.6 3 3 10.6 3 20s7.6 17 17 17 17-7.6 17-17S29.4 3 20 3z'/><path d='M46.6 48.1c-.4 0-.8-.1-1.1-.4L32 34.2c-.6-.6-.6-1.5 0-2.1s1.5-.6 2.1 0l13.5 13.5c.6.6.6 1.5 0 2.1-.2.3-.6.4-1 .4z'/></svg></button>
                    </b:includable>
                  </b:widget>
                </b:section>
		<div class='buka-tutup'>
          <svg class='buka-tutup menubookmark' style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M17,3H7A2,2 0 0,0 5,5V21L12,18L19,21V5C19,3.89 18.1,3 17,3Z'/></svg>
  		</div>
	<span aria-label='Dark' class='navDark' data-text='Dark' onclick='darkMode()' role='button'><i/></span>
	<div class='searchbtn' onclick='document.getElementById(&apos;BlogSearch1&apos;).style.display = &apos;block&apos;;'><svg aria-label='Cari' height='24' viewBox='0 0 65 65' width='24'><path d='M20 40C9 40 0 31 0 20S9 0 20 0s20 9 20 20-9 20-20 20zm0-37C10.6 3 3 10.6 3 20s7.6 17 17 17 17-7.6 17-17S29.4 3 20 3z'/><path d='M46.6 48.1c-.4 0-.8-.1-1.1-.4L32 34.2c-.6-.6-.6-1.5 0-2.1s1.5-.6 2.1 0l13.5 13.5c.6.6.6 1.5 0 2.1-.2.3-.6.4-1 .4z'/></svg></div>
  	</header>
  <b:if cond='data:view.isMultipleItems'>
    <style>#page {padding-bottom: 0;padding-top: 60px}</style>
                <b:section class='labelbottom' id='labelbottom' name='Kategori Bawah' showaddelement='false'>
                  <b:widget id='Label1' locked='true' title='Kategori' type='Label' version='2' visible='true'>
                    <b:widget-settings>
                      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                      <b:widget-setting name='display'>CLOUD</b:widget-setting>
                      <b:widget-setting name='selectedLabelsList'/>
                      <b:widget-setting name='showType'>ALL</b:widget-setting>
                      <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
                    </b:widget-settings>
                    <b:includable id='main' var='this'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
                    <b:includable id='cloud'>
  <b:loop values='data:labels' var='label'>
    <span class='label-bawah-menu'>
      <a class='label-bawah-menu-a' expr:href='data:label.url'>
        <data:label.name/>
        <b:if cond='data:this.showFreqNumbers'>
          <span class='label-count'><data:label.count/></span>
        </b:if>
      </a>
    </span>
  </b:loop>
</b:includable>
                    <b:includable id='content'>
	<div class='left-btn'><button id='left-button'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M15.41,16.58L10.83,12L15.41,7.41L14,6L8,12L14,18L15.41,16.58Z' fill='currentColor'/></svg></button></div>
    <div class='right-btn'><button id='right-button'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z' fill='currentColor'/></svg></button></div>
  <div class='widget-content'>
    <b:class expr:name='data:this.display + &quot;-label-widget-content&quot;'/>
    <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
    <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
  </div>
</b:includable>
                    <b:includable id='list'>
  <ul>
    <b:loop values='data:labels' var='label'>
      <li>
        <a class='label-name' expr:href='data:label.url'>
          <data:label.name/>
          <b:if cond='data:this.showFreqNumbers'>
            <span class='label-count'><data:label.count/></span>
          </b:if>
        </a>
      </li>
    </b:loop>
  </ul>
</b:includable>
                    <b:includable id='widget-title'>
                      <h3 class='sec-title hidden'><data:title/></h3>
                    </b:includable>
                  </b:widget>
                </b:section>
  </b:if>
</div>
<div class='darkshadow'/>
  <!-- wrapper start -->
  <div id='wrapper'>
  <!-- post wrapper start -->
  <div id='post-wrapper'>
  <div class='post-container'> 
  <b:section class='main' id='main' showaddelement='no'>
     <b:widget id='HTML4' locked='true' title='IKLAN DIBAWAH HEADER' type='HTML' version='2' visible='true'>
       <b:widget-settings>
         <b:widget-setting name='content'>&lt;a title=&quot;Iklan Prib Adstera 1&quot;
href=&quot;https://publishers.adsterra.com/referral/WvH27VPBkV&quot;target=&quot;_blank&quot;&gt;&lt;img alt=&quot;referals adstera&quot;
src=&quot;https://blogger.googleusercontent.com/img/b/R29vZ2&#8230;bpFmXA9gl_SkQD2E4Lf/w900/720x90_adsterra_reff.gif&quot;
width=&quot;700px&quot;height=&quot;60px&quot;/&gt;&lt;/a&gt;</b:widget-setting>
       </b:widget-settings>
       <b:includable id='main'>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
     </b:widget>
     <b:widget id='Blog1' locked='true' title='Postingan Blog' type='Blog' version='1'>
       <b:widget-settings>
         <b:widget-setting name='commentLabel'>comments</b:widget-setting>
         <b:widget-setting name='showShareButtons'>true</b:widget-setting>
         <b:widget-setting name='authorLabel'>By</b:widget-setting>
         <b:widget-setting name='disableGooglePlusShare'>true</b:widget-setting>
         <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
         <b:widget-setting name='timestampLabel'>pada tanggal</b:widget-setting>
         <b:widget-setting name='reactionsLabel'/>
         <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
         <b:widget-setting name='style.layout'>1x1</b:widget-setting>
         <b:widget-setting name='showLocation'>false</b:widget-setting>
         <b:widget-setting name='showTimestamp'>true</b:widget-setting>
         <b:widget-setting name='postsPerAd'>1</b:widget-setting>
         <b:widget-setting name='style.bordercolor'>#b22e2e</b:widget-setting>
         <b:widget-setting name='showDateHeader'>true</b:widget-setting>
         <b:widget-setting name='style.textcolor'>#222222</b:widget-setting>
         <b:widget-setting name='showCommentLink'>true</b:widget-setting>
         <b:widget-setting name='style.urlcolor'>#b7af24</b:widget-setting>
         <b:widget-setting name='showAuthor'>false</b:widget-setting>
         <b:widget-setting name='style.linkcolor'>#b3b712</b:widget-setting>
         <b:widget-setting name='style.bgcolor'>#b22e2e</b:widget-setting>
         <b:widget-setting name='showLabels'>true</b:widget-setting>
         <b:widget-setting name='postLabelsLabel'>Category</b:widget-setting>
         <b:widget-setting name='showBacklinks'>false</b:widget-setting>
         <b:widget-setting name='showInlineAds'>false</b:widget-setting>
         <b:widget-setting name='showReactions'>false</b:widget-setting>
       </b:widget-settings>
       <b:includable id='main' var='top'>
  <b:if cond='data:mobile == &quot;false&quot;'>
    <!-- posts -->
      <b:include data='top' name='status-message'/>
    <div class='blog-posts'>
      <data:defaultAdStart/> 
      <b:loop index='infeed' values='data:posts' var='post'>	
	    <b:if cond='data:blog.pageType in {&quot;index&quot;}'>
		<b:if cond='data:blog.searchLabel != &quot;Artikel&quot;'>
		<b:if cond='data:post.labels'>
		<b:loop values='data:post.labels' var='label'>
		<b:if cond='data:label.name == &quot;Artikel&quot;'>
		&lt;div class=&#39;hilangkan&#39;&gt;
		</b:if>
		</b:loop>
		</b:if>
		</b:if>
		</b:if>
        <article class='post-outer'>
        <b:include data='post' name='post'/>
        <b:if cond='data:blog.pageType == &quot;static_page&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
        <b:if cond='data:blog.pageType == &quot;item&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
        </article>
        <b:if cond='data:view.isMultipleItems'>
  <b:if cond='data:infeed == 3'>
        <article class='post-outer'>
          <div class='img-thumbnail'>
	<!-- IKLAN DIANTARA POSTINGAN -->
            <div class='....' style='min-height: 200px;'/>
            <div class='.....'><h1 itemprop='name'>Advertisement</h1></div>
            </div>
        </article>
  </b:if>
</b:if>
		<b:if cond='data:blog.pageType in {&quot;index&quot;}'>
		<b:if cond='data:blog.searchLabel != &quot;Artikel&quot;'>
		<b:if cond='data:post.labels'>
		<b:loop values='data:post.labels' var='label'>
		<b:if cond='data:label.name == &quot;Artikel&quot;'>
		&lt;/div&gt;
		<script>$(&quot;.hilangkan&quot;).remove();</script>
		</b:if>
		</b:loop>
		</b:if>
		</b:if>
		</b:if>
		
      </b:loop>
      <data:adEnd/>
	  
    </div>

    <!-- navigation -->
	<div class='clear'/>
	    <b:if cond='data:blog.pageType in {&quot;index&quot;}'>
	<b:include name='nextprev'/>

		</b:if>

  <b:else/>
    <b:include name='mobile-main'/>
  </b:if>
</b:includable>
       <b:includable id='backlinkDeleteIcon' var='backlink'>
  <span expr:class='&quot;item-control &quot; + data:backlink.adminClass'>
    <a expr:href='data:backlink.deleteUrl' expr:title='data:top.deleteBacklinkMsg'>
      <img src='//www.blogger.com/img/icon_delete13.gif'/>
    </a>
  </span>
</b:includable>
       <b:includable id='backlinks' var='post'/>
       <b:includable id='breadcrumb' var='posts'>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<b:loop values='data:posts' var='post'>
<b:if cond='data:post.labels'>
<div class='breadcrumbs' itemscope='itemscope' itemtype='https://schema.org/BreadcrumbList'>
<svg viewBox='0 0 24 24'><path d='M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z' fill='#000000'/></svg>
<span itemprop='itemListElement' itemscope='itemscope' itemtype='https://schema.org/ListItem'>
<a expr:href='data:blog.homepageUrl' itemprop='item' title='Home'>
<span itemprop='name'>Home</span><svg viewBox='0 0 24 24'><path d='M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z' fill='#000000'/></svg></a>
<meta content='1' itemprop='position'/>
</span>
<svg viewBox='0 0 24 24'><path d='M5.5,9A1.5,1.5 0 0,0 7,7.5A1.5,1.5 0 0,0 5.5,6A1.5,1.5 0 0,0 4,7.5A1.5,1.5 0 0,0 5.5,9M17.41,11.58C17.77,11.94 18,12.44 18,13C18,13.55 17.78,14.05 17.41,14.41L12.41,19.41C12.05,19.77 11.55,20 11,20C10.45,20 9.95,19.78 9.58,19.41L2.59,12.42C2.22,12.05 2,11.55 2,11V6C2,4.89 2.89,4 4,4H9C9.55,4 10.05,4.22 10.41,4.58L17.41,11.58M13.54,5.71L14.54,4.71L21.41,11.58C21.78,11.94 22,12.45 22,13C22,13.55 21.78,14.05 21.42,14.41L16.04,19.79L15.04,18.79L20.75,13L13.54,5.71Z' fill='#000000'/></svg>
<b:loop index='num' values='data:post.labels' var='label'>
<span itemprop='itemListElement' itemscope='itemscope' itemtype='https://schema.org/ListItem'>
<a expr:href='data:label.url + &quot;?&amp;max-results=16&quot;' expr:title='data:label.name' itemprop='item'>
<span itemprop='name'><data:label.name/></span>
</a>
<meta expr:content='data:num+2' itemprop='position'/>
</span>
<b:if cond='data:label.isLast != &quot;true&quot;'>
<svg viewBox='0 0 24 24'><path d='M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z' fill='#000000'/></svg>
</b:if>
</b:loop>
<svg viewBox='0 0 24 24'><path d='M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z' fill='#000000'/></svg>
<span><data:post.title/></span>
</div>
</b:if>
</b:loop>
</b:if>
</b:includable>
       <b:includable id='comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <h4 id='comment-post-message'>
        <a expr:id='data:widget.instanceId + &quot;_comment-editor-toggle-link&quot;' href='javascript:void(0)'><data:postCommentMsg/></a></h4>
      <div class='pesan-komentar'><p><data:blogCommentMessage/></p></div>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <h4 id='comment-post-message'><data:postCommentMsg/></h4>
      <div class='pesan-komentar'><p><data:blogCommentMessage/></p></div>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
       <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:top.deleteCommentMsg'>
        <img src='//www.blogger.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
       <b:includable id='comment_count_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <span class='cmt_count_iframe_holder' expr:data-count='data:post.numComments' expr:data-onclick='data:post.addCommentOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.canonicalUrl'>
    </span>
  <b:else/>
    <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'>
      <data:post.commentLabelFull/>:
    </a>
  </b:if>
</b:includable>
       <b:includable id='comment_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <b:include data='post' name='iframe_comments'/>
  <b:else/>
    <b:if cond='data:post.showThreadedComments'>
      <b:include data='post' name='threaded_comments'/>
    <b:else/>
      <b:include data='post' name='comments'/>
    </b:if>
  </b:if>
</b:includable>
       <b:includable id='comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>
      <div class='judul-review'><h3><b:if cond='data:post.numComments == 0'>Komentar (0)</b:if> <b:if cond='data:post.numComments == 1'>Komentar (1)</b:if> <b:if cond='data:post.numComments &gt; 1'>Komentar (<data:post.numComments/>)</b:if></h3></div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <b:if cond='data:post.hasOlderLinks'>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'><data:post.oldestLinkText/></a>
              &#160;
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'><data:post.olderLinkText/></a>
              &#160;
          </b:if>
          <data:post.commentRangeText/>
          <b:if cond='data:post.hasNewerLinks'>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'><data:post.newerLinkText/></a>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'><data:post.newestLinkText/></a>
          </b:if>
        </span>
      </b:if>

      <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <dl expr:class='data:post.avatarIndentClass' id='comments-block'>
          <b:loop values='data:post.comments' var='comment'>
            <dt expr:class='&quot;comment-author &quot; + data:comment.authorClass' expr:id='data:comment.anchorName'>
              <b:if cond='data:comment.favicon'>
                <img expr:src='data:comment.favicon' height='16px' style='margin-bottom:-2px;' width='16px'/>
              </b:if>
              <a expr:id='data:comment.anchorName'/>
              <b:if cond='data:blog.enabledCommentProfileImages'>
                <data:comment.authorAvatarImage/>
              </b:if>
              <b:if cond='data:comment.authorUrl'>
                <a expr:href='data:comment.authorUrl' rel='nofollow'><data:comment.author/></a>
              <b:else/>
                <data:comment.author/>
              </b:if>
              <data:commentPostedByMsg/>
            </dt>
            <dd class='comment-body' expr:id='data:widget.instanceId + data:comment.cmtBodyIdPostfix'>
              <b:if cond='data:comment.isDeleted'>
                <span class='deleted-comment'><data:comment.body/></span>
              <b:else/>
                <p>
                  <data:comment.body/>
                </p>
              </b:if>
            </dd>
            <dd class='comment-footer'>
              <span class='comment-timestamp'>
                <a expr:href='data:comment.url' title='comment permalink'>
                  <data:comment.timestamp/>
                </a>
                <b:include data='comment' name='commentDeleteIcon'/>
              </span>
            </dd>
          </b:loop>
        </dl>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
            <data:post.oldestLinkText/>
          </a>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
            <data:post.olderLinkText/>
          </a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
            <data:post.newerLinkText/>
          </a>
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
            <data:post.newestLinkText/>
          </a>
        </span>
      </b:if>

      <p class='comment-footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='comment-form'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:else/>
          <b:if cond='data:post.allowComments'>
            <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
          </b:if>
        </b:if>

      </p>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:if cond='data:post.showBacklinks'>
         <b:include data='post' name='backlinks'/>
       </b:if>
    </div>
    </div>
  </div>
</b:includable>
       <b:includable id='feedLinks'>
  <b:if cond='data:blog.pageType != &quot;item&quot;'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
        <b:include data='feedLinks' name='feedLinksBody'/>
      </div>
    </b:if>

    <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.allowComments'>
          <b:if cond='data:post.feedLinks'>
            <b:include data='post.feedLinks' name='feedLinksBody'/>
          </b:if>
        </b:if>
      </b:loop>
    </div>
  </b:if>
</b:includable>
       <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links'>
  <data:feedLinksMsg/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
       <b:includable id='iframe_comments' var='post'>

  <b:if cond='data:post.allowIframeComments'>
    <script expr:src='data:post.iframeCommentSrc'/>
    <div class='cmt_iframe_holder' expr:data-href='data:post.canonicalUrl' expr:data-viewtype='data:post.viewType'/>

    <b:if cond='data:post.embedCommentForm == &quot;false&quot;'>
      <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
    </b:if>
  </b:if>
</b:includable>
       <b:includable id='mobile-index-post' var='post'>
<!-- MOBILE INDEX POST HERE -->
  <div class='mobile-date-outer date-outer'>

    <div class='mobile-post-outer'>

        <div class='mobile-index-contents'>
          <b:if cond='data:post.thumbnailUrl'>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
                <img expr:src='data:post.thumbnailUrl'/>
              </div>
            </div>
			<b:else/>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
				<img expr:alt='data:post.title' expr:title='data:post.title' src='//3.bp.blogspot.com/-ltyYh4ysBHI/U04MKlHc6pI/AAAAAAAADQo/PFxXaGZu9PQ/s66-c/no-image.png'/>
              </div>
            </div>
          </b:if>

      <a expr:href='data:post.url'>
        <h3 class='mobile-index-title entry-title'>
          <data:post.title/>
        </h3>
	  </a>		  

          <div class='post-body'>

		    <div class='post-info'>
				<b:if cond='data:top.showAuthor'>
					<b:if cond='data:post.authorProfileUrl'>
					  <span class='author-info'>
						<a class='g-profile' expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
						  <data:post.author/>
						</a>
					  </span>
					<b:else/>
					  <span class='author-info'>
						<data:post.author/>
					  </span>
					</b:if>
				</b:if> 
				<b:if cond='data:top.showTimestamp'>
				<b:if cond='data:post.url'>
				  <span class='time-info'>
				  / <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><span class='published updated' expr:content='data:post.timestampISO8601'><data:post.timestamp/></span></a>
				  </span>
				</b:if>
				</b:if> 
				<b:if cond='data:blog.pageType != &quot;item&quot;'>
				  <b:if cond='data:blog.pageType != &quot;static_page&quot;'>
					<b:if cond='data:post.allowComments'>
					  <span class='comment-info'>
					  / <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'> <b:if cond='data:post.numComments == 0'> Add Comment </b:if> <b:if cond='data:post.numComments == 1'> 1 Comment </b:if> <b:if cond='data:post.numComments &gt; 1'> <data:post.numComments/> Comments </b:if> 
					  </a>
					  </span>
					</b:if>
				  </b:if>
				</b:if>	
			</div>

          </div>
        </div>

        <div style='clear: both;'/>

    </div>
	
  </div>
</b:includable>
       <b:includable id='mobile-main' var='top'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-index-post'/>
        </b:loop>
      <b:else/>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-post'/>
        </b:loop>
      </b:if>
    </div>

   <b:include name='mobile-nextprev'/>
</b:includable>
       <b:includable id='mobile-nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <div class='mobile-link-button' id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'>Wallpaper Terbaru</a>
      </div>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <div class='mobile-link-button' id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>&amp;rsaquo;</a>
      </div>
    </b:if>

    <div class='mobile-link-button' id='blog-pager-home-link'>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    </div>

    <div class='mobile-desktop-link'>
      <a class='home-link' expr:href='data:desktopLinkUrl'><data:desktopLinkMsg/></a>
    </div>

  </div>
  <div class='clear'/>
</b:includable>
       <b:includable id='mobile-post' var='post'>
  <div class='date-outer'>
    <b:if cond='data:post.dateHeader'>
      <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
    </b:if>
    <div class='date-posts'>
      <div class='post-outer'>

        <div class='post hentry uncustomized-post-template'>

          <a expr:id='data:post.id'/>
          <b:if cond='data:post.title'>
            <h3 class='post-title entry-title'>
              <b:if cond='data:post.link'>
                <a expr:href='data:post.link'><data:post.title/></a>
              <b:elseif cond='data:post.url and data:blog.url != data:post.url'/>
                <a expr:href='data:post.url'><data:post.title/></a>
              <b:else/>
                <data:post.title/>
              </b:if>
            </h3>
          </b:if>

          <div class='post-header'>
            <div class='post-header-line-1'/>
          </div>

          <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id'>
            <data:post.body/>
            <div style='clear: both;'/> <!-- clear for photos floats -->
          </div>

          <div class='post-footer'>
            <div class='post-footer-line post-footer-line-1'>
              <span class='post-author'>
                <b:if cond='data:top.showAuthor'>
                  <b:if cond='data:post.authorProfileUrl'>
                      <a expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                        <data:post.author/>
                      </a>
                  <b:else/>
                      <data:post.author/>
                  </b:if>
                </b:if>
              </span>

              <span class='post-timestamp'>
                <b:if cond='data:top.showTimestamp'>
                  <data:top.timestampLabel/>
                  <b:if cond='data:post.url'>
                    <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><span class='published' expr:title='data:post.timestampISO8601'><data:post.timestamp/></span></a>
                  </b:if>
                </b:if>
              </span>

              <span class='post-comment-link'>
                <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                                  and data:post.allowComments' data='post' name='comment_count_picker'/>
              </span>
            </div>

            <div class='post-footer-line post-footer-line-2'>
              <b:if cond='data:top.showMobileShare'>
                <div class='mobile-link-button goog-inline-block' id='mobile-share-button'>
                  <a href='javascript:void(0);'><data:shareMsg/></a>
                </div>
              </b:if>
              <b:if cond='data:top.showDummy'>
                <div class='goog-inline-block dummy-container'><data:post.dummyTag/></div>
              </b:if>
            </div>

          </div>
        </div>

        <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
      </div>
    </div>
  </div>
</b:includable>
       <b:includable id='nextprev'>
 <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
        <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><data:newerPageTitle/></a>
      </span>
    </b:if>
    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
        <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>
          Load More
        </a>
      </span>
    </b:if>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    <b:if cond='data:mobileLinkUrl'>
      <div class='blog-mobile-link'>
        <a expr:href='data:mobileLinkUrl'><data:mobileLinkMsg/></a>
      </div>
    </b:if>
  </div>
  <div class='clear'/>
</b:includable>
       <b:includable id='post' var='post'>  
  <div class='post'>
    <b:if cond='data:blog.pageType in {&quot;item&quot;,&quot;index&quot;}'>
	&lt;div itemscope=&#39;itemscope&#39; itemtype=&#39;http://schema.org/Blog&#39;&gt;
	</b:if>  
	<b:switch var='data:blog.pageType'>
	<b:case value='static_page'/>
	<!-- Posting halaman statis -->
	    <b:if cond='data:post.title'>
          <h1 class='post-title entry-title'>
            <b:if cond='data:post.link'>
              <a expr:href='data:post.link'><data:post.title/></a>
            <b:else/>
              <b:if cond='data:post.url'>
                <b:if cond='data:blog.url != data:post.url'>
                  <a expr:href='data:post.url'><data:post.title/></a>
                <b:else/>
                  <data:post.title/>
                </b:if>
                <b:else/>
                  <data:post.title/>
              </b:if>
            </b:if>
          </h1>
		</b:if>
		<div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id'>
			<div id='body-post-it'>
			<data:post.body/>
			</div>
	<div style='clear: both;'/> 
	</div>	
	<script>
	if (typeof(BLOG_attachCsiOnload) != &#39;undefined&#39; &amp;&amp; BLOG_attachCsiOnload != null) { window[&#39;blogger_templates_experiment_id&#39;] = &quot;templatesV1&quot;;window[&#39;blogger_blog_id&#39;] = &#39;<data:blog.blogId/>&#39;;BLOG_attachCsiOnload(&#39;&#39;); }_WidgetManager._Init(&#39;//www.blogger.com/rearrange?blogIDx3d<data:blog.blogId/>&#39;,&#39;<data:blog.homepageUrl/>&#39;,&#39;<data:blog.blogId/>&#39;);
	_WidgetManager._RegisterWidget(&#39;_ContactFormView&#39;, new _WidgetInfo(&#39;ContactForm1&#39;, &#39;footer1&#39;, null, document.getElementById(&#39;ContactForm1&#39;), {&#39;contactFormMessageSendingMsg&#39;: &#39;Sending...&#39;, &#39;contactFormMessageSentMsg&#39;: &#39;Your message has been sent.&#39;, &#39;contactFormMessageNotSentMsg&#39;: &#39;Message could not be sent. Please try again later.&#39;, &#39;contactFormInvalidEmailMsg&#39;: &#39;A valid email address is required.&#39;, &#39;contactFormEmptyMessageMsg&#39;: &#39;Message field cannot be empty.&#39;, &#39;title&#39;: &#39;Contact Form&#39;, &#39;blogId&#39;: &#39;<data:blog.blogId/>&#39;, &#39;contactFormNameMsg&#39;: &#39;Name&#39;, &#39;contactFormEmailMsg&#39;: &#39;Email&#39;, &#39;contactFormMessageMsg&#39;: &#39;Message&#39;, &#39;contactFormSendMsg&#39;: &#39;Send&#39;, &#39;submitUrl&#39;: &#39;https://www.blogger.com/contact-form.do&#39;}, &#39;displayModeFull&#39;));
	</script> 	
	  <b:case value='item'/>
	  <!-- Posting halaman item -->
    <a alt='Kembali' class='bckbtn' href='/' title='kembali'><svg style='width:22px;height:22px' viewBox='0 0 24 24'>
<path d='M20,11V13H8L13.5,18.5L12.08,19.92L4.16,12L12.08,4.08L13.5,5.5L8,11H20Z' fill='#fff'/></svg></a>
	  <b:if cond='data:post.firstImageUrl'>
		<meta expr:content='data:post.firstImageUrl' itemprop='image'/>
	  </b:if>
	  <meta expr:content='data:post.snippet' itemprop='description'/>
	  <a expr:id='data:post.id'/>
		<div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id'>
	    <b:if cond='data:post.title'>
		<b:if cond='data:post.url'>
		  <meta expr:content='data:post.url.canonical' itemprop='url'/>
		</b:if>
	<div class='maxwidht--'><div class='firstimage--'>
<b:if cond='data:post.firstImageUrl'>
<img class='lazyload' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.firstImageUrl, 900)' expr:data-srcset='resizeImage(data:post.firstImageUrl, 900)' expr:src='resizeImage(data:post.firstImageUrl, 1)' expr:title='data:post.title'/>
<b:else/>
<img class='firstimage' expr:alt='data:post.title' src='https://res.cloudinary.com/practicaldev/image/fetch/s--DIr6g6vv--/f_auto,fl_progressive,q_auto,w_auto/https://1.bp.blogspot.com/-8iwc70zdPfg/XoeWd_PgAsI/AAAAAAAAEtE/P1Gd2XH40g0jJN5IlJNH8I0DBgyAW_kbACLcBGAsYHQ/s640/dog-4977599_1280-picsay.jpg'/></b:if></div>
<b:if cond='data:post.firstImageUrl'><style>#wrapper {background: url(https://res.cloudinary.com/practicaldev/image/fetch/s--DIr6g6vv--/f_auto,fl_progressive,q_auto,w_10/<data:post.firstImageUrl/>) no-repeat center center;background-size: cover;max-width:100%}</style></b:if>
      <a name='details'/>
<b:if cond='data:post.labels'><b:loop values='data:post.labels' var='label'><b:if cond='data:label.name == &quot;Live&quot;'><style>.firstimage-- {display: none;}#jwpopupLink {display: none;}</style></b:if></b:loop></b:if>
         <b:if cond='data:post.labels'><b:loop values='data:post.labels' var='label'><b:if cond='data:label.name == &quot;Video&quot;'><style>.firstimage-- {display: none;}#jwpopupLink {display: none;}</style></b:if></b:loop></b:if>
  </div>
		</b:if>
		<div class='postwrapper-artikel'>
                           <div class='menubtm'>
                             <a class='btnlook download-wall' expr:alt='&quot;Download Wallpaper &quot; + data:post.title' expr:title='&quot;Download Wallpaper &quot; + data:post.title' href='javascript:void(0);' id='jwpopupLink' style='color: black;display: flex;'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M5,20H19V18H5M19,9H15V3H9V9H5L12,16L19,9Z' fill='currentColor'/></svg></a>
<a class='btndwnld hartomy-bookmark-btn' data-quantity='1' expr:alt='&quot;Download Wallpaper &quot; + data:post.title' expr:data-borkimage='resizeImage(data:post.firstImageUrl, 800)' expr:data-id='data:post.id' expr:data-link='data:post.url' expr:data-title='data:post.title' href='javascript:void(0);' style='color: white;display: flex;'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M17,18L12,15.82L7,18V5H17M17,3H7A2,2 0 0,0 5,5V21L12,18L19,21V5C19,3.89 18.1,3 17,3Z' fill='currentColor'/></svg></a>
            <a class='btn btn-outline-secondary js-share' expr:aria-label='data:post.title' expr:data-text='data:post.title' expr:data-title='data:post.title' expr:data-url='data:post.url' href='#'>
<svg style='width: 34px;height: 34px;transition: all .3s ease;' viewBox='0 0 24 24'><path d='M16,12A2,2 0 0,1 18,10A2,2 0 0,1 20,12A2,2 0 0,1 18,14A2,2 0 0,1 16,12M10,12A2,2 0 0,1 12,10A2,2 0 0,1 14,12A2,2 0 0,1 12,14A2,2 0 0,1 10,12M4,12A2,2 0 0,1 6,10A2,2 0 0,1 8,12A2,2 0 0,1 6,14A2,2 0 0,1 4,12Z'/></svg>
</a>
</div>
<div class='title-wrapper'><h1 class='post-title entry-title' itemprop='headline'><b:if cond='data:post.url'><data:post.title/></b:if></h1></div>
<div class='post-dates'><abbr class='updated timeago' expr:title='data:post.timestampISO8601'><data:post.timestamp/></abbr></div>
<div class='lang-iklanpost' id='iklan-lang'><div id='iklan-atas-artikel'/></div>
<div class='article-more'><data:post.body/></div>
<div class='lang-iklanpost' id='iklan-lang'><div id='iklan-bawah-artikel'/></div>
     
          <b:include name='shareButtons'/>
	  <b:include data='posts' name='breadcrumb'/>
          </div>
          <div class='jwpopup' id='jwpopupBox'>
<div class='jwpopup-content'>
<div class='jwpopup-head'>
<h2>Download Wallpaper</h2>
<a class='closee' href='#' onclick='hide(&apos;jwpopupBox&apos;)'><svg class='close' style='width:30px;height: 30px;transition: all .3s ease;' viewBox='0 0 24 24'><path d='M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z'/></svg></a>
</div>
  <div class='iklan-download'>
    	<!-- IKLAN DALAM BOX DOWNLOAD -->
<div class='iklantext'/>
  </div>
  <div class='wp-jwpopup'>
<button class='btnlook download-wall' id='wp-btn' onclick='generate()'>Download</button>
<a class='btnlook download-wall' expr:alt='&quot;Download Wallpaper &quot; + data:post.title' expr:download='resizeImage(data:post.firstImageUrl, 1200)' expr:href='resizeImage(data:post.firstImageUrl, 1200) + &quot;-d&quot;' expr:title='&quot;Download Wallpaper &quot; + data:post.title' id='wp-count' style='color: black;display:none;margin:auto'>Download</a>

</div>
              <div class='iklan-download'>
                    	<!-- IKLAN DALAM BOX DOWNLOAD -->
  </div>

            </div>
            
</div>
		<div style='clear: both;'/>		
      </div>  
      
	<b:default/>
	<!-- Posting halaman default (index, arsip, dll.) -->
	  <b:include data='post' name='postthumbnail'/>
	  <b:if cond='data:post.firstImageUrl'>
		<meta expr:content='data:post.firstImageUrl' itemprop='image'/>
	  </b:if>
	  <meta expr:content='data:post.snippet' itemprop='description'/>
	  <a expr:id='data:post.id'/>
		  <meta expr:content='data:post.url.canonical' itemprop='url'/>
	</b:switch>
	
    <b:if cond='data:blog.pageType in {&quot;item&quot;,&quot;index&quot;}'>
	&lt;/div&gt;
    </b:if>
	
	<div style='clear: both;'/> 
   </div>
</b:includable>
       <b:includable id='postQuickEdit' var='post'>
  <b:if cond='data:post.editUrl'>
    <span expr:class='&quot;item-control &quot; + data:post.adminClass'>
	<span class='edit-post'>
      <a expr:href='data:post.editUrl' expr:title='data:top.editPostMsg'>
		<strong>Edit</strong>
      </a>
	</span>
    </span>
  </b:if>
</b:includable>
       <b:includable id='postcommentinfo' var='post'>
<b:if cond='data:post.allowComments'>
  <span class='comment-info'>
  <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'> <b:if cond='data:post.numComments == 0'> Add Comment </b:if> <b:if cond='data:post.numComments == 1'> 1 Comment </b:if> <b:if cond='data:post.numComments &gt; 1'> <data:post.numComments/> Comments </b:if> 
  </a>
  </span>
</b:if>
</b:includable>
       <b:includable id='postcommentinfo2' var='post'>
<b:if cond='data:post.allowComments'>
  <span class='comment-info'>
  <a expr:onclick='data:post.addCommentOnclick' href='#comment-form'> <b:if cond='data:post.numComments == 0'> Add Comment </b:if> <b:if cond='data:post.numComments == 1'> 1 Comment </b:if> <b:if cond='data:post.numComments &gt; 1'> <data:post.numComments/> Comments </b:if> 
  </a>
  </span>
</b:if>
</b:includable>
       <b:includable id='postdateinfo' var='post'>
<b:if cond='data:post.dateHeader'>
 <span class='time-info'><span class='updated published' expr:title='data:post.timestampISO8601'>
 <meta expr:content='data:post.timestampISO8601'/>
  <data:post.dateHeader/>
 </span></span>
<b:else/>
<b:if cond='data:top.showTimestamp'>
 <span class='time-info'><span class='updated published' expr:title='data:post.timestampISO8601'>
 <meta expr:content='data:post.timestampISO8601'/>
  <data:post.timestamp/>
 </span></span>
</b:if>
</b:if>
</b:includable>
       <b:includable id='postlabelinfo' var='post'>
<b:if cond='data:post.labels'>
  <span class='label-info'>
  <b:loop values='data:post.labels' var='label'>
	<a expr:href='data:label.url' rel='tag'><data:label.name/></a><b:if cond='data:label.isLast != &quot;true&quot;'/>
  </b:loop>
  </span>
</b:if>
</b:includable>
       <b:includable id='postthumbnail' var='post'>
  <a expr:alt='data:post.title' expr:href='data:post.url' expr:title='data:post.title'>
	<div class='img-thumbnail'>
  <b:if cond='data:post.thumbnailUrl'>
	<img class='lazyload' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.thumbnailUrl, 900)' expr:src='resizeImage(data:post.thumbnailUrl, 1)' expr:title='data:post.title'/>
  <b:else/>
	<b:if cond='data:post.firstImageUrl'>
	<img class='lazyload' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.firstImageUrl, 900)' expr:src='resizeImage(data:post.firstImageUrl, 1)' expr:title='data:post.title'/>
  <b:else/>
	<img expr:alt='data:post.title' expr:title='data:post.title' src='//3.bp.blogspot.com/-ltyYh4ysBHI/U04MKlHc6pI/AAAAAAAADQo/PFxXaGZu9PQ/w300-h375-c/no-image.png'/>
  </b:if> 
  </b:if>
      <b:if cond='data:post.labels'><b:loop values='data:post.labels' var='label'><div class='PyenC'><span expr:class='data:label.name'/></div></b:loop></b:if>
</div>
  </a>
	<div class='title-image'>
      <h1 itemprop='name'><data:post.title/></h1> 
            <a class='btn btn-outline-secondary js-share' expr:aria-label='data:post.title' expr:data-text='data:post.title' expr:data-title='data:post.title' expr:data-url='data:post.url' href='#'>
	<svg style='width: 24px;height: 24px;transition: all .3s ease;' viewBox='0 0 24 24'><path d='M16,12A2,2 0 0,1 18,10A2,2 0 0,1 20,12A2,2 0 0,1 18,14A2,2 0 0,1 16,12M10,12A2,2 0 0,1 12,10A2,2 0 0,1 14,12A2,2 0 0,1 12,14A2,2 0 0,1 10,12M4,12A2,2 0 0,1 6,10A2,2 0 0,1 8,12A2,2 0 0,1 6,14A2,2 0 0,1 4,12Z'/></svg></a></div>

    <div class='media-left hidden'>
<figure class='image'><img alt='author' class='imgaes lazyload' expr:data-src='resizeImage(data:post.authorPhoto.url, 96)' expr:data-srcset='resizeImage(data:post.authorPhoto.url, 40)' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/></figure>
<div class='is-4' itemprop='name'><span class='authorposts'><data:post.author/></span></div>
</div>
</b:includable>
       <b:includable id='relatedpost' var='post'>
<div class='related-post' expr:id='&quot;related-post-&quot; + data:post.id'/>
</b:includable>
       <b:includable id='shareButtons' var='post'>
			<div class='bagikan'>
                              <a class='fb' expr:href='&quot;https://www.facebook.com/sharer/sharer.php?u=&quot; + data:blog.canonicalUrl' target='_blank' title='Bagikan di Facebook'><svg viewBox='0 0 64 64'><path d='M20.1,36h3.4c0.3,0,0.6,0.3,0.6,0.6V58c0,1.1,0.9,2,2,2h7.8c1.1,0,2-0.9,2-2V36.6c0-0.3,0.3-0.6,0.6-0.6h5.6 c1,0,1.9-0.7,2-1.7l1.3-7.8c0.2-1.2-0.8-2.4-2-2.4h-6.6c-0.5,0-0.9-0.4-0.9-0.9v-5c0-1.3,0.7-2,2-2h5.9c1.1,0,2-0.9,2-2V6.2 c0-1.1-0.9-2-2-2h-7.1c-13,0-12.7,10.5-12.7,12v7.3c0,0.3-0.3,0.6-0.6,0.6h-3.4c-1.1,0-2,0.9-2,2v7.8C18.1,35.1,19,36,20.1,36z'/></svg></a> 

                              <a class='twitter' expr:href='&quot;https://twitter.com/intent/tweet?text=&quot; + data:post.title + &quot;&amp;amp;url=&quot; + data:blog.canonicalUrl' target='_blank' title='Bagikan di Twitter'><svg viewBox='0 0 64 64'><path d='M11.4,26.6C11.5,26.6,11.5,26.6,11.4,26.6c-0.9,0-1.8-0.2-2.6-0.4c-1.3-0.4-2.5,0.8-2.1,2 c1.1,4.3,4.5,7.7,8.8,8.6c-1,0.3-2,0.4-3,0.4c-1,0-1.7,1.1-1.2,2c1.9,3.5,5.6,5.9,9.7,6h1c1.1,0,2,0.9,2,2c0,1.1-0.9,2-2,2 c-1.3,0-2.9-0.1-4.5-0.5c-1-0.2-2-0.2-2.9,0.1c-1.7,0.6-3.5,1.1-5.4,1.3C8.5,50.2,8,50.7,8,51.4v0c0,0.5,0.3,1,0.8,1.2 c3.9,1.7,8.3,2.7,12.9,2.7c21.1,0,32.7-17.9,32.7-33.5v0c0-0.9,0.4-1.8,1.1-2.4c1.2-1,2.3-2.1,3.3-3.4c0.4-0.5-0.1-1.2-0.7-1 c-1.2,0.4-2.4,0.7-3.7,0.9c-0.2,0-0.3-0.2-0.1-0.4c1.5-1.1,2.8-2.6,3.6-4.3c0.3-0.6-0.3-1.2-0.9-0.9c-1.1,0.6-2.3,1-3.5,1.4 c-1.2,0.4-2.6,0.1-3.6-0.7c-1.9-1.5-4.4-2.4-7-2.4c-5.3,0-9.8,3.7-11.1,8.8c-0.2,0.9,0.5,1.7,1.4,1.7c1.6-0.1,3.2-0.3,4.4-0.5 c1-0.2,2,0.3,2.4,1.2c0.5,1.2-0.2,2.4-1.3,2.7c-4.6,1.3-9.7,0.4-9.7,0.4l0,0C21.2,21.8,14.3,18,9.3,12.5C8.6,11.7,7.3,12,7,12.9 c-0.4,1.2-0.6,2.5-0.6,3.9C6.4,20.9,8.4,24.5,11.4,26.6z'/></svg></a> 

                              <a class='pinterest' expr:href='&quot;https://www.blogger.com/share-post.g?blogID=&quot; + data:blog.blogId + &quot;&amp;postID=&quot; + data:post.id + &quot;&amp;target=pinterest&quot;'><svg viewBox='0 0 64 64'><path d='M14.4,53.8c2.4,2,6.1,0.6,6.8-2.4l0-0.1c0.4-1.8,2.4-10.2,3.2-13.7c0.2-0.9,0.2-1.8-0.1-2.7 C24.2,34,24,32.8,24,31.5c0-4.1,2.4-7.2,5.4-7.2c2.5,0,3.8,1.9,3.8,4.2c0,2.6-1.6,6.4-2.5,9.9c-0.7,3,1.5,5.4,4.4,5.4 c5.3,0,8.9-6.8,8.9-14.9c0-6.1-4.1-10.7-11.6-10.7c-8.5,0-13.8,6.3-13.8,13.4c0,2.4,0.7,4.2,1.8,5.5c0.5,0.6,0.6,0.9,0.4,1.6 c-0.1,0.5-0.4,1.8-0.6,2.2c-0.2,0.7-0.8,1-1.4,0.7c-3.9-1.6-5.7-5.9-5.7-10.7c0-8,6.7-17.5,20-17.5c10.7,0,17.7,7.7,17.7,16 c0,11-6.1,19.2-15.1,19.2c-1.9,0-3.8-0.7-5.2-1.6c-0.9-0.6-2.1-0.1-2.4,0.9c-0.5,1.9-1.1,4.3-1.3,4.9c-0.1,0.5-0.3,0.9-0.4,1.4 c-1,2.7,0.9,5.5,3.7,5.7c2.1,0.1,4.2,0,6.3-0.3c12.4-2,22.1-12.2,23.4-24.7C61.5,18.1,48.4,4,32,4C16.5,4,4,16.5,4,32 C4,40.8,8.1,48.6,14.4,53.8z'/></svg></a>

                              <a class='whatsapp' data-action='share/whatsapp/share' expr:href='&quot;whatsapp://send?text=&quot; + data:post.title + &quot; - &quot; + data:blog.canonicalUrl'><svg viewBox='0 0 64 64'><path d='M6.9,48.4c-0.4,1.5-0.8,3.3-1.3,5.2c-0.7,2.9,1.9,5.6,4.8,4.8l5.1-1.3c1.7-0.4,3.5-0.2,5.1,0.5 c4.7,2.1,10,3,15.6,2.1c12.3-1.9,22-11.9,23.5-24.2C62,17.3,46.7,2,28.5,4.2C16.2,5.7,6.2,15.5,4.3,27.8c-0.8,5.6,0,10.9,2.1,15.6 C7.1,44.9,7.3,46.7,6.9,48.4z M21.3,19.8c0.6-0.5,1.4-0.9,1.8-0.9s2.3-0.2,2.9,1.2c0.6,1.4,2,4.7,2.1,5.1c0.2,0.3,0.3,0.7,0.1,1.2 c-0.2,0.5-0.3,0.7-0.7,1.1c-0.3,0.4-0.7,0.9-1,1.2c-0.3,0.3-0.7,0.7-0.3,1.4c0.4,0.7,1.8,2.9,3.8,4.7c2.6,2.3,4.9,3,5.5,3.4 c0.7,0.3,1.1,0.3,1.5-0.2c0.4-0.5,1.7-2,2.2-2.7c0.5-0.7,0.9-0.6,1.6-0.3c0.6,0.2,4,1.9,4.7,2.2c0.7,0.3,1.1,0.5,1.3,0.8 c0.2,0.3,0.2,1.7-0.4,3.2c-0.6,1.6-2.1,3.1-3.2,3.5c-1.3,0.5-2.8,0.7-9.3-1.9c-7-2.8-11.8-9.8-12.1-10.3c-0.3-0.5-2.8-3.7-2.8-7.1 C18.9,22.1,20.7,20.4,21.3,19.8z'/></svg></a>
                            </div></b:includable>
       <b:includable id='status-message'>
  <b:if cond='data:navMessage'>
  <div class='status-msg-wrap'>
    <div class='status-msg-body'>
      <data:navMessage/>
    </div>
    <div class='status-msg-border'>
      <div class='status-msg-bg'>
        <div class='status-msg-hidden'><data:navMessage/></div>
      </div>
    </div>
  </div>
  <div style='clear: both;'/>
  </b:if>
</b:includable>
       <b:includable id='threaded-comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <div class='pesan-komentar'><p><data:blogCommentMessage/></p></div>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <div class='pesan-komentar'><p><data:blogCommentMessage/></p></div>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;, &#39;<data:post.communityId/>&#39;);
    </script>
  </div>
</b:includable>
       <b:includable id='threaded_comment_js' var='post'>
  <script async='async' expr:src='data:post.commentSrc'/>

  <script>
    (function() {
      var items = <data:post.commentJso/>;
      var msgs = <data:post.commentMsgs/>;
      var config = <data:post.commentConfig/>;

// <![CDATA[
      var cursor = null;
      if (items && items.length > 0) {
        cursor = parseInt(items[items.length - 1].timestamp) + 1;
      }

      var bodyFromEntry = function(entry) {
        if (entry.gd$extendedProperty) {
          for (var k in entry.gd$extendedProperty) {
            if (entry.gd$extendedProperty[k].name == 'blogger.contentRemoved') {
              return '<span class="deleted-comment">' + entry.content.$t + '</span>';
            }
          }
        }
        return entry.content.$t;
      }

      var parse = function(data) {
        cursor = null;
        var comments = [];
        if (data && data.feed && data.feed.entry) {
          for (var i = 0, entry; entry = data.feed.entry[i]; i++) {
            var comment = {};
            // comment ID, parsed out of the original id format
            var id = /blog-(\d+).post-(\d+)/.exec(entry.id.$t);
            comment.id = id ? id[2] : null;
            comment.body = bodyFromEntry(entry);
            comment.timestamp = Date.parse(entry.published.$t) + '';
            if (entry.author && entry.author.constructor === Array) {
              var auth = entry.author[0];
              if (auth) {
                comment.author = {
                  name: (auth.name ? auth.name.$t : undefined),
                  profileUrl: (auth.uri ? auth.uri.$t : undefined),
                  avatarUrl: (auth.gd$image ? auth.gd$image.src : undefined)
                };
              }
            }
            if (entry.link) {
              if (entry.link[2]) {
                comment.link = comment.permalink = entry.link[2].href;
              }
              if (entry.link[3]) {
                var pid = /.*comments\/default\/(\d+)\?.*/.exec(entry.link[3].href);
                if (pid && pid[1]) {
                  comment.parentId = pid[1];
                }
              }
            }
            comment.deleteclass = 'item-control blog-admin';
            if (entry.gd$extendedProperty) {
              for (var k in entry.gd$extendedProperty) {
                if (entry.gd$extendedProperty[k].name == 'blogger.itemClass') {
                  comment.deleteclass += ' ' + entry.gd$extendedProperty[k].value;
                } else if (entry.gd$extendedProperty[k].name == 'blogger.displayTime') {
                  comment.displayTime = entry.gd$extendedProperty[k].value;
                }
              }
            }
            comments.push(comment);
          }
        }
        return comments;
      };

      var paginator = function(callback) {
        if (hasMore()) {
          var url = config.feed + '?alt=json&v=2&orderby=published&reverse=false&max-results=50';
          if (cursor) {
            url += '&published-min=' + new Date(cursor).toISOString();
          }
          window.bloggercomments = function(data) {
            var parsed = parse(data);
            cursor = parsed.length < 50 ? null
                : parseInt(parsed[parsed.length - 1].timestamp) + 1
            callback(parsed);
            window.bloggercomments = null;
          }
          url += '&callback=bloggercomments';
          var script = document.createElement('script');
          script.type = 'text/javascript';
          script.src = url;
          document.getElementsByTagName('head')[0].appendChild(script);
        }
      };
      var hasMore = function() {
        return !!cursor;
      };
      var getMeta = function(key, comment) {
        if ('iswriter' == key) {
          var matches = !!comment.author
              && comment.author.name == config.authorName
              && comment.author.profileUrl == config.authorUrl;
          return matches ? 'true' : '';
        } else if ('deletelink' == key) {
          return config.baseUri + '/delete-comment.g?blogID='
               + config.blogId + '&postID=' + comment.id;
        } else if ('deleteclass' == key) {
          return comment.deleteclass;
        }
        return '';
      };

      var replybox = null;
      var replyUrlParts = null;
      var replyParent = undefined;

      var onReply = function(commentId, domId) {
        if (replybox == null) {
          // lazily cache replybox, and adjust to suit this style:
          replybox = document.getElementById('comment-editor');
          if (replybox != null) {
            replybox.height = '250px';
            replybox.style.display = 'block';
            replyUrlParts = replybox.src.split('#');
          }
        }
        if (replybox && (commentId !== replyParent)) {
          document.getElementById(domId).insertBefore(replybox.parentNode, null);
          replybox.src = replyUrlParts[0]
              + (commentId ? '&parentID=' + commentId : '')
              + '#' + replyUrlParts[1];
          replyParent = commentId;
        }
      };

      var hash = (window.location.hash || '#').substring(1);
      var startThread, targetComment;
      if (/^comment-form_/.test(hash)) {
        startThread = hash.substring('comment-form_'.length);
      } else if (/^c[0-9]+$/.test(hash)) {
        targetComment = hash.substring(1);
      }

      // Configure commenting API:
      var configJso = {
        'maxDepth': config.maxThreadDepth
      };
      var provider = {
        'id': config.postId,
        'data': items,
        'loadNext': paginator,
        'hasMore': hasMore,
        'getMeta': getMeta,
        'onReply': onReply,
        'rendered': true,
        'initComment': targetComment,
        'initReplyThread': startThread,
        'config': configJso,
        'messages': msgs
      };

      var render = function() {
        if (window.goog && window.goog.comments) {
          var holder = document.getElementById('comment-holder');
          window.goog.comments.render(holder, provider);
        }
      };

      // render now, or queue to render when library loads:
      if (window.goog && window.goog.comments) {
        render();
      } else {
        window.goog = window.goog || {};
        window.goog.comments = window.goog.comments || {};
        window.goog.comments.loadQueue = window.goog.comments.loadQueue || [];
        window.goog.comments.loadQueue.push(render);
      }
    })();
// ]]>
  </script>
</b:includable>
       <b:includable id='threaded_comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
      <div class='judul-review'><h3><b:if cond='data:post.numComments == 0'>Komentar (0)</b:if> <b:if cond='data:post.numComments == 1'>Komentar (1)</b:if> <b:if cond='data:post.numComments &gt; 1'>Komentar (<data:post.numComments/>)</b:if></h3></div>

    <div class='comments-content'>
      <b:if cond='data:post.embedCommentForm'>
        <b:include data='post' name='threaded_comment_js'/>
      </b:if>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threaded-comment-form'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:if cond='data:post.showBacklinks'>
         <b:include data='post' name='backlinks'/>
       </b:if>
    </div>
    </div>
  </div>
</b:includable>
     </b:widget>
     <b:widget id='HTML5' locked='true' title='IKLAN ATAS FOOTER' type='HTML' version='2' visible='true'>
       <b:widget-settings>
         <b:widget-setting name='content'/>
       </b:widget-settings>
       <b:includable id='main'>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
     </b:widget>
     <b:widget cond='data:view.isPost' id='HTML1' locked='true' title='Iklan Atas Artikel' type='HTML' version='2' visible='true'>
       <b:widget-settings>
         <b:widget-setting name='content'/>
       </b:widget-settings>
       <b:includable id='main'>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<div id='iklan-lang'>
  <div class='widget-content' id='atas-post'>
    <data:content/>
  </div>
</div>
</b:if>
</b:includable>
     </b:widget>
     <b:widget cond='data:view.isPost' id='HTML3' locked='true' title='Iklan Bawah Artikel' type='HTML' version='2' visible='true'>
       <b:widget-settings>
         <b:widget-setting name='content'/>
       </b:widget-settings>
       <b:includable id='main'>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<div id='iklan-lang'>
  <div class='widget-content' id='bawah-post'>
    <data:content/>
  </div>
</div>
</b:if>
</b:includable>
     </b:widget>
   </b:section>
  </div>

  </div>
  <div class='clear'/>
  <!-- post wrapper end -->
  </div>
  <!-- wrapper end -->
  <aside id='widget-footer-container'>
    <div id='widget-footer-wrapper'>
    <b:section class='widget-footer' id='widget-footer' preferred='yes'>
      <b:widget id='PopularPosts1' locked='false' title='Postingan Populer' type='PopularPosts' version='1'>
        <b:widget-settings>
          <b:widget-setting name='numItemsToShow'>9</b:widget-setting>
          <b:widget-setting name='showThumbnails'>true</b:widget-setting>
          <b:widget-setting name='showSnippets'>false</b:widget-setting>
          <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'><h2><data:title/></h2></b:if>
  <div class='widget-content popular-posts'>
    <ul>
      <b:loop index='x' values='data:posts' var='post'>
        <b:if cond='data:x == 2'>
 	 <li class='iklan-pop'>
    <!-- IKLAN POPULER POST -->      
          <div class='item-thumbnail-only'>
            <div class='iklantext' style='min-height: 200px;border-radius: 10px;'/>
  			</div>
          </li>
        </b:if>
        
        
      <li>
        <b:if cond='!data:showThumbnails'>
          <b:if cond='!data:showSnippets'>
            <!-- (1) No snippet/thumbnail -->
            <a expr:href='data:post.href'><data:post.title/></a>
          <b:else/>
            <!-- (2) Show only snippets -->
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <div class='item-snippet'><data:post.snippet/></div>
          </b:if>
        <b:else/>
          <!-- (3) Show only thumbnails or (4) Snippets and thumbnails. -->
          <div expr:class='data:showSnippets ? &quot;item-content&quot; : &quot;item-thumbnail-only&quot;'>
                <a expr:href='data:post.href'>
            <b:if cond='data:post.featuredImage.isResizable or data:post.thumbnail'>
              <div class='img-thumbnail-popular'>
                  <b:with value='data:post.featuredImage.isResizable                                  ? resizeImage(data:post.featuredImage, 300): data:post.thumbnail' var='image'>
                    <img expr:alt='data:post.title' expr:src='data:image'/></b:with>
            <div class='title-image-popular'><h3><data:post.title/></h3></div></div></b:if>
            <b:if cond='data:showSnippets'>
              <div class='item-snippet'><data:post.snippet/></div>
            </b:if>
                </a>
          </div>
        </b:if>
      </li>
      </b:loop>
    </ul>
  </div>
</b:includable>
      </b:widget>
    </b:section>
    </div>
  </aside>
  <div class='clear'/>
  <b:include cond='data:view.isPost' name='iklan-lang_dalampost'/>
  <!-- footer widget -->
  <b:if cond='data:view.isMultipleItems'>
<div class='menubottom'>
      <nav>
        <ul>
          <li><a expr:href='data:blog.homepageUrl' expr:title='data:messages.home' itemprop='url'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z'/>
</svg><span itemprop='name'><data:messages.home/></span></a></li>
          <li><a class='toggleMenu' href='javascript:void(0);' itemprop='url' title='Menu'><svg height='24' viewBox='0 0 24 24' width='24'><path d='M6,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM16,6c0,1.1 0.9,2 2,2s2,-0.9 2,-2 -0.9,-2 -2,-2 -2,0.9 -2,2zM12,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2z'/></svg><span itemprop='name'>Menu</span></a></li>
          <li class='ripple buka-tutup'><a href='javascript:void(0);' itemprop='url' title='Tersimpan'><svg style='width:24px;height:24px' viewBox='0 0 24 24'><path d='M17,3H7A2,2 0 0,0 5,5V21L12,18L19,21V5C19,3.89 18.1,3 17,3Z'/></svg><span itemprop='name'>Tersimpan</span></a></li>
        </ul>
      </nav>
    </div>
  </b:if>
<nav class='dropdowns' itemprop='mainEntity' itemscope='itemscope' itemtype='http://schema.org/SiteNavigationElement'>
<div class='wrapper'>
<div class='menu-btn menu-btn-close toggleMenu hidden' onclick='closeMenu()'><div class='bar_1'/><div class='bar_2'/><div class='bar_3'/></div>
  <div class='penjudul'><data:blog.title/></div>
<b:section id='Main Menu' preferred='yes' showaddelement='fasle'>
  <b:widget id='Label3' locked='true' title='Label' type='Label' version='1'>
    <b:widget-settings>
      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
      <b:widget-setting name='display'>LIST</b:widget-setting>
      <b:widget-setting name='selectedLabelsList'/>
      <b:widget-setting name='showType'>ALL</b:widget-setting>
      <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
    <b:if cond='data:display == &quot;list&quot;'>
	<ul class='nav-menu2'>
		<li><a expr:href='data:blog.homepageUrl' title='Beranda'><svg viewBox='0 0 24 24'><path d='M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z'/></svg><data:messages.home/></a></li>
        <b:loop values='data:labels' var='label'>
          <li>
            <b:if cond='data:blog.url == data:label.url'>
		<a class='actv' expr:dir='data:blog.languageDirection' expr:href='data:label.url'><svg viewBox='0 0 24 24'><path d='M3,5A2,2 0 0,1 5,3H19A2,2 0 0,1 21,5V19A2,2 0 0,1 19,21H5C3.89,21 3,20.1 3,19V5M7,18H9L9.35,16H13.35L13,18H15L15.35,16H17.35L17.71,14H15.71L16.41,10H18.41L18.76,8H16.76L17.12,6H15.12L14.76,8H10.76L11.12,6H9.12L8.76,8H6.76L6.41,10H8.41L7.71,14H5.71L5.35,16H7.35L7,18M10.41,10H14.41L13.71,14H9.71L10.41,10Z'/></svg><data:label.name/></a>
            <b:else/>
              <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><svg viewBox='0 0 24 24'><path d='M3,5A2,2 0 0,1 5,3H19A2,2 0 0,1 21,5V19A2,2 0 0,1 19,21H5C3.89,21 3,20.1 3,19V5M7,18H9L9.35,16H13.35L13,18H15L15.35,16H17.35L17.71,14H15.71L16.41,10H18.41L18.76,8H16.76L17.12,6H15.12L14.76,8H10.76L11.12,6H9.12L8.76,8H6.76L6.41,10H8.41L7.71,14H5.71L5.35,16H7.35L7,18M10.41,10H14.41L13.71,14H9.71L10.41,10Z'/></svg><data:label.name/></a>
            </b:if>
            <b:if cond='data:showFreqNumbers'>
              <span dir='ltr'>(<data:label.count/>)</span>
            </b:if>
          </li>
        </b:loop>
      </ul>
    <b:else/>
      <b:loop values='data:labels' var='label'>
        <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
          <b:if cond='data:blog.url == data:label.url'>
            <li expr:dir='data:blog.languageDirection'><data:label.name/></li>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span class='label-count' dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </span>
      </b:loop>
    </b:if>
  </div>
</b:includable>
  </b:widget>
  <b:widget id='LinkList1' locked='true' title='Halaman' type='LinkList' version='2' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='sorting'>NONE</b:widget-setting>
      <b:widget-setting name='text-1'>Privacy Policy</b:widget-setting>
      <b:widget-setting name='link-1'>#</b:widget-setting>
      <b:widget-setting name='text-0'>Terms Of Service</b:widget-setting>
      <b:widget-setting name='link-0'>#</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
    <b:includable id='content'>
 <div class='widget-content'>
	<ul class='nav-menu2'>
     <b:loop values='data:links' var='link'>
       <li><a expr:href='data:link.target' expr:title='data:link.name'><data:link.name/></a></li>
     </b:loop>
   </ul>
 </div>
</b:includable>
    <b:includable id='widget-title'>
</b:includable>
  </b:widget>
</b:section>

</div>
</nav>
<b:defaultmarkups>
	<b:defaultmarkup type='Common'>
		<b:includable id='iklan-lang_dalampost'>
<script type='text/javascript'>
   var atas = document.getElementById(&#39;iklan-atas-artikel&#39;);
   var isiatas = document.getElementById(&#39;atas-post&#39;);
   atas.appendChild(isiatas);

   var bawah = document.getElementById(&#39;iklan-bawah-artikel&#39;);
   var isibawah = document.getElementById(&#39;bawah-post&#39;);
   bawah.appendChild(isibawah);
</script>
		</b:includable>
		<b:includable id='allJavascriptThemes'>
<b:if cond='data:view.isMultipleItems'>
  <script> //<![CDATA[
  // Infinite Scroll Blogger
  !function(ignielScroll) {
    var auto = false; // true atau false
    var img = 'https://4.bp.blogspot.com/-a8y2WkWKzU0/W90DTo4X29I/AAAAAAAAG2c/5FWxJt9VaYUM7Mz-bH0emW3A50lJxCltQCLcBGAs/s1600/igniel-loading.gif';
    eval(function(p,a,c,k,e,d){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--){d[e(c)]=k[c]||e(c)}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('B a=["\\v\\t\\c\\d\\f\\i\\g\\m\\f\\b\\e","\\I\\t\\c\\d\\f\\i\\g\\d\\k\\l\\k","\\e\\b\\D\\d\\G\\b","\\v\\t\\c\\d\\f\\i\\g\\m\\f\\b\\e\\i\\j\\b\\U\\b\\e\\i\\c\\h\\j\\w","\\y\\h\\j\\p","\\n\\c\\h\\n\\w","\\v\\t\\c\\d\\f\\i\\g\\m\\f\\b\\e\\i\\d\\c\\p\\b\\e\\i\\c\\h\\j\\w\\F\\m","\\r\\e\\b\\y","\\c\\b\\j\\f\\l\\r","\\I\\g\\d\\k\\l","\\s\\p\\h\\G\\u\\s\\C\\p\\h\\G\\u","\\r\\l\\D\\c","\\m\\g\\g\\b\\j\\p","\\n\\c\\d\\j\\b","\\v\\t\\c\\d\\f\\i\\g\\m\\f\\b\\e\\i\\d\\c\\p\\b\\e\\i\\c\\h\\j\\w","\\f\\b\\l","\\s\\k\\g\\m\\j\\u\\s\\h\\D\\f\\F\\k\\e\\n\\P\\J","\\J\\C\\u\\s\\C\\k\\g\\m\\j\\u","\\e\\b\\g\\c\\m\\n\\b\\Y\\h\\l\\r","\\d\\j","\\k\\n\\e\\d\\c\\c\\F\\e\\b\\k\\h\\O\\b","\\k\\n\\e\\d\\c\\c\\N\\d\\g","\\r\\b\\h\\f\\r\\l","\\l\\d\\g","\\d\\y\\y\\k\\b\\l","\\l\\e\\h\\f\\f\\b\\e"];B q=o(a[0]),K=o(a[1]),z=L;q[a[4]](a[3])[a[2]](),q[a[19]](a[5],a[6],E(){1c o[a[15]](x[a[7]],{},E(A){B H=o(A)[a[4]](a[9])[a[8]]?o(A):o(a[10]);K[a[12]](H[a[4]](a[1])[a[11]]()),q[a[11]](H[a[4]](a[14])[a[13]]());z=L},a[11]),o(x)[a[18]](a[16]+Z+a[17]),!1});M(1a){$(1b)[a[19]](a[W],E(){M(!z&&($(x)[a[V]]()+$(x)[a[R]]())>=q[a[Q]]()[a[S]]){q[a[4]](a[6])[a[T]](a[5]);z=X}})}',62,75,'||||||||||_0x143a|x65|x6C|x6F|x72|x67|x70|x69|x2D|x6E|x73|x74|x61|x63|ignielScroll|x64|pager|x68|x3C|x62|x3E|x23|x6B|this|x66|loading|_0x5348x4|var|x2F|x6D|function|x20|x76|_0x5348x5|x2E|x22|post|false|if|x54|x7A|x3D|24|22|23|25|x77|21|20|true|x57|img|||||||||||auto|window|return'.split('|'),0,{}));
  }(jQuery);

const rightBtn = document.querySelector('#right-button');
const leftBtn = document.querySelector('#left-button');

rightBtn.addEventListener("click", function(event) {
  const conent = document.querySelector('#Label1 .cloud-label-widget-content');
  conent.scrollLeft += 300;
  event.preventDefault();
});

leftBtn.addEventListener("click", function(event) {
  const conent = document.querySelector('#Label1 .cloud-label-widget-content');
  conent.scrollLeft -= 300;
  event.preventDefault();
});

  //]]> </script>
</b:if>
<script type='text/javascript'>
//<![CDATA[
jQuery(window).scroll(function(){jQuery(window).scrollTop()>40?jQuery(".menurekom").addClass("scrolled"):jQuery(".menurekom").removeClass("scrolled")});
// Sub Nav
var Script=function(){jQuery('.nav-menu2 .sub-menu > a').click(function(){var last=jQuery('.sub-menu.open',$('.nav-menu2'));last.removeClass("open");jQuery('.dropdown').addClass("open");jQuery('.dropdown',last).removeClass("open");jQuery('.sub',last).slideUp(300);var sub=jQuery(this).next();if(sub.is(":visible")){jQuery('.dropdown',jQuery(this)).removeClass("open");jQuery(this).parent().removeClass("open");sub.slideUp(300)}else{jQuery('.dropdown',jQuery(this)).addClass("open");jQuery(this).parent().addClass("open");sub.slideDown(300)}var o=($(this).offset());diff=300-o.top;if(diff>0)$(".nav-menu2").scrollTo("-="+Math.abs(diff),500);else $(".nav-menu2").scrollTo("+="+Math.abs(diff),500)})}();
$(function(){var e=$(document).scrollTop();var t=$(".menubottom").outerHeight();$(window).scroll(function(){var n=$(document).scrollTop();if($(document).scrollTop()>=50){$(".menubottom").css("position","fixed")}else{$(".menubottom").css("position","fixed")}if(n>t){$(".menubottom").addClass("scroll-1")}else{$(".menubottom").removeClass("scroll-1")}if(n>e){$(".menubottom").removeClass("scroll-bottom")}else{$(".menubottom").addClass("scroll-bottom")}e=$(document).scrollTop()})})
$(document).ready(function(){$(".toggleMenu").click(function(){$("html").addClass("lock");});});
$(document).ready(function(){$(".darkshadow, .menu-btn-close").click(function(){$("html").removeClass("lock");});});
$(document).ready(function(){$(".toggleMenu").click(function(){$(".dropdowns").toggleClass("shows");});});
$(document).ready(function(){$(".darkshadow").click(function(){$(".dropdowns").removeClass("shows");});});
$(document).ready(function(){$(".darkshadow").click(function(){$(".darkshadow").removeClass("shows");});});
$(document).ready(function(){$(".toggleMenu").click(function(){$(".darkshadow").toggleClass("shows");});});
function LazyOnScroll(){setTimeout(function(){function e(){for(var e=document.getElementsByClassName("lazy"),t=0;t<e.length;t++)n=e[t],void 0,0<=(o=n.getBoundingClientRect()).bottom&&0<=o.right&&o.top<=(window.innerHeight||document.documentElement.clientHeight)&&o.left<=(window.innerWidth||document.documentElement.clientWidth)&&(e[t].src=e[t].getAttribute("data-src"));var n,o,i;i=document.querySelectorAll(".lds-ripple"),[].forEach.call(i,function(e){e.classList.remove("lds-ripple")})}function t(e,t){window.addEventListener?window.addEventListener(e,t):window.attachEvent("on"+e,t)}t("load",e),t("scroll",e),document.addEventListener("DOMContentLoaded",function(){"use strict";for(var e=document.querySelectorAll("a"),t=e.length,u=/firefox|trident/i.test(navigator.userAgent)?document.documentElement:document.body;t--;)e.item(t).addEventListener("click",function(e){var c,l=u.scrollTop,t=document.getElementById(/[^#]+$/.exec(this.href)[0]).getBoundingClientRect().top,n=u.scrollHeight-window.innerHeight,r=l+t<n?t:n-l,a=function(e){var t,n,o,i=e-(c=c||e),d=(t=i,n=l,o=r,(t/=900/2)<1?o/2*t*t*t+n:o/2*((t-=2)*t*t+2)+n);u.scrollTop=d,i<900&&requestAnimationFrame(a)};requestAnimationFrame(a),e.preventDefault()})})},1e3)}window.addEventListener?window.addEventListener("load",LazyOnScroll,!1):window.attachEvent?window.attachEvent("onload",LazyOnScroll):window.onload=LazyOnScroll;
document.addEventListener("load", function() {let lazyImages = [].slice.call(document.querySelectorAll("img.lazy")); let active = false; const lazyLoad = function() {if (active === false) {active = true; setTimeout(function() {lazyImages.forEach(function(lazyImage) {if ((lazyImage.getBoundingClientRect().top <= window.innerHeight && lazyImage.getBoundingClientRect().bottom >= 0) && getComputedStyle(lazyImage).display !== "none") {lazyImage.src = lazyImage.dataset.src; lazyImage.srcset = lazyImage.dataset.srcset; lazyImage.classList.remove("lazy"); lazyImages = lazyImages.filter(function(image) {return image !== lazyImage;}); if (lazyImages.length === 0) {document.removeEventListener("scroll", lazyLoad); window.removeEventListener("resize", lazyLoad); window.removeEventListener("orientationchange", lazyLoad); } } }); active = false;}, 200);} }; document.addEventListener("scroll", lazyLoad); window.addEventListener("resize", lazyLoad); window.addEventListener("orientationchange", lazyLoad); });
!function(a,b){var c=b(a,a.document,Date);a.lazySizes=c,"object"==typeof module&&module.exports&&(module.exports=c)}("undefined"!=typeof window?window:{},function(a,b,c){"use strict";var d,e;if(function(){var b,c={lazyClass:"lazyload",loadedClass:"lazyloaded",loadingClass:"lazyloading",preloadClass:"lazypreload",errorClass:"lazyerror",autosizesClass:"lazyautosizes",srcAttr:"data-src",srcsetAttr:"data-srcset",sizesAttr:"data-sizes",minSize:40,customMedia:{},init:!0,expFactor:1.5,hFac:.8,loadMode:2,loadHidden:!0,ricTimeout:0,throttleDelay:125};e=a.lazySizesConfig||a.lazysizesConfig||{};for(b in c)b in e||(e[b]=c[b])}(),!b||!b.getElementsByClassName)return{init:function(){},cfg:e,noSupport:!0};var f=b.documentElement,g=a.HTMLPictureElement,h="addEventListener",i="getAttribute",j=a[h].bind(a),k=a.setTimeout,l=a.requestAnimationFrame||k,m=a.requestIdleCallback,n=/^picture$/i,o=["load","error","lazyincluded","_lazyloaded"],p={},q=Array.prototype.forEach,r=function(a,b){return p[b]||(p[b]=new RegExp("(\\s|^)"+b+"(\\s|$)")),p[b].test(a[i]("class")||"")&&p[b]},s=function(a,b){r(a,b)||a.setAttribute("class",(a[i]("class")||"").trim()+" "+b)},t=function(a,b){var c;(c=r(a,b))&&a.setAttribute("class",(a[i]("class")||"").replace(c," "))},u=function(a,b,c){var d=c?h:"removeEventListener";c&&u(a,b),o.forEach(function(c){a[d](c,b)})},v=function(a,c,e,f,g){var h=b.createEvent("Event");return e||(e={}),e.instance=d,h.initEvent(c,!f,!g),h.detail=e,a.dispatchEvent(h),h},w=function(b,c){var d;!g&&(d=a.picturefill||e.pf)?(c&&c.src&&!b[i]("srcset")&&b.setAttribute("srcset",c.src),d({reevaluate:!0,elements:[b]})):c&&c.src&&(b.src=c.src)},x=function(a,b){return(getComputedStyle(a,null)||{})[b]},y=function(a,b,c){for(c=c||a.offsetWidth;c<e.minSize&&b&&!a._lazysizesWidth;)c=b.offsetWidth,b=b.parentNode;return c},z=function(){var a,c,d=[],e=[],f=d,g=function(){var b=f;for(f=d.length?e:d,a=!0,c=!1;b.length;)b.shift()();a=!1},h=function(d,e){a&&!e?d.apply(this,arguments):(f.push(d),c||(c=!0,(b.hidden?k:l)(g)))};return h._lsFlush=g,h}(),A=function(a,b){return b?function(){z(a)}:function(){var b=this,c=arguments;z(function(){a.apply(b,c)})}},B=function(a){var b,d=0,f=e.throttleDelay,g=e.ricTimeout,h=function(){b=!1,d=c.now(),a()},i=m&&g>49?function(){m(h,{timeout:g}),g!==e.ricTimeout&&(g=e.ricTimeout)}:A(function(){k(h)},!0);return function(a){var e;(a=!0===a)&&(g=33),b||(b=!0,e=f-(c.now()-d),e<0&&(e=0),a||e<9?i():k(i,e))}},C=function(a){var b,d,e=99,f=function(){b=null,a()},g=function(){var a=c.now()-d;a<e?k(g,e-a):(m||f)(f)};return function(){d=c.now(),b||(b=k(g,e))}},D=function(){var g,m,o,p,y,D,F,G,H,I,J,K,L=/^img$/i,M=/^iframe$/i,N="onscroll"in a&&!/(gle|ing)bot/.test(navigator.userAgent),O=0,P=0,Q=0,R=-1,S=function(a){Q--,(!a||Q<0||!a.target)&&(Q=0)},T=function(a){return null==K&&(K="hidden"==x(b.body,"visibility")),K||!("hidden"==x(a.parentNode,"visibility")&&"hidden"==x(a,"visibility"))},U=function(a,c){var d,e=a,g=T(a);for(G-=c,J+=c,H-=c,I+=c;g&&(e=e.offsetParent)&&e!=b.body&&e!=f;)(g=(x(e,"opacity")||1)>0)&&"visible"!=x(e,"overflow")&&(d=e.getBoundingClientRect(),g=I>d.left&&H<d.right&&J>d.top-1&&G<d.bottom+1);return g},V=function(){var a,c,h,j,k,l,n,o,q,r,s,t,u=d.elements;if((p=e.loadMode)&&Q<8&&(a=u.length)){for(c=0,R++;c<a;c++)if(u[c]&&!u[c]._lazyRace)if(!N||d.prematureUnveil&&d.prematureUnveil(u[c]))ba(u[c]);else if((o=u[c][i]("data-expand"))&&(l=1*o)||(l=P),r||(r=!e.expand||e.expand<1?f.clientHeight>500&&f.clientWidth>500?500:370:e.expand,d._defEx=r,s=r*e.expFactor,t=e.hFac,K=null,P<s&&Q<1&&R>2&&p>2&&!b.hidden?(P=s,R=0):P=p>1&&R>1&&Q<6?r:O),q!==l&&(D=innerWidth+l*t,F=innerHeight+l,n=-1*l,q=l),h=u[c].getBoundingClientRect(),(J=h.bottom)>=n&&(G=h.top)<=F&&(I=h.right)>=n*t&&(H=h.left)<=D&&(J||I||H||G)&&(e.loadHidden||T(u[c]))&&(m&&Q<3&&!o&&(p<3||R<4)||U(u[c],l))){if(ba(u[c]),k=!0,Q>9)break}else!k&&m&&!j&&Q<4&&R<4&&p>2&&(g[0]||e.preloadAfterLoad)&&(g[0]||!o&&(J||I||H||G||"auto"!=u[c][i](e.sizesAttr)))&&(j=g[0]||u[c]);j&&!k&&ba(j)}},W=B(V),X=function(a){var b=a.target;if(b._lazyCache)return void delete b._lazyCache;S(a),s(b,e.loadedClass),t(b,e.loadingClass),u(b,Z),v(b,"lazyloaded")},Y=A(X),Z=function(a){Y({target:a.target})},$=function(a,b){try{a.contentWindow.location.replace(b)}catch(c){a.src=b}},_=function(a){var b,c=a[i](e.srcsetAttr);(b=e.customMedia[a[i]("data-media")||a[i]("media")])&&a.setAttribute("media",b),c&&a.setAttribute("srcset",c)},aa=A(function(a,b,c,d,f){var g,h,j,l,m,p;(m=v(a,"lazybeforeunveil",b)).defaultPrevented||(d&&(c?s(a,e.autosizesClass):a.setAttribute("sizes",d)),h=a[i](e.srcsetAttr),g=a[i](e.srcAttr),f&&(j=a.parentNode,l=j&&n.test(j.nodeName||"")),p=b.firesLoad||"src"in a&&(h||g||l),m={target:a},s(a,e.loadingClass),p&&(clearTimeout(o),o=k(S,2500),u(a,Z,!0)),l&&q.call(j.getElementsByTagName("source"),_),h?a.setAttribute("srcset",h):g&&!l&&(M.test(a.nodeName)?$(a,g):a.src=g),f&&(h||l)&&w(a,{src:g})),a._lazyRace&&delete a._lazyRace,t(a,e.lazyClass),z(function(){var b=a.complete&&a.naturalWidth>1;p&&!b||(b&&s(a,"ls-is-cached"),X(m),a._lazyCache=!0,k(function(){"_lazyCache"in a&&delete a._lazyCache},9)),"lazy"==a.loading&&Q--},!0)}),ba=function(a){if(!a._lazyRace){var b,c=L.test(a.nodeName),d=c&&(a[i](e.sizesAttr)||a[i]("sizes")),f="auto"==d;(!f&&m||!c||!a[i]("src")&&!a.srcset||a.complete||r(a,e.errorClass)||!r(a,e.lazyClass))&&(b=v(a,"lazyunveilread").detail,f&&E.updateElem(a,!0,a.offsetWidth),a._lazyRace=!0,Q++,aa(a,b,f,d,c))}},ca=C(function(){e.loadMode=3,W()}),da=function(){3==e.loadMode&&(e.loadMode=2),ca()},ea=function(){if(!m){if(c.now()-y<999)return void k(ea,999);m=!0,e.loadMode=3,W(),j("scroll",da,!0)}};return{_:function(){y=c.now(),d.elements=b.getElementsByClassName(e.lazyClass),g=b.getElementsByClassName(e.lazyClass+" "+e.preloadClass),j("scroll",W,!0),j("resize",W,!0),j("pageshow",function(a){if(a.persisted){var c=b.querySelectorAll("."+e.loadingClass);c.length&&c.forEach&&l(function(){c.forEach(function(a){a.complete&&ba(a)})})}}),a.MutationObserver?new MutationObserver(W).observe(f,{childList:!0,subtree:!0,attributes:!0}):(f[h]("DOMNodeInserted",W,!0),f[h]("DOMAttrModified",W,!0),setInterval(W,999)),j("hashchange",W,!0),["focus","mouseover","click","load","transitionend","animationend"].forEach(function(a){b[h](a,W,!0)}),/d$|^c/.test(b.readyState)?ea():(j("load",ea),b[h]("DOMContentLoaded",W),k(ea,2e4)),d.elements.length?(V(),z._lsFlush()):W()},checkElems:W,unveil:ba,_aLSL:da}}(),E=function(){var a,c=A(function(a,b,c,d){var e,f,g;if(a._lazysizesWidth=d,d+="px",a.setAttribute("sizes",d),n.test(b.nodeName||""))for(e=b.getElementsByTagName("source"),f=0,g=e.length;f<g;f++)e[f].setAttribute("sizes",d);c.detail.dataAttr||w(a,c.detail)}),d=function(a,b,d){var e,f=a.parentNode;f&&(d=y(a,f,d),e=v(a,"lazybeforesizes",{width:d,dataAttr:!!b}),e.defaultPrevented||(d=e.detail.width)&&d!==a._lazysizesWidth&&c(a,f,e,d))},f=function(){var b,c=a.length;if(c)for(b=0;b<c;b++)d(a[b])},g=C(f);return{_:function(){a=b.getElementsByClassName(e.autosizesClass),j("resize",g)},checkElems:g,updateElem:d}}(),F=function(){!F.i&&b.getElementsByClassName&&(F.i=!0,E._(),D._())};return k(function(){e.init&&F()}),d={cfg:e,autoSizer:E,loader:D,init:F,uP:w,aC:s,rC:t,hC:r,fire:v,gW:y,rAF:z}});

//]]>
</script>
<script>
//<![CDATA[
var massgEmpty='Tekan <svg height="20" viewBox="0 0 24 24" width="20" style="vertical-align: middle;"><path style="fill: black;" d="M17,18L12,15.82L7,18V5H17M17,3H7A2,2 0 0,0 5,5V21L12,18L19,21V5C19,3.89 18.1,3 17,3Z" fill="#fff"></path></svg> untuk menyimpan gambar favorit kamu!';!function($){"use strict";var OptionManager=(objToReturn={},defaultOptions={bookmarkIcon:"bookmarkIcon",bookmarkBadge:"show-bookmark",articleQuantity:"article-quantity",affixBookmarkIcon:!0,showBookmarkModal:!0,clickOnAddToBookmark:function(t){},clickOnbookmarkIcon:function(t,a){}},objToReturn.getOptions=function(t){var a=$.extend({},defaultOptions);return"object"==typeof t&&$.extend(a,t),a},objToReturn),objToReturn,defaultOptions,articleManager=function(){var t={};localStorage.konten=localStorage.konten?localStorage.konten:"";var a=function(t){localStorage.konten=JSON.stringify(t)},e=function(){try{return JSON.parse(localStorage.konten)}catch(t){return[]}},o=function(t,o){var n=function(t){var a=-1,o=e();return $.each(o,function(e,o){o.id!=t||(a=e)}),a}(t);if(n<0)return!1;var i=e();return i[n].quantity=void 0===o?i[n].quantity:o,a(i),!0};return t.getAllkonten=e,t.updatePoduct=o,t.setarticle=function(t,n,i,r,l,c){return void 0===t?(console.error("id required"),!1):void 0===n?(console.error("title required"),!1):void 0===i?(console.error("link required"),!1):void 0===c?(console.error("borkimage required"),!1):(r=void 0===r?"":r,void(o(t)||function(t,o,n,i,r,l){var c=e();c.push({id:t,title:o,link:n,summary:i,quantity:r,borkimage:l}),a(c)}(t,n,i,r,l,c)))},t.cleararticle=function(){a([])},t.removearticle=function(t){var o=e();o=$.grep(o,function(a,e){return a.id!=t}),a(o)},t.getTotalQuantity=function(){var t=0,a=e();return $.each(a,function(a,e){t+=e.quantity}),t},t}(),loadBookmarkEvent=function(t){var a=OptionManager.getOptions(t),e=$("."+a.bookmarkIcon),o=$("."+a.bookmarkBadge),n=a.articleQuantity;o.text(articleManager.getTotalQuantity()),$("#cart-modal").length||$("body").append('<div class="pop-area" id="cart-modal"><div class="pop-html"><div class="head-pop"><span>Gambar Disimpan</span><a class="close-btn buka-tutup"><svg style="width:24px;height:24px" viewBox="0 0 24 24"><path d="M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z"/></svg></a></div><div class="table-responsive" id="cart-table"></div></div></div>');var i=function(){var t=$("#cart-table");t.empty();var a=articleManager.getAllkonten();$.each(a,function(){t.append('<div class="table-bookmark"><table class="table"><tbody><tr title="'+this.summary+'" data-id="'+this.id+'"><td class="img-left"><a href="'+this.link+'"><img src="'+this.borkimage+'"/></a></td><td class="item-left"><a href="'+this.link+'">'+this.title+'</a></td><td class="item-remove" title="Remove favorit" class="text-center" style="width: 30px;"><a class="btn-remove"><svg width="16px" height="16px" viewBox="0 0 16 16" class="bi bi-trash-fill text-danger" fill="#fff"><path fill-rule="evenodd" d="M2.5 1a1 1 0 0 0-1 1v1a1 1 0 0 0 1 1H3v9a2 2 0 0 0 2 2h6a2 2 0 0 0 2-2V4h.5a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H10a1 1 0 0 0-1-1H7a1 1 0 0 0-1 1H2.5zm3 4a.5.5 0 0 1 .5.5v7a.5.5 0 0 1-1 0v-7a.5.5 0 0 1 .5-.5zM8 5a.5.5 0 0 1 .5.5v7a.5.5 0 0 1-1 0v-7A.5.5 0 0 1 8 5zm3 .5a.5.5 0 0 0-1 0v7a.5.5 0 0 0 1 0v-7z"/></svg></a></td></tr></tbody></table></div>')}),t.append(a.length?"":'<div role="alert" id="cart-empty-message"><div class="text-center"><div class="svg-msg"><svg width="80" height="80" viewBox="0 0 24 24"><path fill="currentColor" d="M17,3A2,2 0 0,1 19,5V21L12,18L5,21V5C5,3.89 5.9,3 7,3H17M11,14L17.25,7.76L15.84,6.34L11,11.18L8.41,8.59L7,10L11,14Z" /></svg></div><div class="massgEmpty">'+massgEmpty+"</div></div></div>")};if(a.affixBookmarkIcon){var r=1*e.offset().top+1*e.css("height").match(/\d+/);$(window).scroll(function(){$(window).scrollTop()>=r?e.addClass("bookmarkIcon-affix"):e.removeClass("bookmarkIcon-affix")})}e.click(function(){a.showBookmarkModal?i():a.clickOnbookmarkIcon(e,articleManager.getAllkonten())}),$(document).on("keypress","."+n,function(t){38!=t.keyCode&&40!=t.keyCode&&t.preventDefault()}),$(document).on({click:function(){var t=$(this).closest("tr"),a=t.data("id");t.hide(500,function(){articleManager.removearticle(a),i(),o.text(articleManager.getTotalQuantity())})}},".btn-remove")};$(document).on({click:function(){return $(".pop-area").toggleClass("open"),!1}},".buka-tutup"),$(function(){var goTohartomyBookmark=function(t){};eval(function(t,a,e,o,n,i){if(n=function(t){return(t<58?"":n(parseInt(t/58)))+((t%=58)>35?String.fromCharCode(t+29):t.toString(36))},!"".replace(/^/,String)){for(;e--;)i[n(e)]=o[e]||n(e);o=[function(t){return i[t]}],n=function(){return"\\w+"},e=1}for(;e--;)o[e]&&(t=t.replace(new RegExp("\\b"+n(e)+"\\b","g"),o[e]));return t}('q h=["\\B\\e\\M","\\g\\r\\k\\E\\i\\v\\l\\l\\w\\m\\n\\e\\e\\f\\j\\g\\i\\f","\\x\\y\\f\\g\\C\\k\\y\\k\\y\\F","\\N\\z\\g\\i\\k\\e\\j\\G\\C\\x\\e\\e\\f\\j\\g\\i\\f\\C\\x\\k\\m","\\H\\z\\A\\r\\k","\\F\\y\\H\\z","\\s\\t\\s","\\s\\t\\O","\\s\\t\\P","\\z\\g\\i\\k\\e\\j\\G\\n\\e\\e\\f\\j\\g\\i\\f","\\s\\t\\Q"];q D=[h[0],h[1],h[2],h[3]];(o(b,c){q d=o(a){R(--a){b[h[5]](b[h[4]]())}};d(++c)}(D,S));q u=o(a,b){a=a-I;q c=D[a];T c};$(u(h[U]))[h[9]]({\'\\x\\e\\e\\f\\j\\g\\i\\f\\J\\p\\e\\m\':u(h[6]),\'\\g\\r\\r\\A\\t\\n\\e\\e\\f\\j\\g\\i\\f\\J\\p\\e\\m\':!I,\'\\p\\B\\A\\p\\f\\w\\m\\v\\l\\l\\K\\e\\n\\e\\e\\f\\j\\g\\i\\f\':o(a){L(a)},\'\\g\\r\\k\\E\\i\\v\\l\\l\\w\\m\\n\\e\\e\\f\\j\\g\\i\\f\':o(a){V[u(h[8])](u(h[7]),a)},\'\\p\\B\\A\\p\\f\\w\\m\\v\\l\\l\\K\\e\\n\\e\\e\\f\\j\\g\\i\\f\':o(a){L(a)}})',0,58,"||||||||||||||x6F|x6B|x61|_0x6a0a|x72|x6D|x74|x64|x6E|x42|function|x63|var|x66|x30|x78|_0x3889|x41|x4F|x62|x75|x68|x69|x6C|x2D|_0x4117|x65|x70|x79|x73|0x0|x49|x54|goTohartomyBookmark|x67|x2E|x33|x32|x31|while|0xd6|return|10|console".split("|"),0,{}))});var MyBookmark=function(t,a){var e=$(t),o=OptionManager.getOptions(a),n=$("."+o.bookmarkBadge);e.click(function(){o.clickOnAddToBookmark(e);var t=e.data("id"),a=e.data("title"),i=e.data("link"),r=e.data("summary"),l=e.data("quantity"),c=e.data("borkimage");articleManager.setarticle(t,a,i,r,l,c),n.text(articleManager.getTotalQuantity())})};$.fn.hartomyBookmark=function(t){return loadBookmarkEvent(t),$.each(this,function(){new MyBookmark(this,t)})}}(jQuery);
//]]>
</script>
          <script>
//<![CDATA[
function darkMode(){localStorage.setItem("mode","darkmode"===localStorage.getItem("mode")?"light":"darkmode"),"darkmode"===localStorage.getItem("mode")?document.querySelector("#mainContent").classList.add("darkMode"):document.querySelector("#mainContent").classList.remove("darkMode")};
   //]]>
</script>
<script src='https://cdn.fyi.my.id/assets/js/wpx-share.min.js'/>
<script type='text/javascript'> //<![CDATA[ 
document.addEventListener('click',(evt)=>{const share=evt.target.closest('.js-share');if(!share){return}
if(!share.dataset.title){return}
navigator.share({title:share.dataset.title,text:share.dataset.text,url:share.dataset.url||location.href});evt.preventDefault()})
//]]>
          </script>
  <b:if cond='data:view.isPost'>
    <script type='text/javascript'> //<![CDATA[ 
function hide(target) {
    document.getElementById(target).style.display = 'none';
}
var jwpopup = document.getElementById('jwpopupBox');
var mpLink = document.getElementById("jwpopupLink");
var close = document.getElementsByClassName("closes")[0];
mpLink.onclick = function() {
    jwpopup.style.display = "flex";
}
closes.onclick = function() {
    jwpopup.style.display = "none";
}

window.onclick = function(event) {
    if (event.target == jwpopup) {
        jwpopup.style.display = "none";
    }
}
function generate() {
    var linkDL = document.getElementById("wp-count"),
        btn = document.getElementById("wp-btn"),
        direklink = document.getElementById("wp-count").href,
        waktu = 10;
    var teks_waktu = document.createElement("span");
    linkDL.parentNode.replaceChild(teks_waktu, linkDL);
    var id;
    id = setInterval(function () {
        waktu--;
        if (waktu < 0) {
            teks_waktu.parentNode.replaceChild(linkDL, teks_waktu);
            clearInterval(id);
            window.location.replace(direklink);
            linkDL.style.display = "inline";
   
        } else {
            teks_waktu.innerHTML = "File siap diunduh dalam " + "" + waktu.toString() + " Detik....";
            btn.style.display = "none";
        }
    }, 1000);
}

//]]>
  </script>
    <script type='text/javascript'> //<![CDATA[ 
$(document).ready(function(){$(".menubtm").click(function(){$(".hartomy-bookmark-btn").fadeOut(function(){$(".hartomy-bookmark-btn").text("Simpan"==$(".hartomy-bookmark-btn").text()?"Saved":"Saved").fadeIn()})})});
//]]>
  </script>
    <script type='text/javascript'>
/*<![CDATA[*/
$(document).ready(function(){$('a[name="details"]').before($('#live-wallpaper').html());$('#live-wallpaper').html('')});
/*]]>*/
</script>
  </b:if>
          
		</b:includable>
</b:defaultmarkup>
</b:defaultmarkups>	
<b:include name='allJavascriptThemes'/>
  &lt;!--</body>--&gt;&lt;/body&gt;
</html>
