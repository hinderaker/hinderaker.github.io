---
layout: post
title: 18 forskjellige favicons = høy oppløsning, for alle!
tags: "favicon, internett"
published: true
---

[Favicons][FaviconLink] var et kult tillegg til [Internet](http://no.wikipedia.org/wiki/Internett) når det ble introdusert i Mars 1999. På den tiden var verden noe enklere og `favicon.ico` var den eneste filen du trengte for at [Internet Explorer 5](http://no.wikipedia.org/wiki/Internet_Explorer) skulle vise _ikonet_ med høyest mulig oppløsning. Senere samme år ble konseptet adoptert som en standard både av industrien og av W3C.

I dag derimot er historien litt annerledes. Denne nettsiden for eksempel har totalt 18 _"forskjellige"_ [favicons][FaviconLink]. Flere av dem fordi [Apple](http://no.wikipedia.org/wiki/Apple) bestemte seg for ikke å benytte standarden `rel="icon"` og i stedet laget sin egen versjon i form av `rel="apple-touch-icon"`. Etter å ha laget det samme _ikonet_ i 17 forskjellige størrelser og konvertert det i `64x64` fra `.png` til `.ico` måtte jeg inkludere 20 linjer med kode for å få dem alle til å virke.

{% highlight css linenos %}
<link rel="shortcut icon" href="{{ site.baseurl }}/public/favicon.ico">
<link rel="icon" sizes="16x16 32x32 64x64" href="{{ site.baseurl }}/public/favicon.ico">
<link rel="icon" type="image/png" sizes="196x196" href="{{ site.baseurl }}/public/favicon-192.png">
<link rel="icon" type="image/png" sizes="160x160" href="{{ site.baseurl }}/public/favicon-160.png">
<link rel="icon" type="image/png" sizes="96x96" href="{{ site.baseurl }}/public/favicon-96.png">
<link rel="icon" type="image/png" sizes="64x64" href="{{ site.baseurl }}/public/favicon-64.png">
<link rel="icon" type="image/png" sizes="32x32" href="{{ site.baseurl }}/public/favicon-32.png">
<link rel="icon" type="image/png" sizes="16x16" href="{{ site.baseurl }}/public/favicon-16.png">
<link rel="apple-touch-icon" href="{{ site.baseurl }}/public/favicon-57.png">
<link rel="apple-touch-icon" sizes="114x114" href="{{ site.baseurl }}/public/favicon-114.png">
<link rel="apple-touch-icon" sizes="72x72" href="{{ site.baseurl }}/public/favicon-72.png">
<link rel="apple-touch-icon" sizes="144x144" href="{{ site.baseurl }}/public/favicon-144.png">
<link rel="apple-touch-icon" sizes="60x60" href="{{ site.baseurl }}/public/favicon-60.png">
<link rel="apple-touch-icon" sizes="120x120" href="{{ site.baseurl }}/public/favicon-120.png">
<link rel="apple-touch-icon" sizes="76x76" href="{{ site.baseurl }}/public/favicon-76.png">
<link rel="apple-touch-icon" sizes="152x152" href="{{ site.baseurl }}/public/favicon-152.png">
<link rel="apple-touch-icon" sizes="180x180" href="{{ site.baseurl }}/public/favicon-180.png">
<meta name="msapplication-TileColor" content="#FFFFFF">
<meta name="msapplication-TileImage" content="{{ site.baseurl }}/public/favicon-144.png">
<meta name="msapplication-config" content="{{ site.baseurl }}/public/browserconfig.xml">
{% endhighlight %}

På denne måten vil alle telefoner, nettbrett og datamaskiner vise _ikonet_ i høyest mulige oppløsning. Under kan du se koden som er inkludert i `browserconfig.xml`.

{% highlight xml linenos %}
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
  <msapplication>
    <tile>
      <square70x70logo src="/favicon-70.png"/>
      <square150x150logo src="/favicon-150.png"/>
      <square310x310logo src="/favicon-310.png"/>
      <TileColor>#FFFFFF</TileColor>
    </tile>
  </msapplication>
</browserconfig>
{% endhighlight %}

Du kan auto-generere alle _ikonene_ du trenger hvis du besøker  <http://faviconit.com> og laster opp et _ikon_ i `.png` med en minimum oppløsning på `310x310`. Jeg derimot bestemte meg for å lage alle hver for seg i [Photoshop](http://no.wikipedia.org/wiki/Adobe_Photoshop) for å sikre meg mot kvalitetstap.

[FaviconLink]: http://en.wikipedia.org/wiki/Favicon