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
<!-- Definimos la codificación de caracteres de la página -->
<meta charset="utf-8"> 
<!-- Indicamos si habrá soporte de modo de documento heredado -->
<meta http-equiv="x-ua-compatible" content="ie=edge"> 
<!-- Definimos que el sitio tendrá soporte de diseño web responsivo -->
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no"> 
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

<!-- Ayuda a prevenir problemas con duplicación de contenido -->
<link rel="canonical" href="https://ejemplo.com/2017/06/9-consejos-para-seo.html">

<!-- Usado para ser incluido antes del icono de enlace, pero esta obsoleto y no se utiliza más -->
<link rel="shortlink" href="https://ejemplo.com/?p=42">

<!-- Enlace para la versión HTML AMP del documento actual -->
<link rel="amphtml" href="https://ejemplo.com/ruta/a/version-amp.html">

<!-- Enlaces a un archivo JSON que específica las credenciales de "instalación" para aplicaciones web -->
<link rel="manifest" href="manifest.json">

<!-- Enlace al autor del documento -->
<link rel="author" href="humans.txt">

<!-- Referencia a la declaración de copyright que aplica al contexto del enlace -->
<link rel="license" href="copyright.html">

<!-- Proporciona una referencia a la ubicación en tu documento que puede estar en otro lenguaje -->
<link rel="alternate" href="https://en.ejemplo.com/" hreflang="en">

<!-- Proporciona información acerca del autor u otra persona -->
<link rel="me" href="https://google.com/perfiles/web" type="text/html">
<link rel="me" href="mailto:nombre@ejemplo.com">
<link rel="me" href="sms:+15035550125">

<!-- Enlaza a un documento que describe una colección de registros, documentos u otros materiales de interés histórico. -->
<link rel="archives" href="https://ejemplo.com/archivos/">

<!-- Enlaza a un recurso de alto nivel en una estructura jerarquica -->
<link rel="index" href="https://ejemplo.com/">

<!-- Proporciona una auto referencia - útil cuando el documento tiene multiples referencias -->
<link rel="self" type="application/atom+xml" href="https://ejemplo.com/atomFeed.php?pagina=3">

<!-- El primero, el siguiente, el anterior y el último documento en una serie de documentos, respectivamente -->
<link rel="first" href="https://ejemplo.com/atomFeed.php">
<link rel="next" href="https://ejemplo.com/atomFeed.php?pagina=4">
<link rel="prev" href="https://ejemplo.com/atomFeed.php?pagina=2">
<link rel="last" href="https://ejemplo.com/atomFeed.php?pagina=147">

<!-- Usado al utilizar un servicio de terceros para mantener un blog -->
<link rel="EditURI" href="https://ejemplo.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Genera un comentario automatizado cuando otro blog WordPress usa un enlace hacia tu blog o publicación WordPress -->
<link rel="pingback" href="https://ejemplo.com/xmlrpc.php">

<!-- Notifica a una url cuando la enlazas a tu sitio -->
<link rel="webmention" href="https://ejemplo.com/webmention">

<!-- Carga un archivo HTML externo en el archivo HTML actual -->
<link rel="import" href="/ruta/a/componente.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Título de búsqueda">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://ejemplo.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//ejemplo.com/">
<link rel="preconnect" href="https://www.ejemplo.com/">
<link rel="prefetch" href="https://www.ejemplo.com/">
<link rel="prerender" href="https://ejemplo.com/">
<link rel="preload" href="image.png" as="image">
<!-- Más información: https://css-tricks.com/prefetching-preloading-prebrowsing/  (fuente en inglés)-->
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Favicons

``` html
<!-- Para IE 10 y versiones inferiores -->
<!-- Coloca el facivon.ico en la raíz del directorio - no requiere etiqueta -->

<!-- Para IE 11, Chrome, Firefox, Safari, Opera -->
<!-- Se recomienda usar un archivo .PNG sobre un archivo .ico -->
<link rel="icon" type="image/png" sizes="16x16" href="/ruta/a/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/ruta/a/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/ruta/a/favicon-96x96.png">
```

