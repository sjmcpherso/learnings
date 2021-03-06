<h1>HTML</h1>

<!-- doctoc HTML.md JavaScript.md CSS.md -->
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
### Contents

- [HTML Doctype](#html-doctype)
- [The Viewport](#the-viewport)
  - [Compatibility Mode](#compatibility-mode)
- [Loading Resources](#loading-resources)
- [Images/Graphics](#imagesgraphics)
  - [Image/Graphic Elements](#imagegraphic-elements)
  - [Image/Graphic Formats](#imagegraphic-formats)
  - [Image/Graphic Performance](#imagegraphic-performance)
- [HTML5 Forms](#html5-forms)
    - [Form Inputs](#form-inputs)
    - [Form Attributes](#form-attributes)
- [Other Elements/APIs](#other-elementsapis)
- [HTML Preprocessors](#html-preprocessors)
- [SEO Optimization](#seo-optimization)
    - [Microdata](#microdata)
- [Web Components](#web-components)
    - [Custom Elements](#custom-elements)
    - [HTML Templates](#html-templates)
    - [HTML Imports](#html-imports)
    - [Shadow DOM](#shadow-dom)
- [HTML Performance](#html-performance)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<h2>HTML Doctype</h2>

 - <strong>HTML5 Doctype &lt;!doctype html&gt;</strong> must be first on page before the <html> tag. IE will revert to Quirks Mode if not the case
 - <strong>HTML4 vs HTML5</strong> - In HTML4, there are 2 types of elements: Block and Inline. HTML5 emphasizes semantics and structure, so it has organized its elements into the categories of metadata, flow, sectioning, heading, phrasing, interactive & embedded

<h2>The Viewport</h2>

 - The recommened viewport setting for responsive design '&lt;meta name="viewport" content="width=device-width"&gt;' this allows the user to zoom.
 - To disable zooming use '&lt;meta name="viewport" content="maximum-scale=1"&gt;' this would be recommend for a Mobile Web App.
 - Alternatively to disable a responsive design use '&lt;meta name="viewport" content="width=1200"&gt;' the width being the size of your outer container.
 - See https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html for more info.

<h3>Compatibility Mode</h3>

- Internet Explorer 8/9/10 support document compatibility modes that affect the way webpages are interpreted and displayed, its possible those versions will not use the latest rendering engine, instead using the Internet Explorer 5.5 rendering engine. To avoid this set the X-UA-Compatible meta tag: "&lt;meta http-equiv="X-UA-Compatible" content="IE=edge"&gt;"
- There are some complications that may cause the X-UA-Compatible meta tag not to work and in that case it needs to be set in the HTTP request header. See https://hsivonen.fi/doctype/


<h2>Loading Resources</h2>

 - The Protocol-relative URL &lt;img src="//domain.com/img/logo.png"&gt; Note: Using protocol relative URLs for stylesheets in IE7 & 8 will mean the file is download twice. For More Info http://paulirish.com/2010/the-protocol-relative-url/
 - The "download" attribute forces browser to invoke download dialog &lt;a href="logo.png" download="Logo.png"&gt;download me&lt;/a&gt; Chrome Only



<h2>Images/Graphics</h2>

<h3>Image/Graphic Elements</h3>

 - <strong>&lt;figure&gt;</strong> element is used to markup illustrations, graphs, code snippets and images used with &lt;figurecaption&gt; IE9+

```HTML
<figure>
  <img src="mdn-logo-sm.png" alt="An awesome picture">
  <figcaption>Fig1. MDN Logo</figcaption>
</figure>
```

 - <strong>&lt;picture&gt;</strong> element is a container to specify multiple sources for a specific image, using the media query attribute or mimetype attribute the browser can determine if the source is suitable or fallback to the standard img element enclosed before the end of the 'picture' element. Giving the ability to deal with responsive images and  non-cross-browser compatible file formants.  Firefox, Chrome, Opera, Edge Only http://caniuse.com/#feat=picture

```HTML
<picture>
  <source srcset="mdn-logo-wide.png" media="(min-width: 600px)">
  <source srcset="mdn-logo.svg" type="image/svg+xml">
  <img src="mdn-logo-narrow.png" alt="MDN">
</picture>
```

<h3>Image/Graphic Formats</h3>

 - <strong>GIF (Graphics Interchange Format)</strong> - Lossless format that can have transparency & animation with a maximum of 256 colors.
 - <strong>BMP (Bitmap Image Format)</strong> - A less used raster image format.
 - <strong>PNG (Portable Network Graphics)</strong> - Lossless graphic file format with 24bit colors & supports transparency. Also a less used 8bit version that only support 256 colors.
 - <strong>APNG (Animated PNG)</strong> - A PNG but allows frames for animation. Limited support - FF & Safari only
 - <strong>JPEG/JPG (Joint Photographic Experts Group)</strong> -  Lossy compression whereby the level of compression can be adjusted supports a maximum image size of 65535×65535 pixels
- <strong>Progressive vs Baseline JPEGs</strong> -  A Progressive jpeg is a series of scans of increasing quality, a Baseline jpeg is a single full resolution scan, Progressive JPEGs load faster on IE9, Chrome & Firefox but use more CPU. http://calendar.perfplanet.com/2012/progressive-jpegs-a-new-best-practice/
 - <strong>WebP</strong> is a new image format developed by Google, superior to PNG and JPG. It produces 24-35% lossy & lossless images, browser support is limited to Chrome & Android Browsers but fallbacks can be provided using the &lt;picture&gt; element. In the below example if 'webp' or the &lt;picture&gt; element isn't supported(IE)the img element is used as a fallback with a 'jpg'. 

```HTML
<picture>
  <source srcset="img/awesomeWebPImage.webp" type="image/webp">
  <img src="img/creakyOldJPEG.jpg" alt="Alt Text!">
</picture>
 ```
 
 - <strong>SVG (Scalable Vector Graphics )</strong> - is a XML markup language for describing & plotting vector graphics

<h4>SVG (Scalable Vector Graphics)</h4>
 - SVGs is a XML markup language for describing & plotting vector graphics but have a number of quirks between browsers. IE9+ IE9-IE11 has some scaling issues which can be addressed by adding height, width, viewBox and/or CSS rules seen here https://codepen.io/tomByrer/pen/qEBbzw
 

<h4>Image/Graphic Performance</h4>
 - <strong>Specifing image size attributes</strong> by specifying a width and height for all images allows for faster rendering by eliminating the need for unnecessary reflows and repaints.



<h2>HTML5 Forms</h2>

<h4>Form Inputs</h4>

- <strong>New Input types</strong> - HTML5 introduces a number of new input types all have varing browser support. color, date, datetime, datetime-local, email, month, number, range, search, tel, time, url, week. Modernizr can be used to determine support and if not fallback to input="text" or to avoid browser specific support.
- <strong>type="search"</strong> - In Webkit browsers it adds a Clear field button and as a result Webkit browsers style it differently.  In Chrome hitting 'Esc' will clear field.
- <strong>Meter</strong> &lt;meter value="2" min="0" max="10"&gt;2 out of 10&lt;/meter&gt; tag defines a measurement within a known range, or a fractional value.
- <strong>Datalist</strong> - &lt;datalist&gt; Databinding Autocomplete. IE10+, No Safari support. Example:
```HTML
<input list="browsers">
<datalist id="browsers">
     <option value="Chrome">
     <option value="Firefox">
     <option value="Safari">
</datalist>
```

<h4>Form Attributes</h4>

- <strong>required="required"</strong> - The required attribute is used for validation and most modern browsers will check this attribute & add there own native validation errors when submitting the form.
- <strong>placeholder="Enter Here"</strong> - Text is displayed inside the input field as long as the field is empty. When you click on (or tab to) the input field and start typing, the placeholder text disappears. IE10+, polyfill fallback jquery-placeholder.js for IE9 & below.
- Autofocus attribute - On page load set focus to element. Can be used on inputs buttons and textareas. e.g <input autofocus /> IE10+
- <strong>contenteditable="true"</strong> - The attribute contenteditable="true" is used to allow text elements the abilty to be typed into like a textbox e.g. http://jsfiddle.net/sjmcpherso/q3kWw/ (Full Support). Similarly the CSS attribute. -moz-user-input:enabled can be use to replicate but with only support for Firefox.
- <strong>spellcheck="true"</strong> - when set to true on an input, textarea and a contenteditable set element will tell the browser(if supported) to check the spelling of element and add a red underline to a word it deems incorrect. By default the attribute is false for inputs and true for textareas and contenteditible in most browsers.
- <strong>autocorrect="false"</strong> - Used specifically by Touch device web browsers to offer options to correct potential spelling mistakes. Disabled by default on input="email"
- <strong>autocapitalize="false"</strong> - Used specifically by Touch device web browsers to Autocapitalize the first letter in an input. Disabled by default on input="email"
- <strong>autocomplete="email"</strong> - Used by browser to autopopulate a field based on previously entered data. Set by default on most modern browsers determind by the id/name.
```HTML
    <input type="email" name="email" id="email" autocomplete="email">
```

- <strong>inputputmode="numeric"</strong> - On iOS & Android mobile browsers will display a 10-key phone-like keypad, Firefox OS requires the attribute: x-inputmode="numeric"


<h2>Other Elements/APIs</h2>

<h3>Video Element/API</h3>

 - &lt;video autoplay controls&gt;&lt;/video&gt;
- CDATA witten in HTML as <![CDATA[]]> is a section of element content that is marked for the parser to interpret as only character data, not markup i.e. Like a comment although is still part of the document and therefore can be read from JS.
- Cookies vs sessionStorage vs localStorage - Cookies are for storing small amounts of website data, such as a username. HTML5 Web Storage is a faster and larger method created by the browser, sessionsStorage expires after the browser window closes, and localStorage is for persistant data.
- Application Cache (AppCache)

<h3>Dialog Element/API</h3>

- The Dialog Element is for including a native popup and can be manipulated with .show(), .close() calls with with limited browser support (Chrome Only) see https://codepen.io/sjmcpherson/pen/PawdeM for example
```HTML
<dialog open id="dialog">
  <p>Hi, I'm a dialog!</p>
  <button id="close">Okay</button>
</dialog>
<button id="show">Open Dialog!</button>
```

<h2>HTML Preprocessors</h2>

- <strong>Markdown</strong> -  A text-to-HTML conversion tool, used as a format for writing content for the web. Uses linebreaks used to determine closing of many block tags. Allows compiled HTML.

- <strong>Jade</strong> - is NodeJS based, HTML precompiler with a powerful templating engine. Jade like HAML uses indenting to determine HTML element hieracy and as a result will not accept unminfied HTML, forcing the developer to use the Jade syntax.

- <strong>HAML (HTML Abstraction Markup Language)</strong> is a lightweight Ruby based markup language. Example:

```HTML
  %body
    #header
      %h1 BoBlog
```
Would Produce:
```HTML
  <body>
    <div id='header'>
      <h1>BoBlog</h1>
    </div>
```


| Preprocessor  | Extension  | Can Use Standard HTML  | Uses Tabs for Hierachy    |
| ------------- |:-------------:| -----:| -----:|
| Markdown | .md      | true  | false  |
| Jade      | .jade | false  | true |
| Haml      | .haml      | true  | true  |


<h2>SEO Optimization</h2>

- Include descriptive terms to your URLs and create a easily to understand hierarchy, i.e. List of Products at “www.yoursite.com/products/” individual products at “www.yoursite.com/products/descriptive-product-name/”
- Make use of header tag. h1,h2,h3,h4,h5 tags to emphasize important text but use sparingly across the page.
- Place links on descriptive wording rather than text such as "Click Here" and load the Title attribute with info about the link i.e

```HTML
To read our View our website, click <a href="http://www.instantshift.com">here</a>. <!- Not terrible ->

Visit <a href="http://www.smashdynamic.com" title="Visit Smash Dynamic magazine, Web Development">Smash Dynamic, web design & development specialists</a>. <!- Much better ->
```

- When using images add a description to the “Alt” tag of the image markup.
- Create unique meta title tags for each page which are brief but descriptive (info on Meta Tags here) https://support.google.com/webmasters/answer/79812?hl=en&ref_topic=2371375
- Include important keywords in your text but don’t overdo it as Google will see this as content manipulation. And of course you should always be thinking of your audience not just your page ranking.
- You may find the need to abreviate important terms to make you content more concise use the 'abbr' tag to get the best of both worlds i.e. <abbr title="Front End Developer">FED</abbr>
- An under-utilized and often misunderstood element is the Definition List, semantically correct when displaying a list of titles with a description
```HTML
    <dl><!--Container-->
       <dt>Definition Term (like a title)</dt>
       <dd>Definition Description</dd>
    </dl>
```

<h4>Microdata</h4>

- Microdata is a way to label content as a specific type of information for Search Engines to process, for example reviews, personal information, products, locations & events.
- Use the Microdata specification to add metadata to content i.e
```HTML
<section itemscope itemtype="http://schema.org/Person">
        Hello, my name is
        <span itemprop="name">John Doe</span>,
        I am a
        <span itemprop="jobTitle">graduate research assistant</span>
        at the
        <span itemprop="affiliation">University of Dreams</span>.
        My friends call me
        <span itemprop="additionalName">Johnny</span>.
        You can visit my homepage at
        <a href="http://www.JohnnyD.com" itemprop="url">www.JohnnyD.com</a>.
        <section itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
                I live at
                <span itemprop="streetAddress">1234 Peach Drive</span>,
                <span itemprop="addressLocality">Warner Robins</span>,
                <span itemprop="addressRegion">Georgia</span>.
       </section>
</section>
```
 - Use the  Google Data Testing tool to validate https://developers.google.com/structured-data/testing-tool/



<h2>Web Components</h2>

- A new specification for creating encapsulated, reusable widgets, the 4 components that make up the spec are Custom Elements, HTML Imports, Templates and Shadow DOM. Limited browser support, Only Chrome & Opera currently implement all 4 features, Safari & Firefox just HTML Templates. IE12 Unlikely to have any support. http://webcomponents.org/
- <strong>Web Components Frameworks</strong> - add polyfils and intergrate web components with frameworks such as X-Tags, Polymer & Bosonic.

<h4>Custom Elements</h4>

- Define and use new types of DOM elements, its name must contain a dash, and its prototype must extend HTMLElement. i.e <custom-element></custom-element>. All native tag names do not contain a dash.

<h4>HTML Templates</h4>

 - Wrap any scripts, css or markup in a "template" tag to ignore parsing the contents until   i.e. images won't load, scripts won't run, elements will not render etc until specified via JavaScript i.e.

```HTML
<template id="template">
  <style>
    ...
  </style>
  <h1>Template Web Component</h1>
  <image src="image.png" />
</template>
<script>
  var template = document.querySelector('#template');
  var clone = document.importNode(template.content, true);
  document.body.appendChild(clone);
</script>
```

<h4>HTML Imports</h4>

 - Allows importing of external html file through an http request that can then be rendered to the page.
 - For HTML imports use the "import" value on the "rel" attribute in a standard <link> tag, for example: '&lt;link rel="import" href="import-file.html"&gt;'
 - Note: HTML imports adhere to the same-origin policy for security reasons. Therefore, if you wish to import an HTML document from an external domain, you need to make sure you have CORS set up correctly.
 - Limited support in Chrome & Opera Only.

<h4>Shadow DOM</h4>

- Already the browser uses Shadow DOM simplify complex elements like '&lt;input type="date"&gt;', '&lt;select&gt;', '&lt;video&gt;' etc
- Style & Script encapusation inside Shadow DOM


<h2>HTML Performance</h2>

 - Reduce unecessary html tags to improve performance
 - Reduce the total number of referenced files to css, js & images by using image sprites and combining CSS & JavaScript. Because of the round-trip to the server extra HTTP requests add to the download time and most browsers limit the number of concurrent downloads per host to between 2-8. For individual browser limitations see http://www.browserscope.org/?category=network
 - Putting stylesheets in the &lt;head&gt; allows the page to render progressively and avoid potential browser repaints.
 - Use dispersed servers(CDN) for referenced files such as css, js & images. So resources
 - For common libraries using a popular CDN(such as //ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js) can enhance the chance the user has the file cached.
 - To give more control and to speed up loading time of Web Fonts use Web Font Loader, Fonts provided by Typekit, FontDeck and Google can be loaded through the script, for best performance embed the script directly after head tag and to remove FOUT add CSS for the class ".wf-loading" on the HTML element to hide text e.g. *.wf-loading{opacity(0)} the script then removes this class once fonts are loaded. https://developers.google.com/fonts/docs/webfont_loader
 - Place Google Analytics code at bottom even though Google recommends placing in the head, as pageviews will be tracked even if they leave the page before fully loaded also keeps the all the scripts together.
 - Use Link Prefetching (limited browser support) to preload whole pages or just images, css etc.

```HTML
<!-- full page -->
<link rel="prefetch" href="http://davidwalsh.name/css-enhancements-user-experience" />
<!-- just an image -->
<link rel="prefetch" href="http://davidwalsh.name/wp-content/themes/walshbook3/images/sprite.png" />
```

 - Like Link Prefetching DNS prefetch will preload the DNS for external url, helpful when a particular page contains a number of external links but also in the case where browsers will limit the number of simulatanious connections to a host.
 
```HTML
<!-- Google Analytics -->
<link rel="dns-prefetch" href="//www.google-analytics.com">
<!-- Google Fonts -->
<link rel="dns-prefetch" href="//fonts.googleapis.com">
```

```HTML
<!-- full page -->
<link rel="dns-prefetch" href="http://davidwalsh.name/css-enhancements-user-experience" />
<!-- just an image -->
<link rel="prefetch" href="http://davidwalsh.name/wp-content/themes/walshbook3/images/sprite.png" />
```

- Compress Your Images - Photoshop does a fairly decent job at optimizing images but their are other tools that can take you files and compress them even further. Yahoo's www.smushit.com does a good job with PNG's & GIF's & theres also FileOptimizer a Desktop app that compresses images and a number of other file formats.
