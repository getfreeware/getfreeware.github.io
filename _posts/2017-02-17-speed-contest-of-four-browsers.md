---
layout: default
title: 四大浏览器内核引擎网页载入速度大比武
published: true
author: gro
comments: true
date: 2008-02-12 03:02:45
tags: [ ]
categories:
    - app
permalink: /2008/02/12/speed-contest-of-four-browsers.html
---
对于普通的用户来说, 网页浏览器最重要的一项指标就是速度,而页面的载入和渲染速度有是这速度指标中重要的一环,虽然浏览器速度还包含Javascript脚本的速度,CSS 显示的速度,但对于用户来说,怎样最快速的将网页上的文字和图片信息显示出来是非常重要的, 所以本文就讨论一下我们经常使用的浏览器对于网页文字和图片的载入速度做一个比较.
  
当前浏览器界存在着四大浏览器引擎,即Trident, Gecko, Presto 和 KHTML,这里我们选择了这四大引擎在Windows上的相应代表:



Trident:
  
IE7.0
  
外壳浏览器 The World 2.1 Lite
  
Gecko:
  
Firefox 3.x
  
Firefox 2.x
  
K-Meleon (CCF ME 0.08)
  
Presto:
  
Opera 9.5
  
KHTML:
  
Safari 3.1
  
然后我们就分别比较一下这些浏览器对于网页文字和图片的载入和渲染速度的表现
  
**(1) 文字载入速度**
  
一个最简单的文字载入测试页面最能说明问题:
  

  
这个测试所采用的Javascript时间计算源码在这里:
  
var then = (new Date()).getTime();
  
function endT() {
  
var now=(new Date()).getTime();
  
loadT=now-then;
  
document.getElementById(&#8216;loadingtime&#8217;).innerHTML += &#8216;Load time:&#8217;+loadT+'ms&#8217;;
  
}
  
这个脚本对于任何浏览器都是公正的，不存在偏袒任何一个浏览器的问题.
  
经过多次的反复测试结果(每一次测试都需要删除之前的历史数据),得到了如下的结果:

[][1]

**(2) 图片载入速度**
  
使用于文字测试页面相同的JS时间计算代码，我们采用了这个测试页面:
  
[http://speedtesting.4qh.info][2]
  
测试了各个浏览器载入Google图片的载入和渲染速度，我们得到了各浏览器图片速度的比较:

[][3]

**(3) 结论**
  
Trident引擎:
  
IE7.0 及其外壳浏览器显示了微软在浏览器引擎上依然很有功力，在文字的载入方面更是如此，IE 7.0是载入文字速度最快的浏览器，使用IE引擎的外壳浏览器The World也显示非常好的性能，在图片载入速度方面虽然不如Gecko引擎的浏览器，不过依然大幅领先于Safari和Opera浏览器，然而我们在实际使用中发现，IE引擎在载入很多图片的页面时，内存的使用效率很低，导致反应速度很慢的问题，反而在载入多图片的页面时不如Safari和Opera等浏览器, 如果IE引擎能够克服这个缺点，将来还是依然能很有作为。
  
Gecko 引擎:
  
这个开源协议下浏览器引擎非常出色，经过了众多程序员的努力之后，在文字和图片的载入渲染方面都显示了强大的效能, K-Meleon是仅此于IE7的显示文字速度最快的浏览器，而且也是显示图片速度最快的浏览器。Firefox 由于使用了多平台的XUL结构，虽然在Windows上的效能不如K-Meleon, 不过依然表现了非常快的速度，在图片的载入和显示速度方面, Gecko引擎超过了所有其它任何引擎的浏览器。
  
Presto 引擎:
  
Opera 这款在网络上评价很高的浏览器在这次的测试中显示了非常令人失望的结果，无论是文字和图片的载入速度方面，都是最慢的，然而我们也发现这款浏览器对于缓存的利用方面非常不错，虽然网页文字和图片的载入速度都很慢，但是只要是访问过的页面，Opera和很快的显示出来, 这可能也是为什么网络上称赞Opera速度较快的原因吧。不过Opera在此次测试中体现的低效能让人非常担心它今后的表现。
  
KHTML 引擎:
  
Safari 这款浏览器暂时还是Windows平台上新客人, Safari在Mac平台上的速度和性能是有口皆碑的，然而在Windows平台，我们发现它还有很长的一段路要走，虽然在文字页面的显示速度上, Safari相当地快，然而在图片的载入和渲染方面也显示出了它的缺陷，仅快于Opera。所以如果Safari想在Windows平台上有所作为，它还有很多工作需要去做。
  
最后，这篇文章只是针对网页浏览器在文字和图片载入以及渲染速度方面的测评，用户在使用浏览器方面还应当考虑到很多其它的因素，比如用户界面，使用方便程度和扩展功能等等。希望这篇拙文抛砖引玉，能够让大家对于四大浏览器引擎有更深的认识。

 [1]: http://getfreeware.net/wp-content/uploads/2008/02/1-152312.jpg
 [2]: http://speedtesting.4qh.info/
 [3]: http://getfreeware.net/wp-content/uploads/2008/02/2-152323.jpg