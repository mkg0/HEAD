## Kaldırılan İçerikler

Alt kısımda yer alan meta etiketleri kullanılmayan ve eski olduğu bilgisinin artık bir değer yaratmadığı meta etiketleri içerir. Esas içeriğe [bu bağlantıdan](https://github.com/mkg0/HEAD) ulaşabilirsiniz.

<!-- Çok kısa (10 kelime veya daha azı) açıklama. Genellikle akademik yayınlar için -->
<meta name="abstract" content="">

<!-- Web site adresinin tümü -->
<meta name="url" content="https://example.com/">

<meta name="directory" content="submission">

<!-- Belgenin dilini belirtmek için kullanılır fakat çok desteklenmez. <html lang=""> kullanmanız tavsiye edilir -->
<meta name="language" content="en">

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
```