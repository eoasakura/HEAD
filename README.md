# HEAD

[![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Contributors](https://img.shields.io/github/contributors/joshbuchea/head.svg)](https://github.com/eoasakura/HEAD/graphs/contributors)

Lista de todo lo que puedes colocar en el `<head>` de tu documento

## Tabla de contenidos

- [Mínimo recomendado](#mínimo-recomendado)
- [Elementos](#elementos)
- [Meta](#meta)
- [Link](#link)
  - [Favicons](#favicons)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Facebook Articulos Instantáneos](#facebook-artículos-instantáneos)
  - [Twitter Cards](#twitter-cards)
  - [Google+ / Schema.org](#google--schemaorg)
  - [OEmbed](#oembed)
- [Navagadores / Plataformas](#navegadores--plataformas)
  - [Apple iOS](#apple-ios)
  - [Apple Safari](#apple-safari)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Navegadores (Chinos)](#navegadores-chinos)
  - [Navegador 360](#navegador-360)
  - [Navegador Móvil QQ](#navegador-móvil-qq)
  - [Navegador Móvil UC](#navegador-móvil-uc)
- [Enlaces a aplicaciones](#enlaces-a-aplicaciones)
- [Notas](#notas)
  - [Rendimiento](#rendimiento)
- [Otros recursos](#otros-recursos)
- [Proyectos relacionados](#proyectos-relacionados)
- [Otros formatos](#otros-formatos)
- [Tranducciones](#tranducciones)
- [Contribuciones](#contribuciones)
- [Contribuidores](#contribuidores)
- [Auor](#autor)
- [Licencia](#licencia)

## Mínimo recomendado

Debajo se encuentran las etiquetas esenciales para un sitio web básico:

```html
<!-- Definimos la codificación de caracteres de la página -->
<meta charset="utf-8">
<!-- Indicamos si habrá soporte de modo de documento heredado -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
<!-- Definimos que el sitio tendrá soporte de diseño web responsivo -->
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- Las 3 meta etiquetas arriba *deben* estar primero en el head; cualquier otro contenido del head debe colocarse *después* de estas etiquetas -->
<title>Título de la página</title> 
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Elementos

``` html
<!-- Título del documento -->
<title>Título de página</title>

<!-- Dirección base a usar para todas las direcciones relativas contenidas en el documento -->
<base href="https://ejemplo.com/pagina.html">

<!-- Se agrega CSS Externo a la página-->
<link rel="stylesheet" href="estilos.css">

<!-- CSS incrustado en el documento -->
<style>
  /* ... Estilos aquí*/
</style>

<!-- JavaScript -->
<script src="script.js"></script>
<noscript><!--alternativa que no use JavaScript--></noscript>
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Meta

``` html
<meta charset="utf-8"> <!-- Definimos la codificación de caracteres de la página -->
<meta http-equiv="x-ua-compatible" content="ie=edge"> <!-- Indicamos si habrá soporte de modo de documento heredado -->
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no"> <!-- Definimos que el sitio tendrá soporte de diseño web responsivo -->
<!-- Las 3 meta etiquetas arriba *deben* estar primero en el head; cualquier otro contenido del head debe colocarse *después* de estas etiquetas -->

<!-- Permite control sobre el origen desde donde los recursos son cargados -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
<!-- Debe colocarse lo antes posible en el documento -->
<!-- Solo aplica a contenido debajo de esta etiqueta -->

<!-- Nombre de la aplicación web (solo debe usarse si el sitio web es utilizado como aplicación)-->
<meta name="application-name" content="Nombre de la aplicación">

<!-- Descripción corta de la página (limitado a 150 caracteres) -->
<!-- En *algunas* situaciones esta descripción es usada como parte del extracto mostrado en los resultados de búsqueda -->
<meta name="description" content="Descripción de la página">

<!-- Controla el comportamiento de los motores de búsqueda que visitan e indexan el sitio -->
<meta name="robots" content="index,follow"><!-- Todos los motores de búsqueda -->
<meta name="googlebot" content="index,follow"><!-- Específico para Google -->

<!-- Indica a Google no mostrar la caja de búsqueda de los enlaces del sitio -->
<meta name="google" content="nositelinkssearchbox">

<!-- Indica a Google no proporcionar una traducción para esta página -->
<meta name="google" content="notranslate">

<!-- Verifica pertenencia para la Consola de Búsqueda de Google -->
<meta name="google-site-verification" content="verification_token">

<!-- Verifica pertenencia para Webmasters Yandex -->
<meta name="yandex-verification" content="verification_token">

<!-- Verifica pertenencia para Bing Webmaster Center -->
<meta name="msvalidate.01" content="verification_token">

<!-- Verifica pertenencia para la Consola Alexa -->
<meta name="alexaVerifyID" content="verification_token">

<!-- Verify ownership for Pinterest Console-->
<meta name="p:domain_verify" content="code from pinterest">

<!-- Verifica pertenencia para Norton Sage Web -->
<meta name="norton-safeweb-site-verification" content="norton code">

<!-- Usado para mencionar el programa utilizado para construir el sitio (ej. WordPress, Dreamweaver) -->
<meta name="generator" content="programa">

<!-- Descripción corta del tema de tu sitio -->
<meta name="subject" content="Tema tratado en el sitio">

<!-- Da una clasificación general de edad basada en el contenido en los sitios -->
<meta name="rating" content="General">

<!-- Permite control sobre cómo se pasa información referenciada -->
<meta name="referrer" content="no-referrer">

<!-- Deshabilita la detección automática y formateo de posibles números telefónicos -->
<meta name="format-detection" content="telephone=no">

<!-- Oprtar por la resolución previa de DNS al configurarlo a 'off' -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Almacena cookies en el navegador web del cliente para identificarlo -->
<meta http-equiv="set-cookie" content="name=value; expires=date; path=url">

<!-- Indica que la página aparezca en un frame específico -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Código de país (ISO 3166-1): obligatorio, código de estado (ISO 3166-2): opcional; ej. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- eg. content="New York City" -->
```

- [Meta etiquetas que Google entiende](https://support.google.com/webmasters/answer/79812?hl=es)
- [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions) `(fuente en inglés)`
- [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use) `(fuente en inglés)`
- [Geotagging on Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Link

``` html
<!-- Apunta a una hoja de estilo CSS -->
<link rel="stylesheet" href="https://ejemplo.com/estilos.css">

<!-- Helps prevent duplicate content issues -->
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">

<!-- Used to be included before the icon link, but is deprecated and no longer is used -->
<link rel="shortlink" href="https://example.com/?p=42">

<!-- Links to an AMP HTML version of the current document -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Links to a JSON file that specifies "installation" credentials for web applications -->
<link rel="manifest" href="manifest.json">

<!-- Links to the author of the document -->
<link rel="author" href="humans.txt">

<!-- Refers to a copyright statement that applies to the links context -->
<link rel="license" href="copyright.html">

<!-- Gives a reference to a location in your document that may be in another language -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Gives information about an author or another person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Links to a document that describes a collection of records, documents, or other materials of historical interest. -->
<link rel="archives" href="https://example.com/archives/">

<!-- Links to top level resource in an hierarchical structure -->
<link rel="index" href="https://example.com/">

<!-- Gives a self reference - useful when the document has multiple possible references -->
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">

<!-- The first, next, previous, and last documents in a series of documents, respectively -->
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="prev" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">

<!-- Used when using a 3rd party service to maintain a blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forms an automated comment when another WordPress blog links to your WordPress blog or post -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Notifies a url when you link to it on your site -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Loads in an external HTML file into the current HTML file -->
<link rel="import" href="/path/to/component.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Favicons

``` html
<!-- For IE 10 and below -->
<!-- Place favicon.ico in the root directory - no tag necessary -->

<!-- For IE 11, Chrome, Firefox, Safari, Opera -->
<link rel="icon" type="image/png" sizes="16x16" href="/path/to/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/path/to/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/path/to/favicon-96x96.png">
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Social

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
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Facebook Artículos Instantáneos

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="http://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Instant Articles: Creating Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Instant Articles: Format Reference](https://developers.facebook.com/docs/instant-articles/reference)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Twitter Cards

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://cards-dev.twitter.com/validator)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Pinterest

Pinterest lets you prevent people from saving things from your website, according [to their help center](https://help.pinterest.com/en/articles/prevent-people-saving-things-pinterest-your-site). The `description` is optional.

``` html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

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

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Navegadores / Plataformas

### Apple iOS

``` html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Add to Home Screen -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Touch Icons -->
<!-- In most cases, one 180×180px touch icon in the head is enough -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">
<!-- Note: Safari on iOS 7 doesn’t add effects to icons. -->
<!-- Older versions of Safari will not add effects for icon files named with the -precomposed.png suffix. -->

<!-- Startup Image ( Deprecated ) -->
<link rel="apple-touch-startup-image" href="/path/to/startup.png">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Apple Safari

```html
<!-- Pinned Site -->
<link rel="mask-icon" href="/path/to/icon.svg" color="red">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- Add to home screen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" content="notranslate">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Chrome para móviles (solo Android)

Since Chrome 31, you can set up your web app to "app mode" like Safari.

``` html
<!-- Link to a manifest and define the manifest metadata. -->
<!-- The example of manifest.json could be found in the link below. -->
<link rel="manifest" href="manifest.json">

<!-- Define your web page as a web app -->
<meta name="mobile-web-app-capable" content="yes">

<!-- Homescreen Icon  -->
<link rel="icon" sizes="192x192" href="highres-icon.png">
```

- [Google Developer](https://developer.chrome.com/multidevice/android/installtohomescreen)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- IE10: Disable link highlighting upon tap (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Pinned sites (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Sample Title">
<meta name="msapplication-tooltip" content="A description of what this site does.">
<meta name="msapplication-starturl" content="http://example.com/index.html?pinned=true">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-window" content="width=800;height=600">
<meta name="msapplication-task" content="name=Task 1;action-uri=http://host/Page1.html;icon-uri=http://host/icon1.ico">
<meta name="msapplication-task" content="name=Task 2;action-uri=http://microsoft.com/Page2.html;icon-uri=http://host/icon2.ico">
<meta name="msapplication-badge" value="frequency=NUMBER_IN_MINUTES;polling-uri=http://example.com/path/to/file.xml">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="/path/to/tileimage.jpg">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile;polling-uri2=http://example.com/livetile2">
<meta name="msapplication-task-separator" content="1">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

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
<!-- More info: http://applinks.org/documentation/ -->
```

- [App Links Docs](http://applinks.org/documentation/)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Navegadores (Chinos)

### Navegador 360

``` html
<!-- select rendering engine in order -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Navegador Móvil QQ

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- Display this page in fullscreen -->
<meta name="x5-fullscreen" content="true">
<!-- Page will be displayed in "application mode"(fullscreen,etc.) -->
<meta name="x5-page-mode" content="app">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Navegador Móvil UC

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- Display this page in fullscreen -->
<meta name="full-screen" content="yes">
<!-- UC browser will display images even if in "text mode" -->
<meta name="imagemode" content="force">
<!-- Page will be displayed in "application mode"(fullscreen,forbiding gesture, etc.) -->
<meta name="browsermode" content="application">
<!-- Disabled the UC browser's "night mode" in this page -->
<meta name="nightmode" content="disable">
<!-- Simplify the page to reduce data transfer -->
<meta name="layoutmode" content="fitscreen">
<!-- Disable the UC browser's feature of "scaling font up when there are many words in this page" -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Notas

### Rendimiento
Moving the `href` attribute to the beginning of an element improves compression when GZIP is enabled, because the `href` attribute is used in `a`, `base` and `link` tags.

Example:

``` html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Otros recursos

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Proyectos relacionados

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Otros formatos

- [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Tranducciones

- [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- [Italian](https://github.com/Fakkio/HEAD)
- [Japanese](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- [Russian/Русский](https://github.com/Konfuze/HEAD)
- [Turkish/Türkçe](https://github.com/mkg0/HEAD)
- [Korean](https://github.com/Lutece/HEAD)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Contribución

**Open an issue or a pull request to suggest changes or additions.**

### Guide

The **HEAD** repository consists of two branches:

#### 1. `master`

This branch consists of the `README.md` file that is automatically reflected on the [\<head> Cheat Sheet](http://gethead.info/) website. All changes to the content of the cheat sheet as such should be directed to this file.

Please follow these steps for pull requests:

- Modify only one tag, or one related set of tags at a time
- Use double quotes on attributes
- Don't include a trailing slash in self-closing elements — the HTML5 spec says they're optional
- Consider including a link to documentation that supports your change

#### 2. `gh-pages`

This branch is responsible for the [\<head> Cheat Sheet](http://gethead.info/) website. We use [Jekyll](https://jekyllrb.com/) to deploy the `README.md` Markdown file through [GitHub Pages](https://pages.github.com/). All website related modifications must be directed here.

You might want to go through the [Jekyll Docs](https://jekyllrb.com/docs/home/) and understand how Jekyll works before working on this branch.

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Contribuidores

Check out all the super awesome [contributors](https://github.com/joshbuchea/HEAD/graphs/contributors).

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Autor

**[Josh Buchea](http://joshbuchea.com/)**

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Licencia

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Josh Buchea](http://joshbuchea.com) has waived all copyright and related or neighboring rights to this work.

**[⬆ volver a arriba](#tabla-de-contenidos)**
