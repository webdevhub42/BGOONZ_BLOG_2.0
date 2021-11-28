---
title: A simple guide to HTML Head Elements
weight: 0
excerpt: A simple guide to HTML Head Elements
seo:
  title: 'A simple guide to HTML Head Elements'
  description: 'Below are the essential elements for any web document '
  robots: []
  extra: []
template: docs
---

# 🤯 HEAD

> A simple guide to HTML `<head>` elements



## Table of Contents

- [Recommended Minimum](#recommended-minimum)
- [Elements](#elements)
- [Meta](#meta)
- [Link](#link)
- [Icons](#icons)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter Card](#twitter-card)
  - [Twitter Privacy](#twitter-privacy)
  - [Schema.org](#schemaorg)
  - [Pinterest](#pinterest)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [OEmbed](#oembed)
  - [QQ/Wechat](#qqwechat)
- [Browsers / Platforms](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Browsers (Chinese)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App Links](#app-links)
- [Other Resources](#other-resources)
- [Related Projects](#related-projects)
- [Other Formats](#other-formats)
- [Translations](#-translations)
- [Contributing](#-contributing)
  - [Contributors](#contributors)
- [Author](#-author)
- [License](#-license)

## Recommended Minimum

Below are the essential elements for any web document (websites/apps):

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  The above 2 meta tags *must* come first in the <head>
  to consistently ensure proper document rendering.
  Any other head element should come *after* these tags.
 -->
<title>Page Title</title>
```

`meta charset` - defines the encoding of the website, `utf-8` is the standard

`meta name="viewport"` - viewport settings related to mobile responsiveness

`width=device-width` - use the physical width of the device (great for mobile!)

`initial-scale=1` - the initial zoom, 1 means no zoom

**[⬆ back to top](#table-of-contents)**

## Elements

Valid `<head>` elements include `meta`, `link`, `title`, `style`, `script`, `noscript`, and `base`.

These elements provide information for how a document should be perceived, and rendered, by web technologies. e.g. browsers, search engines, bots, etc.

```html
<!--
  Set the character encoding for this document, so that
  all characters within the UTF-8 space (such as emoji)
  are rendered correctly.
-->
<meta charset="utf-8">

<!-- Set the document's title -->
<title>Page Title</title>

<!-- Set the base URL for all relative URLs within the document -->
<base href="https://example.com/page.html">

<!-- Link to an external CSS file -->
<link rel="stylesheet" href="styles.css">

<!-- Used for adding in-document CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript & No-JavaScript tags -->
<script src="script.js"></script>
<script>
  // function(s) go here
</script>
<noscript>
  <!-- No JS alternative -->
</noscript>
```

**[⬆ back to top](#table-of-contents)**

## Meta

```html
<!--
  The following 2 meta tags *must* come first in the <head>
  to consistently ensure proper document rendering.
  Any other head element should come *after* these tags.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  Allows control over where resources are loaded from.
  Place as early in the <head> as possible, as the tag  
  only applies to resources that are declared after it.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Name of web application (only should be used if the website is used as an app) -->
<meta name="application-name" content="Application Name">

<!-- Theme Color for Chrome, Firefox OS and Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Short description of the document (limit to 150 characters) -->
<!-- This content *may* be used as a part of search engine results. -->
<meta name="description" content="A description of the page">

<!-- Control the behavior of search engine crawling and indexing -->
<meta name="robots" content="index,follow"><!-- All Search Engines -->
<meta name="googlebot" content="index,follow"><!-- Google Specific -->

<!-- Tells Google not to show the sitelinks search box -->
<meta name="google" content="nositelinkssearchbox">

<!-- Tells Google not to provide a translation for this document -->
<meta name="google" content="notranslate">

<!-- Verify website ownership -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Identify the software used to build the document (i.e. - WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Short description of your document's subject -->
<meta name="subject" content="your document's subject">

<!-- Gives a general age rating based on the document's content -->
<meta name="rating" content="General">

<!-- Allows control over how referrer information is passed -->
<meta name="referrer" content="no-referrer">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Completely opt out of DNS prefetching by setting to "off" -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Specifies the document to appear in a specific frame -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Country code (ISO 3166-1): mandatory, state code (ISO 3166-2): optional; eg. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- eg. content="New York City" -->

<!-- Web Monetization https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [Meta tags that Google understands](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Geotagging on Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ back to top](#table-of-contents)**

## Link

```html
<!-- Points to an external stylesheet -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Helps prevent duplicate content issues -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- Links to an AMP HTML version of the current document -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Links to a JSON file that specifies "installation" credentials for the web applications -->
<link rel="manifest" href="manifest.json">

<!-- Links to information about the author(s) of the document -->
<link rel="author" href="humans.txt">

<!-- Refers to a copyright statement that applies to the link's context -->
<link rel="license" href="copyright.html">

<!-- Gives a reference to a location in your document that may be in another language -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Provides information about an author or another person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Links to a document that describes a collection of records, documents, or other materials of historical interest -->
<link rel="archives" href="https://example.com/archives/">

<!-- Links to top level resource in an hierarchical structure -->
<link rel="index" href="https://example.com/article/">

<!-- Provides a self reference - useful when the document has multiple possible references -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- The first, last, previous, and next documents in a series of documents, respectively -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Used when a 3rd party service is utilized to maintain a blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forms an automated comment when another WordPress blog links to your WordPress blog or post -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Notifies a URL when you link to it on your document -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Enables posting to your own domain using a Micropub client -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ back to top](#table-of-contents)**

## Icons

```html
<!-- For IE 10 and below -->
<!-- Place favicon.ico in the root directory - no tag necessary -->

<!-- Icon in the highest resolution we need it for -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Safari Pinned Tab Icon -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Creating Pinned Tab Icons](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Icons & Browser Colors](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ back to top](#table-of-contents)**

## Social

### Facebook Open Graph
> Most content is shared to Facebook as a URL, so it's important that you mark up your website with Open Graph tags to take control over how your content appears on Facebook. [More about Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup) 

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="A description of what is in the image (not a caption)">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Open Graph protocol](http://ogp.me/)
- 🛠 Test your page with the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card
> With Twitter Cards, you can attach rich photos, videos and media experiences to Tweets, helping to drive traffic to your website. [More about Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="A text description of the image conveying the essential nature of an image to users who are visually impaired. Maximum 420 characters.">
```

- 📖 [Getting started with cards — Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 Test your page with the [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Privacy
If you embed tweets in your website, Twitter can use information from your site to tailor content and suggestions to Twitter users. [More about Twitter privacy options](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- disallow Twitter from using your site's info for personalization purposes -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Content Title">
      <meta itemprop="description" content="Content description less than 200 characters">
      <meta itemprop="image" content="https://example.com/image.jpg">
```

**Note:** These meta tags require the `itemscope` and `itemtype` attributes to be added to the `<html>` tag.

- 📖 [Getting Started - schema.org](https://schema.org/docs/gs.html)
- 🛠 Test your page with the [Rich Results Test](https://search.google.com/test/rich-results)

### Pinterest

Pinterest lets you prevent people from saving things from your website, according [to their help center](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). The `description` is optional.

```html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="https://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Creating Articles - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Code Samples - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [oEmbed format](https://oembed.com/)

### QQ/Wechat

Users share web pages to qq wechat will have a formatted message

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Code Format Docs](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ back to top](#table-of-contents)**

## Browsers / Platforms

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Launch Icon (180x180px or larger) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Launch Screen Image -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Launch Icon Title -->
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Enable standalone (full-screen) mode -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Status bar appearance (has no effect unless standalone mode is enabled) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Add to home screen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Force IE 8/9/10 to use its latest rendering engine -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Disable automatic detection and formatting of possible phone numbers by Skype Toolbar browser extension -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Tiles -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Minimum required xml markup for `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Browser configuration schema reference](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ back to top](#table-of-contents)**

## Browsers (Chinese)

### 360 Browser

```html
<!-- Select rendering engine order -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Locks the screen into the specified orientation -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="x5-fullscreen" content="true">

<!-- Document will be displayed in "application mode" (fullscreen, etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Locks the screen into the specified orientation -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="full-screen" content="yes">

<!-- UC browser will display images even if in "text mode" -->
<meta name="imagemode" content="force">

<!-- Document will be displayed in "application mode"(fullscreen, forbidding gesture, etc.) -->
<meta name="browsermode" content="application">

<!-- Disabled the UC browser's "night mode" for this document -->
<meta name="nightmode" content="disable">

<!-- Simplify the document to reduce data transfer -->
<meta name="layoutmode" content="fitscreen">

<!-- Disable the UC browser's feature of "scaling font up when there are many words in this document" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ back to top](#table-of-contents)**

## App Links

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [App Links](https://developers.facebook.com/docs/applinks)

**[⬆ back to top](#table-of-contents)**

## Other Resources

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ back to top](#table-of-contents)**

## Related Projects

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

**[⬆ back to top](#table-of-contents)**

## Other Formats

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ back to top](#table-of-contents)**





## Basic HTML Meta Tags

``` html
<meta name="keywords" content="your, tags"/>
<meta name="description" content="150 words"/>
<meta name="subject" content="your website's subject">
<meta name="copyright"content="company name">
<meta name="language" content="ES">
<meta name="robots" content="index,follow" />
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm" />
<meta name="abstract" content="">
<meta name="topic" content="">
<meta name="summary" content="">
<meta name="Classification" content="Business">
<meta name="author" content="name, email@hotmail.com">
<meta name="designer" content="">
<meta name="copyright" content="">
<meta name="reply-to" content="email@hotmail.com">
<meta name="owner" content="">
<meta name="url" content="http://www.websiteaddrress.com">
<meta name="identifier-URL" content="http://www.websiteaddress.com">
<meta name="directory" content="submission">
<meta name="category" content="">
<meta name="coverage" content="Worldwide">
<meta name="distribution" content="Global">
<meta name="rating" content="General">
<meta name="revisit-after" content="7 days">
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## OpenGraph Meta Tags

``` html
<meta name="og:title" content="The Rock"/>
<meta name="og:type" content="movie"/>
<meta name="og:url" content="http://www.imdb.com/title/tt0117500/"/>
<meta name="og:image" content="http://ia.media-imdb.com/rock.jpg"/>
<meta name="og:site_name" content="IMDb"/>
<meta name="og:description" content="A group of U.S. Marines, under command of..."/>

<meta name="fb:page_id" content="43929265776" />

<meta name="og:email" content="me@example.com"/>
<meta name="og:phone_number" content="650-123-4567"/>
<meta name="og:fax_number" content="+1-415-123-4567"/>

<meta name="og:latitude" content="37.416343"/>
<meta name="og:longitude" content="-122.153013"/>
<meta name="og:street-address" content="1601 S California Ave"/>
<meta name="og:locality" content="Palo Alto"/>
<meta name="og:region" content="CA"/>
<meta name="og:postal-code" content="94304"/>
<meta name="og:country-name" content="USA"/>

<meta property="og:type" content="game.achievement"/>
<meta property="og:points" content="POINTS_FOR_ACHIEVEMENT"/>

<meta property="og:video" content="http://example.com/awesome.swf" />
<meta property="og:video:height" content="640" />
<meta property="og:video:width" content="385" />
<meta property="og:video:type" content="application/x-shockwave-flash" />
<meta property="og:video" content="http://example.com/html5.mp4" />
<meta property="og:video:type" content="video/mp4" />
<meta property="og:video" content="http://example.com/fallback.vid" />
<meta property="og:video:type" content="text/html" />

<meta property="og:audio" content="http://example.com/amazing.mp3" />
<meta property="og:audio:title" content="Amazing Song" />
<meta property="og:audio:artist" content="Amazing Band" />
<meta property="og:audio:album" content="Amazing Album" />
<meta property="og:audio:type" content="application/mp3" />
```

## Create Custom Meta Tags

Use custom meta tags to store data that you need in javascript, instead of hard-coding that data into your javascript.  I store my Google Analytics code in meta tags.  Here's some examples:

``` html
<meta name="google-analytics" content="1-AHFKALJ"/>
<meta name="disqus" content="abcdefg"/>
<meta name="uservoice" content="asdfasdf"/>
<meta name="mixpanel" content="asdfasdf"/>
```

## Company/Service Meta Tags

#### ClaimID

``` html
<meta name="microid" content="mailto+http:sha1:e6058ed7fca4a1921cq91d7f1f3b8736cd3cc1g7" />
```
    
#### Apple Meta Tags

``` html
<meta name="apple-mobile-web-app-capable" content="yes">
<meta content="yes" name="apple-touch-fullscreen" />
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="format-detection" content="telephone=no">
<meta name="viewport" content="width = 320, initial-scale = 2.3, user-scalable = no">
```

#### Internet Explorer Meta Tags

``` html
<meta http-equiv="Page-Enter" content="RevealTrans(Duration=2.0,Transition=2)" />
<meta http-equiv="Page-Exit" content="RevealTrans(Duration=3.0,Transition=12)" />
<meta name="mssmarttagspreventparsing" content="true">
<meta http-equiv="X-UA-Compatible" content="chrome=1">
<meta name="msapplication-starturl" content="http://blog.reybango.com/about/"/>
<meta name="msapplication-window" content="width=800;height=600"/>
<meta name="msapplication-navbutton-color" content="red"/>
<meta name="application-name" content="Rey Bango Front-end Developer"/>
<meta name="msapplication-tooltip" content="Launch Rey Bango's Blog"/>
<meta name="msapplication-task" content="name=About;action-uri=/about/;icon-uri=/images/about.ico" />
<meta name="msapplication-task" content="name=The Big List;action-uri=/the-big-list-of-javascript-css-and-html-development-tools-libraries-projects-and-books/;icon-uri=/images/list_links.ico" />
<meta name="msapplication-task" content="name=jQuery Posts;action-uri=/category/jquery/;icon-uri=/images/jquery.ico" />
<meta name="msapplication-task" content="name=Start Developing;action-uri=/category/javascript/;icon-uri=/images/script.ico" />
<link rel="shortcut icon" href="/images/favicon.ico" />
```

#### TweetMeme Meta Tags

``` html
<meta name="tweetmeme-title" content="Retweet Button Explained" />
```

#### Blog Catalog Meta Tags

``` html
<meta name="blogcatalog" />
```

#### Rails Meta Tags

``` html
<meta name="csrf-param" content="authenticity_token"/>
<meta name="csrf-token" content="/bZVwvomkAnwAI1Qd37lFeewvpOIiackk9121fFwWwc="/>
```

#### Apple Tags

``` html
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="format-detection" content="telephone=no">
<meta name= "viewport" content = "width = 320, initial-scale = 2.3, user-scalable = no">
<meta name= "viewport" content = "width = device-width">
<meta name = "viewport" content = "initial-scale = 1.0">
<meta name = "viewport" content = "initial-scale = 2.3, user-scalable = no">
<link rel="apple-touch-icon" href="touch-icon-iphone.png" />
<link rel="apple-touch-icon" sizes="72x72" href="touch-icon-ipad.png" />
<link rel="apple-touch-icon" sizes="114x114" href="touch-icon-iphone4.png" />
<link rel="apple-touch-startup-image" href="/startup.png">

<link rel="apple-touch-icon" type="image/png" href="/apple-touch-icon.png" />
```
    
## HTML Link Tags

``` html
<link rel="alternate" type="application/rss+xml" title="RSS" href="http://feeds.feedburner.com/martini" />
<link rel="shortcut icon" type="image/ico" href="/favicon.ico" />
<link rel="fluid-icon" type="image/png" href="/fluid-icon.png" />
<link rel="me" type="text/html" href="http://google.com/profiles/thenextweb"/>
<link rel='shortlink' href='http://blog.unto.net/?p=353' />
<link rel='archives' title='May 2003' href='http://blog.unto.net/2003/05/' />
<link rel='index' title='DeWitt Clinton' href='http://blog.unto.net/' />
<link rel='start' title='Pattern Recognition 1' href='http://blog.unto.net/photos/pattern_recognition_1_about/' />
<link rel='prev' title='OpenSearch and OpenID?  A sure way to get my attention.' href='http://blog.unto.net/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/' />
<link rel='next' title='Not blog' href='http://blog.unto.net/meta/not-blog/' />
<link rel="search" href="/search.xml" type="application/opensearchdescription+xml" title="Viatropos" />

<link rel="self" type="application/atom+xml" href="http://www.syfyportal.com/atomFeed.php?page=3"/>
<link rel="first" href="http://www.syfyportal.com/atomFeed.php"/>
<link rel="next" href="http://www.syfyportal.com/atomFeed.php?page=4"/>
<link rel="previous" href="http://www.syfyportal.com/atomFeed.php?page=2"/>
<link rel="last" href="http://www.syfyportal.com/atomFeed.php?page=147"/>

<link rel='shortlink' href='http://smallbiztrends.com/?p=43625' />
<link rel="canonical" href="http://smallbiztrends.com/2010/06/9-things-to-do-before-entering-social-media.html" />
<link rel="EditURI" type="application/rsd+xml" title="RSD" href="http://smallbiztrends.com/xmlrpc.php?rsd" />
<link rel="pingback" href="http://smallbiztrends.com/xmlrpc.php" />
<link media="only screen and (max-device-width: 480px)" href="http://wordpress.org/style/iphone.css" type="text/css" rel="stylesheet" />
```

## Other Resources

- [Dublic Core Meta Tags](http://www.seoconsultants.com/meta-tags/dublin/)
- [Apple Meta Tags](http://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html)
- [OpenGraph Meta Tags](http://opengraphprotocol.org/)
- [Link Tag Meaning](http://intertwingly.net/wiki/pie/LinkTagMeaning)
- [Google Chrome HTML5 Tags](http://www.html5rocks.com/)




Basic HTML Meta Tags
<meta charset='UTF-8'>
<meta name='keywords' content='your, tags'>
<meta name='description' content='150 words'>
<meta name='subject' content='your website's subject'>
<meta name='copyright' content='company name'>
<meta name='language' content='ES'>
<meta name='robots' content='index,follow'>
<meta name='revised' content='Sunday, July 18th, 2010, 5:15 pm'>
<meta name='abstract' content=''>
<meta name='topic' content=''>
<meta name='summary' content=''>
<meta name='Classification' content='Business'>
<meta name='author' content='name, email@hotmail.com'>
<meta name='designer' content=''>
<meta name='reply-to' content='email@hotmail.com'>
<meta name='owner' content=''>
<meta name='url' content='http://www.websiteaddrress.com'>
<meta name='identifier-URL' content='http://www.websiteaddress.com'>
<meta name='directory' content='submission'>
<meta name='pagename' content='jQuery Tools, Tutorials and Resources - O'Reilly Media'>
<meta name='category' content=''>
<meta name='coverage' content='Worldwide'>
<meta name='distribution' content='Global'>
<meta name='rating' content='General'>
<meta name='revisit-after' content='7 days'>
<meta name='subtitle' content='This is my subtitle'>
<meta name='target' content='all'>
<meta name='HandheldFriendly' content='True'>
<meta name='MobileOptimized' content='320'>
<meta name='date' content='Sep. 27, 2010'>
<meta name='search_date' content='2010-09-27'>
<meta name='DC.title' content='Unstoppable Robot Ninja'>
<meta name='ResourceLoaderDynamicStyles' content=''>
<meta name='medium' content='blog'>
<meta name='syndication-source' content='https://mashable.com/2008/12/24/free-brand-monitoring-tools/'>
<meta name='original-source' content='https://mashable.com/2008/12/24/free-brand-monitoring-tools/'>
<meta name='verify-v1' content='dV1r/ZJJdDEI++fKJ6iDEl6o+TMNtSu0kv18ONeqM0I='>
<meta name='y_key' content='1e39c508e0d87750'>
<meta name='pageKey' content='guest-home'>
<meta itemprop='name' content='jQTouch'>
<meta http-equiv='Expires' content='0'>
<meta http-equiv='Pragma' content='no-cache'>
<meta http-equiv='Cache-Control' content='no-cache'>
<meta http-equiv='imagetoolbar' content='no'>
<meta http-equiv='x-dns-prefetch-control' content='off'>
OpenGraph Meta Tags
<meta name='og:title' content='The Rock'>
<meta name='og:type' content='movie'>
<meta name='og:url' content='http://www.imdb.com/title/tt0117500/'>
<meta name='og:image' content='http://ia.media-imdb.com/rock.jpg'>
<meta name='og:site_name' content='IMDb'>
<meta name='og:description' content='A group of U.S. Marines, under command of...'>

<meta name='fb:page_id' content='43929265776'>
<meta name='application-name' content='foursquare'>
<meta name='og:email' content='me@example.com'>
<meta name='og:phone_number' content='650-123-4567'>
<meta name='og:fax_number' content='+1-415-123-4567'>

<meta name='og:latitude' content='37.416343'>
<meta name='og:longitude' content='-122.153013'>
<meta name='og:street-address' content='1601 S California Ave'>
<meta name='og:locality' content='Palo Alto'>
<meta name='og:region' content='CA'>
<meta name='og:postal-code' content='94304'>
<meta name='og:country-name' content='USA'>

<meta property='fb:admins' content='987654321'>
<meta property='og:type' content='game.achievement'>
<meta property='og:points' content='POINTS_FOR_ACHIEVEMENT'>

<meta property='og:video' content='http://example.com/awesome.swf'>
<meta property='og:video:height' content='640'>
<meta property='og:video:width' content='385'>
<meta property='og:video:type' content='application/x-shockwave-flash'>
<meta property='og:video' content='http://example.com/html5.mp4'>
<meta property='og:video:type' content='video/mp4'>
<meta property='og:video' content='http://example.com/fallback.vid'>
<meta property='og:video:type' content='text/html'>

<meta property='og:audio' content='http://example.com/amazing.mp3'>
<meta property='og:audio:title' content='Amazing Song'>
<meta property='og:audio:artist' content='Amazing Band'>
<meta property='og:audio:album' content='Amazing Album'>
<meta property='og:audio:type' content='application/mp3'>
Create Custom Meta Tags
Use custom meta tags to store data that you need in Javascript, instead of hard-coding that data into your Javascript. I store my Google Analytics code in meta tags. Here's some examples:

<meta name='google-analytics' content='1-AHFKALJ'>
<meta name='disqus' content='abcdefg'>
<meta name='uservoice' content='asdfasdf'>
<meta name='mixpanel' content='asdfasdf'>
Company/Service Meta Tags
ClaimID
<meta name='microid' content='mailto+http:sha1:e6058ed7fca4a1921cq91d7f1f3b8736cd3cc1g7'>
<meta name='readability-verification' content='E7aEHvVQpWc8VHDqKvaB2Z58hek2EAv2HuLuegv7'>
<meta name='google-site-verification' content='4SMIedO1X4IkYrYuhEC2VuovdQM36Xxb0btUjElqQyg'>
<meta name='ICBM' content='40.746990, -73.980537'>
<meta name='generator' content='WordPress 3.3.1'>
<meta name='norton-safeweb-site-verification' content='tz8iotmk-pkhui406y41y5bfmfxdwmaa4a-yc0hm6r0fga7s6j0j27qmgqkmc7oovihzghbzhbdjk-uiyrz438nxsjdbj3fggwgl8oq2nf4ko8gi7j4z7t78kegbidl4'>
Apple Meta Tags
<meta name="apple-mobile-web-app-title" content="My App"> <!-- New in iOS6 -->
<meta name='apple-mobile-web-app-capable' content='yes'>
<meta name='apple-touch-fullscreen' content='yes'>
<meta name='apple-mobile-web-app-status-bar-style' content='black'>
<meta name='format-detection' content='telephone=no'>
<meta name='viewport' content='width=device-width; content='width = 320; initial-scale=1.0; maximum-scale=1.0; user-scalable=yes; target-densitydpi=160dpi'>

<link href='/apple-touch-icon.png' rel='apple-touch-icon' type='image/png'>
<link href='touch-icon-ipad.png' rel='apple-touch-icon' sizes='72x72'>
<link href='touch-icon-iphone4.png' rel='apple-touch-icon' sizes='114x114'>
<link href='/startup.png' rel='apple-touch-startup-image'>

<link href='http://github.com/images/touch-icon-iphone4.png' sizes='114x114' rel='apple-touch-icon-precomposed'>
<link href='http://github.com/images/touch-icon-ipad.png' sizes='72x72' rel='apple-touch-icon-precomposed'>
<link href='http://github.com/images/apple-touch-icon-57x57.png' sizes='57x57' rel='apple-touch-icon-precomposed'>
Internet Explorer Meta Tags
<meta http-equiv='Page-Enter' content='RevealTrans(Duration=2.0,Transition=2)'>
<meta http-equiv='Page-Exit' content='RevealTrans(Duration=3.0,Transition=12)'>
<meta name='mssmarttagspreventparsing' content='true'>
<meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
<meta name='msapplication-starturl' content='http://blog.reybango.com/about/'>
<meta name='msapplication-window' content='width=800;height=600'>
<meta name='msapplication-navbutton-color' content='red'>
<meta name='application-name' content='Rey Bango Front-end Developer'>
<meta name='msapplication-tooltip' content='Launch Rey Bango's Blog'>
<meta name='msapplication-task' content='name=About;action-uri=/about/;icon-uri=/images/about.ico'>
<meta name='msapplication-task' content='name=The Big List;action-uri=/the-big-list-of-javascript-css-and-html-development-tools-libraries-projects-and-books/;icon-uri=/images/list_links.ico'>
<meta name='msapplication-task' content='name=jQuery Posts;action-uri=/category/jquery/;icon-uri=/images/jquery.ico'>
<meta name='msapplication-task' content='name=Start Developing;action-uri=/category/javascript/;icon-uri=/images/script.ico'>
<meta name='msvalidate.01' content='6E3AD52DC176461A3C81DD6E98003BC9'>
<meta http-equiv='cleartype' content='on'>
Google Meta Tags
<meta name="news_keywords" content="World Cup, Brazil 2014, Spain vs Netherlands, soccer, football">
TweetMeme Meta Tags
<meta name='tweetmeme-title' content='Retweet Button Explained'>
Blog Catalog Meta Tags
<meta name='blogcatalog'>
Rails Meta Tags
<meta name='csrf-param' content='authenticity_token'>
<meta name='csrf-token' content='/bZVwvomkAnwAI1Qd37lFeewvpOIiackk9121fFwWwc='>
HTML Link Tags
<link rel='alternate' type='application/rss+xml' title='RSS' href='http://feeds.feedburner.com/martini'>
<link rel='alternate' type='application/atom+xml' title='Atom 0.3' href='https://example.com/feed.atom'>
<link rel='shortcut icon' type='image/ico' href='/favicon.ico'>
<link rel='fluid-icon' type='image/png' href='/fluid-icon.png'>
<link rel='me' type='text/html' href='http://google.com/profiles/thenextweb'>
<link rel='shortlink' href='http://blog.unto.net/?p=353'>
<link rel='archives' title='May 2003' href='http://blog.unto.net/2003/05/'>
<link rel='index' title='DeWitt Clinton' href='http://blog.unto.net/'>
<link rel='start' title='Pattern Recognition 1' href='http://blog.unto.net/photos/pattern_recognition_1_about/'>
<link rel='bookmark'title='Styleguide' href='http://paulrobertlloyd.com/about/styleguide/'>
<link rel='search' href='/search.xml' type='application/opensearchdescription+xml' title='Viatropos'>

<link rel='self' type='application/atom+xml' href='http://www.syfyportal.com/atomFeed.php?page=3'>
<link rel='first' href='http://www.syfyportal.com/atomFeed.php'>
<link rel='next' href='http://www.syfyportal.com/atomFeed.php?page=4'>
<link rel='previous' href='http://www.syfyportal.com/atomFeed.php?page=2'>
<link rel='last' href='http://www.syfyportal.com/atomFeed.php?page=147'>

<link rel='canonical' href='http://smallbiztrends.com/2010/06/9-things-to-do-before-entering-social-media.html'>
<link rel='EditURI' type='application/rsd+xml' title='RSD' href='http://smallbiztrends.com/xmlrpc.php?rsd'>
<link rel='pingback' href='http://smallbiztrends.com/xmlrpc.php'>
<link rel='stylesheet' media='only screen and (max-device-width: 480px)' href='http://wordpress.org/style/iphone.css' type='text/css'>
<link rel='wlwmanifest' href='http://www.example.com/wp-includes/wlwmanifest.xml' type='application/wlwmanifest+xml'>
## Other Resources

- [HTML5 Boilerplate explanations and suggestions of header tags](http://html5boilerplate.com/docs/head-Tips/)
- [Dublic Core Meta Tags](http://www.seoconsultants.com/meta-tags/dublin/)
- [Apple Meta Tags](http://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html)
- [OpenGraph Meta Tags](http://opengraphprotocol.org/)
- [Link Tag Meaning](http://intertwingly.net/wiki/pie/LinkTagMeaning)
- [Google Chrome HTML5 Tags](http://www.html5rocks.com/)