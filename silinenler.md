## Kaldırılan İçerikler

Alt kısımda yer alan meta etiketleri kullanılmayan ve eski olduğu bilgisinin artık bir değer yaratmadığı meta etiketleridir. Aşağıdaki değerleri hiçbir şeykilde kullanmayın.

Güncel içeriğe [bu bağlantıdan](https://github.com/mkg0/HEAD) ulaşabilirsiniz. 

```html
<!-- Çok kısa (10 kelime veya daha azı) açıklama. Genellikle akademik yayınlar için -->
<meta name="abstract" content="">

<!-- Web site adresinin tümü -->
<meta name="url" content="https://example.com/">

<meta name="directory" content="submission">

<!-- Belgenin dilini belirtmek için kullanılır fakat çok desteklenmez. <html lang=""> kullanmanız tavsiye edilir -->
<meta name="language" content="en">

<link rel="shortcut icon" href="path/to/favicon.ico">

<!-- Kullanışlı değil ve hatalı, inceleyin: https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/Y_2eFRh9BOs/gULYapoRBwAJ -->
<link rel="subresource" href="styles.css">

<!-- Google görmezden geliyor & Bing ise spam göstergesi olarak algılıyor -->
<meta name="keywords" content="virgulle,ayrilmis,anahtar,kelimeler,bosluk,yok">
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

<!-- iOS 8+ artık precomposed desteklemiyor, yalnızca apple-touch-icon zorunlu -->
<link rel="apple-touch-icon-precomposed" href="/path/to/apple-touch-icon-sikistirilmamis.png">


```

### Microsoft Internet Explorer

``` html
<!-- IE 6'da görsele tıklandığında çıkan, resim araç çubuğunu devre dışı bırakır (https://msdn.microsoft.com/en-us/library/ms532986(v=vs.85).aspx) -->
<meta http-equiv="imagetoolbar" content="no">

<!-- Form elemanlarından(input/buton) windows temasını kaldırır (https://support.microsoft.com/en-us/kb/322240) -->
<meta name="MSThemeCompatible" content="no">

<!-- Yalnızca IE 6 beta üzerinde olan özelliği kaldırır (https://stackoverflow.com/q/2167301) -->
<meta name="MSSmartTagsPreventParsing" content="true">

<!-- Sayfalar Ararası Geçişler (https://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx) -->
<meta http-equiv="Page-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Page-Exit" content="revealtrans(duration=3,transition=12)">
<meta http-equiv="Site-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Site-Exit" content="revealtrans(duration=3,transition=12)">

<meta http-equiv="cleartype" content="on">
<meta name="msapplication-allowDomainApiCalls" content="true">		
<meta name="msapplication-allowDomainMetaTags" content="true">

```
