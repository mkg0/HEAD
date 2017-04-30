# HEAD

Sayfanızın `<head>` bölümü içerisine girebilecek her şeyin listesi. Orijinali [Josh Buchea](https://github.com/joshbuchea)’ya ait [HEAD](https://github.com/joshbuchea/HEAD) reposunun türkçe çevirisidir. Düzenlemelerden haberdar olmak için repoyu izlemeniz tavsiye edilir.

## İçerik Tablosu

- [Önerilenler Minimum](#onerilenler-minimum)
- [Elementler](#elementler)
- [Meta](#meta)
  - [Meta: Önerilmeyenler](#meta-onerilmeyenler)
- [Link](#link)
  - [Favori Simgeleri](#favori-simgeleri)
- [Sosyal](#sosyal)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [Twitter Cards](#twitter-cards)
  - [Google+ / Schema.org](#google--schemaorg)
  - [OEmbed](#oembed)
- [Tarayıcılar / Platformlar](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Apple Safari](#apple-safari)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Tarayıcılar (Çin)](#tarayicilar-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [Uygulama Linkleri](#uygulama-linkleri)
- [Notlar](#notlar)
  - [Performans](#performans)
- [Diğer Kaynaklar](#diger-kaynaklar)
- [İlgili Projeler](#ilgili-projeler)
- [Diğer Formatlar](#diger-formatlar)
- [Çeviriler](#ceviriler)
- [Katkıda Bulun](#katkida-bulun)
- [Katkıda Bulunanlar](#katkida-bulunanlar)
- [Yazar](#yazar)
- [Lisans](#lisans)

## Önerilenler Minimum

Basit ve sade web siteleri için başlıca etiketler:

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- Yukarıdaki 3 meta etiketi head bölümü içerisinde *ilk sırada* konumlanmalıdır; diğer head içerikleri bu etiketlerin *ardından* yerleştirilmelidir -->
<title>Sayfa Başlığı</title>
```

## Elementler

``` html
<!-- Doküman Başlığı -->
<title>Sayfa Başlığı</title>

<!-- Base URL doküman içerisinde ilişkisel olarak girilmiş bağlantılar(relative path) için başlangıç noktası oluşturur -->
<base href="https://example.com/page.html">

<!-- Harici CSS -->
<link rel="stylesheet" href="styles.css">

<!-- Doküman içi CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript -->
<script src="script.js"></script>
<noscript><!--JS olmaması halinde--></noscript>
```

## Meta

``` html
<meta charset="utf-8"> <!-- Doküman için karakter kodlaması belirler -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- Yukarıdaki 3 meta etiketi head bölümü içerisinde *ilk sırada* konumlanmalıdır; diğer head içerikleri bu taglerin *ardından* yerleştirilmelidir -->

<!-- Kaynakların nereden yükleneceğini kontrol eder -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
<!-- Doküman içerisinde olabildiğince önce konumlandırın -->
<!-- Sadece bu etiketin altındaki içeriğe etki eder -->

<!-- Web uygulamasının adı (yalnızca web sayfası bir uygulamaysa kullanılmalı.) -->
<meta name="application-name" content="Application Name">

<!-- Sayfanın kısa açıklaması (150 karakter ile sınırlıdır) -->
<!-- *Bazı* durumlarda, bu açıklama arama sonuçları içerisinde sayfadan bir kesit olarak kullanılır -->
<meta name="description" content="A description of the page">

<!-- Arama motorunun gezinme ve indeksleme davranışını belirler  -->
<meta name="robots" content="index,follow,noodp"><!-- Bütün Arama Motorları -->
<meta name="googlebot" content="index,follow"><!-- Google'a özgül -->

<!-- Google'a sitelinks search boxı göstermemesini belirtir -->
<meta name="google" content="nositelinkssearchbox">

<!-- Google'a bu sayfa için bir çeviri sağlamamasını belirtir -->
<meta name="google" content="notranslate">

<!-- Google Search Console için site sahipliğini doğrular -->
<meta name="google-site-verification" content="verification_token">

<!-- Yandex Webmasters için site sahipliğini doğrular -->
<meta name="yandex-verification" content="verification_token">

<!-- Bing Webmaster Center için site sahipliğini doğrular -->
<meta name="msvalidate.01" content="verification_token">

<!-- Alexa Console için site sahipliğini doğrular -->
<meta name="alexaVerifyID" content="verification_token">

<!-- Pinterest Console için site sahipliğini doğrular -->
<meta name="p:domain_verify" content="code from pinterest">

<!-- Norton Safe Web için site sahipliğini doğrular -->
<meta name="norton-safeweb-site-verification" content="norton code">

<!-- Web sitesini oluşturmak için kullanılan araç (örnek - WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Web sitenin konusunu ifade eden kısa açıklama -->
<meta name="subject" content="your website's subject">

<!-- Web site içeriğinin hitap ettiği kitleyi belirtir -->
<meta name="rating" content="General">

<!-- Kaynak(referrer) bilgisinin nasıl iletileceğini belirtir -->
<meta name="referrer" content="no-referrer">

<!-- Uygun telefon numaraları için otomatik algılamayı ve biçimlendirmeyi iptal eder -->
<meta name="format-detection" content="telephone=no">

<!-- DNS ön tanımını tümden iptal eder -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Tarayıcı tarafında kullanıcı ile ilgili çerez(cookie) oluşturmayı sağlar -->
<meta http-equiv="set-cookie" content="name=value; expires=date; path=url">

<!-- Sayfanın spesifik bir çerçeve içerisinde açılması durumunu belirler  -->
<meta http-equiv="Window-Target" content="_value">

<!-- Coğrafi etiketler -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Ülke kodu (ISO 3166-1): zorunlu, bölge kodu (ISO 3166-2): tercihen; örn. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- örn. content="New York City" -->
```

- [Google'ın anladığı meta etiketler](https://support.google.com/webmasters/answer/79812?hl=tr)
- [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- [Wikipedia'de ICBM](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- [Wikipedia'de Geotagging](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

### Meta: Önerilmeyenler
Aşağıda, düşük kullanım oranları ve/veya artık kullanılmadıkları için önerilmeyen meta özellikleri verilmiştir:

```html
<!-- Google görmezden geliyor & Bing ise spam göstergesi olarak algılıyor -->
<meta name="keywords" content="your,keywords,here,comma,separated,no,spaces">
<!-- Herhangi bir arama motorunda kullanıldığına dair bir belirti yok -->
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">

<!-- Spam botlarına kolay email kaynağı sağlıyor -->
<meta name="reply-to" content="email@example.com">

<!--  <link rel="author"> ya da humans.txt dosyası kullanılması tavsiye edilir -->
<meta name="author" content="name, email@example.com">
<meta name="designer" content="">
<meta name="owner" content="">

<!-- Arama botlarına belli bir periyottan sonra yeniden ziyaret etmesini belirtir. Fakat çoğu arama motoru, tarama periyotlarını kendi belirlediği için desteklenmiyor -->
<meta name="revisit-after" content="7 days">

<!-- Belirli bir süreden sonra kullanıcıyı yeni bir URLe gönderir -->
<!-- W3C bu etiketin kullanılmamasını, Google ise sunucu taraflı  301 yönlendirmesini tavsiye eder -->
<meta http-equiv="refresh" content="300; url=https://example.com/">

<!-- Web sitenin konusunu belirtir -->
<meta name="topic" content="">

<!-- Şirketin kısa özeti veya web sitesinin amacı -->
<meta name="summary" content="">

<!-- Kullanımdan kalkan, keywords meta etiketi ile aynı işe yarayan bir etiket -->
<meta name="classification" content="business">

<!-- URLin variantı. Daha eski ve desteklenmiyor -->
<meta name="identifier-URL" content="https://example.com/">

<!-- Keywords meta etiketi ile benzer özellikte -->
<meta name="category" content="">

<!-- Web sitenin bütün ülkeleri ve dilleri kapsadığını teyid eder -->
<meta name="coverage" content="Worldwide">

<!-- coverage etiketi ile aynı -->
<meta name="distribution" content="Global">

<!-- Hangi kullanıcının internete erişebileceğini kontrol eder* -->
<meta http-equiv="Pics-label" content="value">

<!-- Cache Kontrolü -->
<!-- Cache kontrolünü sunucu tarafında sağlamak tercih edilmelidir -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## Link

``` html
<!-- CSS stil dosyasını işaret eder -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Yinelenen içerik sorunlarını önlemeye yardımcı olur -->
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">

<!-- İkon bağlantısından önce eklenirdi, ancak kullanımdan kaldırıldı -->
<link rel="shortlink" href="https://example.com/?p=42">

<!--Mevcut sayfanın AMP HTML versiyonuna ait linki belirtir -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Web uygulamaları için "kurulum" kimlik bilgilerini belirten bir JSON dosyasını tanımlar -->
<link rel="manifest" href="manifest.json">

<!-- Belgenin yaratıcısını belirtir -->
<link rel="author" href="humans.txt">

<!-- Telif hakkı bilidirimini açıklayan bağlantıyı işaret eder -->
<link rel="copyright" href="copyright.html">

<!-- Belgenin başka bir dildeki bağlantısına refere eder -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Yaratıcı veya başka biri hakkında bilgi verir  -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Dokümansal, kayıtsal veya tarihsel yönden ilişkisel olan bir koleksiyona işaret eder -->
<link rel="archives" href="https://example.com/2003/05/">

<!-- Bir hiyerarşik yapı içerisinde en üst seviyedeki kaynağa işaret eder -->
<link rel="index" href="https://example.com/">

<!-- Kendine referans verir - doküman birden fazla referansa sahip olduğunda faydalıdır -->
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">

<!-- Bir dizi belgede sırasıyla ilk, bir sonraki, bir önceki ve son sıradaki belgeleri işaret eder -->
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="prev" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">

<!-- Üçüncü taraf servislerden blog hizmeti sağlantığında kullanılır  -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Başka bir WordPress gönderisi sizin blogunuza veya gönderinize bağlantı verdiğinde otomatik bir ping oluşturur -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Başka bir web sayfası sizin sayfanıza bağlantı verdiğinde bilgilendirdiği bağlantıyı işaret eder -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Harici bir HTML belgesini mevcut olan HTML belgesine dahil eder -->
<link rel="import" href="/path/to/component.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Akışlar -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
<!-- Detaylı bilgi: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

### Favori Simgeleri

``` html
<!-- IE 10 ve altı için -->
<!-- favicon.ico isminde bir dosyayı kök dizinine yerleştirin - element gerekli değil -->

<!-- IE 11, Chrome, Firefox, Safari, Opera için -->
<link rel="icon" type="image/png" sizes="16x16" href="/path/to/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/path/to/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/path/to/favicon-96x96.png">
```

- [Favori Simgeleri Hakkında Her Şey (Ve Touch Simgeler)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- [Favori Simgeleri Kopya Kağıdı](https://github.com/audreyr/favicon-cheat-sheet)

## Sosyal

### Facebook Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
<!-- Facebook: https://developers.facebook.com/docs/sharing/webmasters#markup -->
<!-- Open Graph: http://ogp.me/ -->
```

- [Facebook Open Graph İşaretlemesi](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protokolü](http://ogp.me/)

### Facebook Instant Articles

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- Makalenizin web versiyonunun bağlantısı -->
<link rel="canonical" href="http://example.com/article.html">

<!-- Mevcut makale için kullanılacak stil -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Anlık Makaleler: Makale Oluşturma](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Anlık Makaleler: Biçimlendirme Belgesi](https://developers.facebook.com/docs/instant-articles/reference)

### Twitter Cards

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<!-- Detaylı bilgi: https://dev.twitter.com/cards/getting-started -->
<!-- Doğrulama: https://dev.twitter.com/docs/cards/validation/validator -->
```

- [Twitter Kartları: Başlangıç Rehberi](https://dev.twitter.com/cards/getting-started)
- [Twitter Kart Doğrulayıcısı](https://cards-dev.twitter.com/validator)

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

### Pinterest

Pinterest, [yardım merkezine](https://help.pinterest.com/en/articles/prevent-people-saving-things-pinterest-your-site) göre insanların web sitenizdeki içerikleri kaydetmesini önlemenize olanak sağlar. `description` zorunlu değildir.

``` html
<meta name="pinterest" content="nopin" description="Üzgümüm, benim sitemden kaydedemezsiniz!">
```

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- [oEmbed format](http://oembed.com/)

## Tarayıcılar / Platformlar

### Apple iOS

``` html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Uygun telefon numaraları için otomatik algılamayı ve biçimlendirmeyi iptal eder -->
<meta name="format-detection" content="telephone=no">

<!-- Ana Ekran'a ekle -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="Uygulama Başlığı">

<!-- Touch İkonlar -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="/path/to/apple-touch-icon-sikistirilmamis.png">
<!-- iOS 8+ artık precomposed desteklemiyor, yalnızca apple-touch-icon zorunlu -->

<!-- Birçok durum için head alanında bir 180×180px touch simge yeterli -->
<!-- Cihaz tarafından belirlenen benzersiz simgeler istiyorsanız -->
<!-- farklı simge boyutlarından yararlanın -->
<link rel="apple-touch-icon" sizes="57x57" href="/path/to/icon@57.png">
<link rel="apple-touch-icon" sizes="72x72" href="/path/to/icon@72.png">
<link rel="apple-touch-icon" sizes="114x114" href="/path/to/icon@114.png">
<link rel="apple-touch-icon" sizes="144x144" href="/path/to/icon@144.png">

<!-- Başlangıç Görseli ( Kullanımdan kaldırıldı ) -->
<link rel="apple-touch-startup-image" href="path/to/startup.png">

<!-- iOS derin uygulama bağlantısı(deep linking) -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- [Apple Meta Etiketleri](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- Sabitlenmiş(pinned) Site -->
<link rel="mask-icon" href="path/to/icon.svg" color="red">
```

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- Ana ekrana ekle -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Detaylı bilgi: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android derin uygulama bağlantısı(deep linking) -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Çeviri istemini devre dışı bırak -->
<meta name="google" value="notranslate">
```
### Google Chrome Mobil (Yalnızca Android)

Chrome 31'den itibaren, web uygulamanızı tıpkı Safari'deki gibi "uygulama modu" olarak ayarlayabilirsiniz.

``` html
<!-- manifest dosya bağlantısını ve meta bilgisini tanımlar -->
<!-- manifest.json örneği aşağıdaki bağlantıdan bulunabilir -->
<link rel="manifest" href="manifest.json">

<!-- Web sayfanızı web uygulaması olarak tanımlar -->
<meta name="mobile-web-app-capable" content="yes">

<!-- Ana Ekran Simgesi  -->
<link rel="icon" sizes="192x192" href="highres-icon.png">
```

- [Google Developers](https://developer.chrome.com/multidevice/android/installtohomescreen)

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Phone üzerindeki IE 10'da bağlantı vurgulamasını kaldırır (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Sabitlenmiş(pinned) siteler (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Contoso Pinned Site Caption">
<meta name="msapplication-tooltip" content="Example Tooltip Text">
<meta name="msapplication-starturl" content="/">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">

<meta name="msapplication-allowDomainApiCalls" content="true">
<meta name="msapplication-allowDomainMetaTags" content="true">
<meta name="msapplication-badge" content="frequency=30; polling-uri=http://example.com/id45453245/polling.xml">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile">
<meta name="msapplication-square150x150logo" content="path/to/logo.png">
<meta name="msapplication-square310x310logo" content="path/to/largelogo.png">
<meta name="msapplication-square70x70logo" content="path/to/tinylogo.png">
<meta name="msapplication-wide310x150logo" content="path/to/widelogo.png">
<meta name="msapplication-task" content="name=Check Order Status;action-uri=./orderStatus.aspx?src=IE9;icon-uri=./favicon.ico">
<meta name="msapplication-task-separator" content="1">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="/path/to/tileimage.jpg">
<meta name="msapplication-window" content="width=1024;height=768">
```

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- Web Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
<!-- Detaylı bilgi: http://applinks.org/documentation/ -->
```

- [App Links Dokümantasyonu](http://applinks.org/documentation/)

## Browsers (Çin)

### 360 Browser

``` html
<!-- Sırasıyla render motoru seçer -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

``` html
<!-- Ekranı belirtilen yönde sabitler -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- Mevcut sayfayı tam ekranda görüntüler -->
<meta name="x5-fullscreen" content="true">
<!-- Sayfa "uygulama modu"nda görüntülenir (tam ekran, vb.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

``` html
<!-- Ekranı belirtilen yönde sabitler -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- Mevcut sayfayı tam ekranda görüntüler -->
<meta name="full-screen" content="yes">
<!-- UC browser "metin modu"nda olsa bile görselleri gösterir -->
<meta name="imagemode" content="force">
<!-- Sayfa "uygulama modu"nda görüntülenir(tam ekran, hareketi yasaklamak, vb.) -->
<meta name="browsermode" content="application">
<!-- UC browser'ın "gece modu"nu mevcut sayfada iptal eder -->
<meta name="nightmode" content="disable">
<!-- Data transferini azaltmak için sayfayı basitleştirir -->
<meta name="layoutmode" content="fitscreen">
<!-- UC browser'ın "sayfada çok fazla kelime olduğunda font büyütme özelliği"ni iptal eder -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Dokümantasyonu](http://www.uc.cn/download/UCBrowser_U3_API.doc)

## Notlar

### Performans
`href` özelliğini bir elementin başına taşımak, GZIP aktifken sıkıştırma performansını arttırır.

Örnek:

``` html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

## Diğer Kaynaklar

- [HTML5 Boilerplate Dokümantasyonu: HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Dokümantasyonu: Genişlet ve özelleştir](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

## İlgili Projeler

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

## Diğer Formatlar

- [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

## Çeviriler

- [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- [Italian](https://github.com/Fakkio/HEAD)
- [Japanese](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- [Russian/Русский](https://github.com/Konfuze/HEAD)
- [Turkish/Türkçe](https://github.com/mkg0/HEAD)

## Katkıda Bulun

Düzenleme veya ilave önermek için bir issue açın ya da pull request gönderin.
Lütfen pull requestler için şu adımları izleyin:

- Tek seferde yalnıza bir etiket veya ilişkili olan bir etiket grubu düzenleyin
- Özelliklerde çift tırnak kullanın
- Kapatma etiketi olmayan elementlere ters eğik çizgi eklemeyin - HTML 5 tanımları opsiyonel olduğunu belirtiyor
- Değişikliğinizi destekleyecek bir dokümantasyon bağlantısı eklemeyi düşünün

## Katkıda Bulunanlar

Katkıda bulunan bu muhteşem ötesi insanlara [göz gezdirin](https://github.com/joshbuchea/HEAD/graphs/contributors).

## Yazar

**[Josh Buchea](http://joshbuchea.com/)**

## Lisans

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

Yasalar dahilinde mümkün olduğunca, [Josh Buchea](http://joshbuchea.com) bu eserle ilgili tüm telif hakkı ve benzeri haklardan feragat etmiştir.