- [Todo acerca de Favicons (y Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/) `(fuente en inglés)`
- [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Social

### Facebook Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://ejemplo.com/pagina.html">
<meta property="og:type" content="sitio web">
<meta property="og:title" content="Título del contenido">
<meta property="og:image" content="https://ejemplo.com/imagen.jpg">
<meta property="og:description" content="Descripción aquí">
<meta property="og:site_name" content="Nombre del sitio">
<meta property="og:locale" content="es_ES">
<meta property="article:author" content="Autor">
```

- [Guía para webmasters sobre el uso compartido](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Protocolo Open Graph](http://ogp.me/) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Facebook Artículos Instantáneos

``` html
<!-- Definimos el juego de caracteres del documento -->
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- URL de la versión web de tu artículo -->
<link rel="canonical" href="http://ejemplo.com/articulo.html">

<!-- El estilo a utilizar para este artículo -->
<meta property="fb:article_style" content="miestilodearticulo">
```

- [Crear un artículo instantáneo](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Ejemplos de código de artículos instantáneos](https://developers.facebook.com/docs/instant-articles/reference)

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Twitter Cards

``` html
<meta name="twitter:card" content="resumen">
<meta name="twitter:site" content="@cuenta_del_sitio">
<meta name="twitter:creator" content="@cuenta_de_creador">
<meta name="twitter:url" content="https://ejemplo.com/pagina.html">
<meta name="twitter:title" content="Título del contenido">
<meta name="twitter:description" content="Descripción del contenido menor a 200 caracteres">
<meta name="twitter:image" content="https://ejemplo.com/imagen.jpg">
```

- [Twitter Cards: Guía de inicio](https://dev.twitter.com/cards/getting-started) `(fuente en inglés)`
- [Validador de Twitter Card](https://cards-dev.twitter.com/validator) `(herramienta en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Título del contenido">
<meta itemprop="description" content="Descripción del contenido menor a 200 caracteres">
<meta itemprop="image" content="https://ejemplo.com/imagen.jpg">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Pinterest

Pinterest permite prevenir que personas guarden cosas desde tu sitio web,de acuerdo a [su centro de ayuda](https://help.pinterest.com/es/articles/prevent-pinning-your-site). La `descripción` es opcional.

``` html
<meta name="pinterest" content="nopin" description="¡Lo sentimos, no puedes guardar desde este sitio!">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://ejemplo.com/servicios/oembed?url=http%3A%2F%2Fejemplo.com%2Ffoo%2F&amp;format=json"
  title="Perfil oEmbed: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://ejemplo.com/servicios/oembed?url=http%3A%2F%2Fejemplo.com%2Ffoo%2F&amp;format=xml"
  title="Perfil oEmbed: XML">
```

- [oEmbed format](http://oembed.com/) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Navegadores / Plataformas

### Apple iOS

``` html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Deshabilita la detección automática y formateo de números telefónicos -->
<meta name="format-detection" content="telephone=no">

<!-- Agregar a pantalla de inicio -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="Título de aplicación">

<!-- Touch Icons -->
<!-- En la mayoría de los casos, un touch icon de 180x180px en el head es suficiente -->
<link rel="apple-touch-icon" href="/ruta/a/apple-touch-icon.png">
<!-- Nota: Safari en iOS 7 no agrega efectos a los íconos. -->
<!-- Versiones anteriores de Safari no agregaran efectos a los archivos de iconos nombrados con el sufijo -precompised.png -->

<!-- Imagen de arranque ( Obsoleto ) -->
<link rel="apple-touch-startup-image" href="/ruta/a/arranque.png">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- [Meta etiquetas Apple](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Apple Safari

```html
<!-- Sitio fijado -->
<link rel="mask-icon" href="/ruta/a/icono.svg" color="red">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Android

``` html
<!-- Define el color de la barra de tareas del dispositivo -->
<meta name="theme-color" content="#E64545">

<!-- Agregar a la pantalla de inicio -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen fuente en inglés -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=nombre-del-paquete">
<link rel="alternate" href="android-app://nombre-del-paquete/http/url-ejemplo.com">
```

- [Personalización del navegador](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/?hl=es)


**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Deshabilita sugerencia de traducción -->
<meta name="google" content="notranslate">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Google Chrome para móviles (solo Android)

Desde la versión 31 de Chrome, puedes configurar tu aplicación web a "modo aplicación" como en Safari.

``` html
<!-- Enlace a manifest define metadatos del manifest. -->
<!-- Ejemplo de manifest.json puede verse en el enlace debajo. -->
<link rel="manifest" href="manifest.json">

<!-- Define tu página web como una aplicación web -->
<meta name="mobile-web-app-capable" content="yes">

<!-- Homescreen Icon  -->
<link rel="icon" sizes="192x192" href="highres-icon.png">
```

- [Google Developer](https://developer.chrome.com/multidevice/android/installtohomescreen) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- IE10: Dishabilita el resaltado a enlaces al hacer tap(https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) fuente en inglés -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Sitios fijados (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Título de ejemplo">
<meta name="msapplication-tooltip" content="Descripción de lo que el sitio hace.">
<meta name="msapplication-starturl" content="http://ejemplo.com/index.html?pinned=true">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-window" content="width=800;height=600">
<meta name="msapplication-task" content="name=Task 1;action-uri=http://host/Page1.html;icon-uri=http://host/icon1.ico">
<meta name="msapplication-task" content="name=Task 2;action-uri=http://microsoft.com/Page2.html;icon-uri=http://host/icon2.ico">
<meta name="msapplication-badge" value="frequency=NUMBER_IN_MINUTES;polling-uri=http://ejemplo.com/ruta/a/archivo.xml">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="/ruta/a/tileimage.jpg">

<meta name="msapplication-config" content="http://ejemplo.com/browserconfig.xml">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://ejemplo.com/livetile;polling-uri2=http://ejemplo.com/livetile2">
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

- [App Links Docs](http://applinks.org/documentation/) `(fuente en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Navegadores (Chinos)

### Navegador 360

``` html
<!-- seleccionar el orden de motor de renderizado -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Navegador Móvil QQ

``` html
<!-- Bloquea la pantalla en una orientación específica -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- Despliega la página en modo pantalla completa -->
<meta name="x5-fullscreen" content="true">
<!-- La página se desplegará en "modo aplicación"(fullscreen,etc.) -->
<meta name="x5-page-mode" content="app">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

### Navegador Móvil UC

``` html
<!-- Bloquea la pantalla en una orientación específica -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- Despliega la página en modo pantalla completa -->
<meta name="full-screen" content="yes">
<!-- El navegador UC mostrará imágenes aunque este en "modo texto" -->
<meta name="imagemode" content="force">
<!-- La página se mostrará en "modo aplicación"(fullscreen,forbiding gesture, etc.) -->
<meta name="browsermode" content="application">
<!-- Deshabilitar el modo nocturno del navegador UC en esta página -->
<meta name="nightmode" content="disable">
<!-- Simplificar la página para reducir la transferencia de datos -->
<meta name="layoutmode" content="fitscreen">
<!-- Deshabilitar la función del navegador UC de "escalar la fuente cuando hay muchas palabras en la página"-->
<meta name="wap-font-scale" content="no">
```

- [Documentación del navegador UC](http://www.uc.cn/download/UCBrowser_U3_API.doc) `(documento en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Notas

### Rendimiento

Movier el atributo `href` al inicio de un elemento mejora la compresión cuando GZIP está habilitado, el atributo `href` es usado en las etiquetas `a`, `base` y `link`.

Ejemplo:

``` html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Otros recursos

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md) `(repositorio en inglés)`
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md) `(repositorio en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Proyectos relacionados

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets `(repositorio en inglés)`
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets `(repositorio en inglés)`
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets `(repositorio en inglés)`
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js `(repositorio en inglés)`

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Otros formatos

- [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Tranducciones

- [Portugués brazileño](https://github.com/Webschool-io/HEAD)
- [Chino (Simplificado)](https://github.com/Amery2010/HEAD)
- [Italiano](https://github.com/Fakkio/HEAD)
- [Japonés](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- [Ruso/Русский](https://github.com/Konfuze/HEAD)
- [Turco/Türkçe](https://github.com/mkg0/HEAD)
- [Coreano](https://github.com/Lutece/HEAD)

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Contribución

**Abre un issue o pull request para sugerencias o agregar contenido.**

### Guía

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

Check out all the super awesome [contributors](https://github.com/eoasakura/HEAD-ES/graphs/contributors).

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Autor

**[Josh Buchea](http://joshbuchea.com/)**

**[⬆ volver a arriba](#tabla-de-contenidos)**

## Licencia

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Josh Buchea](http://joshbuchea.com) has waived all copyright and related or neighboring rights to this work.

**[⬆ volver a arriba](#tabla-de-contenidos)**
