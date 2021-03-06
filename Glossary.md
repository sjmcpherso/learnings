# Abbreviations/Terms:

### A
 - <strong>Abstraction</strong> - A process of structuring code to be more readable by making functions shorter and code reuseable. Object-Oriented Programming is an approach to Abstraction.
 - <strong>API (Application Programming Interface)</strong> - is a specification for combining software components.
 - <strong>AJAX (Asynchronous JavaScript and XML)</strong> - Despite the name, the use of XML is not required as JSON is often used instead. With AJAX, web applications can send data, and retrieve data from, a server asynchronously (in the background therefore creating a new code thread) without interfering with the display and behavior of the existing page.
 - <strong>ARIA (Assessability Rich Internet Application</strong> - 
 - <strong>Associative Array</strong> - Abstract data type composed of a collection of key/value pairs. Objects are Associative Arrays in JavaScript
 - <strong>Asynchronous vs Synchronous</strong> - Asynchronouse permits other processing to continue while a transmission is being processed.
 - <strong>Atom</strong> - Building apone RSS, Atom is a XML language used for web feeds.

### B
 - <strong>Backend as a Service (BaaS)</strong> - A backend provider accessed via an API e.g Firebase, Parse, Loopback
 - <strong>BEM (Block Element Modifier)</strong> - A methodology for naming CSS classes by attempting to structure elements into components
 - <strong>Bower</strong> - A front-end package management system that runs on Node.js & npm, that is in the process of being depreciated in favour for Yarn or Webpack

### C
 - <strong>Canonical URL</strong> - The URL used for Search Engines to individualize content which can have multiple URLs i.e A single product maybe found under different categories and therefore have different URLs
 - <strong>CDN (Content Delivery Network)</strong> - is a large distributed system of servers hosting content with high availability and download speeds.
 - <strong>CGI (Common Gateway Interface)</strong> - is the standard method for server-side communication when transfering information between the web server & browser. 
 - <strong>CLI</strong> - Command Line Interface
 - <strong>Closure</strong> - A term used when you nest functions, as inner functions can refer to the variables present in their outer enclosing functions even after their parent functions have already executed. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures, http://jsfiddle.net/sjmcpherso/ByJfv/ 
 - <strong>Concatenation</strong> - The practise of joining two variables together, usually a string or array.
 - <strong>CORS (Cross-Origin Resource Sharing</strong> - CORS defines a way in which a server can authenticate a cross-origin(cross-domain) request from a browser. A CORS compatible browser will send a request with its domain as the value of the 'Origin' in the HTTP header, the server could then compare that domain with a list of allowed domains and if found return that domain as value of 'Access-Control-Allow-Origin' in the response, a wilcard value can be set to allow all domains "Access-Control-Allow-Origin: *". In some cases a browser will perform a preflight request to determine what Methods they can have access to i.e the response could contain 'Access-Control-Allow-Methods: PUT, DELETE'
 - <strong>Concurrency</strong> - A property of computer systems in which multiple computations are executed simultaneously.
 - <strong>Continuous Delivery (CD)</strong> -  A design practise to automate and improve the process of software delivery.
 - <strong>CRUD</strong> - Create, Read, Update, Delete (Also BREAD Browse, Read, Edit, Add, Delete) The major functions that are implemented in relational database applications
 - <strong>cURL</strong> - is a libary & command line tool for transfering data with URL syntax. See https://github.com/curl/curl for more info


### D
 - <strong>Data Binding</strong> - Syncronises data between UI components which are bound to the data source
 - <strong>DDOS (Distributed Denial of Service)</strong> - is a method used to overload a network in an attempt to make it unusable typically achieved by flooding a server with requests, from multiple sources(IP Addresses)
 - <strong>Declarative Programming</strong> - seeks to make you coding more descriptive by using techniques to show what is done rather than how is done. This is opposed to Imperative Programming.
 - <strong>Denormalisation</strong> - Is the process of optimizing the read performance of a database by grouping data by the way it will be accessed, often meaning data is duplicated. This process is generally used for storing data in a NoSQL database.
 - <strong>Dependency Injection(DI)</strong> - is a software design pattern that deals with providing the dependencies that an object needs instead of having it construct them itself. AngularJS utilizes this pattern.
 - <strong>Dirty Checking</strong> - 
 - <strong>Document-oriented Database</strong> - A collection of independent documents. E.g CouchDB, MongoDB
 - <strong>DOM (Document Object Model)</strong> - 
 - <strong>DRY (Don't Repeat Yourself)</strong> - is a principle of software development aimed at reducing repetition of information of all kinds, by making components reuseable.

### E
 - <strong>Emmet</strong> - a plugin for popular text editors which speed of HTML authoring using CSS like abreviations.
 - <strong>Encapsulation</strong> - is a feature of OOP, that allows for separation of an objects implementation and its interface by defining its variables an methods as either public or private.
 - <strong>Epoch</strong> - The "epoch" then serves as a reference point from which time is measured. In most systems/languages this is 01 January 1970 00:00:00 UTC, the most notable exception is Apple's Cocoa(NSDate) which is from 2001
 - <strong>ESI (Edge Side Includes)</strong> - 
 - <strong>Eventual consistency</strong>
 - <strong>Evergreen Browsers</strong> - Web browsers that updates itself without prompting the user.
 - <strong>Explicit Iteration vs Implicit Iteration</strong> - In jQuery:

  ```javascript
  // Explicit iteration with the jQuery .each() method
  $( "li" ).each(function() {
  $(this).addClass( "foo" );
  });
  // jQuery Implicit Iteration
  $( "li" ).addClass( "bar" );
  ```
 - <strong>Expression</strong> - is a reference to a variable or value, or a set of variable(s) and value(s) combined with operators. 

### F
 - <strong>Falsy</strong> - Term for a value which returns 'false' although not nessaarily of boolean type when using Equal/Not Equal operands. i.e. In JavaScript null,false,"",undefined and 0 are Falsy while all other values including Objects are Truthy, So '1 == true' would return true
 - <strong>FastCGI</strong> - A system whereby CGI (Common Gateway Interface) programs stay in memory rather than being spawned as individual process when requested. This makes for much better efficiency. 
 - <strong>Functional Programming</strong> - 

### G
 - <strong>Graceful Degradation</strong> - Follows a top down approach to dealing with features and performance, building with latest technologies that more modern browser can use first then degrading gracefully to fallbacks for browsers that don't support the features used.
 - <strong>Gulp</strong> - is a framework to build, run and test your project. It can process/minify/combine the likes of Less, Sass, JS, HAML, Markdown, CoffeeScript etc create a test enviroment and create a webserver to view your project on.
 - <strong>Grunt</strong> - much like its competitor Gulp above, Grunt is used for creating build scripts although uses a configuration over code syntax.
 - <strong>Gzip</strong> - a method of compressing files to make downloads from Webservers faster

### H
 - <strong>Hash Table</strong> - A data structure that maps keys to values and is used for associative arrays, database indexing, caches, and sets.
 - <strong>Hoisting</strong> - In JavaScript no matter where you declare a variable, its declaration is added to the top of its scope(function) this means JavaScript Scope is different to most other languages that use Block Level Scope inwhich new scope is created within any curly brakets('{}')
 - <strong>HSTS (HTTP Strict Transport Security)</strong> - a web security policy enforcing browsers to only interact with a webserver via secure HTTPS connections as a 301 redirect from HTTP to HTTPS still leaves vunerabilities. HSTS uses the user agent via an HTTPS response header field named "Strict-Transport-Security". i.e  "Strict-Transport-Security: max-age=31536000"
 - <strong>HTTP (Hypertext Transfer Protocol)</strong> - is the underlying protocol used by the web to define the format and transmition between client & server
 - <strong>HTTPS</strong> - Result of layering HTTP on top of a secure protocol like SSL or TLS to provide authentication of the visited website and encripted communication between client & server
 - <strong>HTTP/2</strong> - Offers anumber of performance improvements over the current version of HTTP(HTTP 1.1). HTTP/2 uses multiplexing which allows multiple assets to be sent and received at the same time, the connection is left open for extended periods of time elimating the need for multiple HTTP requests. With HTTP/2 also using compression, performance best practises like minification, concatenation and spriting will likely become unnecessary. Browser support for HTTP/2 is available in the latest browsers but only a few HTTP servers are offering the technology currently.

### I
 - <strong>IDE</strong> - Integrated Development Enviroment is a software application that provides computer programmers with a facility to edit, debug and/or compile source code.
 - <strong>Immediately-Invoked Function Expression (IIFE)</strong> - Also known as Self-executing Anonymous Function is a JavaScript design pattern that uses JS Function Scoping to avoid Variable Hoisting poluting the global scope and calls itself immediately.
 - <strong>Immutable</strong> - Refers to a value or an object that cannot be changed once created.
 - <strong>Interpolation (String/Variable)</strong> - Is a form of template processing where placeholders in string are replaced by their corresponding values.
 - <strong>Isomorphic App</strong> - An application the can run both client-side and server-side.

### J
 - <strong>Jekyll</strong> - A static site generator(Generates HTML without a DB) in the form of a ruby parsing engine which can mimick features of blog software using dynamic components such as templates, partials, markdown, paging, permalinks etc. Made famous by GitHub Pages utilizing it.
 - <strong>JSON (JavaScript Object Notation)</strong> - A lightweight data exchange format.
 - <strong>JSONP (JSON with Padding)</strong> - A technique used to allow the web browser to request data from a different domain, not usually allowed because of the "Same-orgin Policy" by using "script" tags added to the DOM to trigger the request.
 - <strong>JSX (Extension for React)</strong> - An XML like JS syntax extension for creating and editing HTML nodes used by ReactJS
 - <strong>JSX (Progamming Language)</strong> - Static type programming language that compiles to JS.

### L
 - <strong>Loose Coupling</strong> - Coupling measures the degree to which program modules rely on other modules. Loose coupling implies each component can operate or be tested independently of other components.
 - <strong>Loosely Typed</strong> - Describes a programming language whereby it is not necessary to create a variable with a type as apposed to Strongly Typed. e.g JavaScript is a Loose Typed language

### M
 - <strong>Markdown</strong> - A text to HTML conversion tool to simplify and speed up creating structurally valid XHTML text content for websites. http://daringfireball.net/projects/markdown/
  
```HTML
  Header 1 Title
  ===========
  - bullet point  
Will be converted to:  
  <h1>Header 1 Title</h1>
  <li>bullet point</li>
```

 - <strong>MEAN</strong> - Stands for MongoDB, ExpressJS, AngularJS and Node.js is a full-stack JS framework for building single page apps.
 - <strong>Minification</strong> - Removes comments and white space to reduce the file size.
 - <strong>Multiplexing</strong> - 
 - <strong>MVC</strong> - stands for Model View Controller which creates a structure of seperation in an application, the Model being the data, the View the presentation layer and the controller which acts as the glue between the Model & View manipulating Data and recording Events.
 - <strong>MVVM</strong> - stands for Model View ViewModel based on the MVC(Model View Controller) pattern, the difference being the ViewModel is more separated from the Data so that its commands can function without having to know where the data is coming from.
 - <strong>MVW</strong> - stands for Model View Whatever termed to avoid developers arguing over which category MV* Frameworks fall over.

### N
 - <strong>Nginx(pronounced "engine x")</strong> - is a web server and/or reverse proxy server that with a strong focus on high concurrency, performance and low memory usage. Nginx is often used as a proxy server in front of Apache to improve speed for fetching static files.
 - <strong>Node</strong> - or NodeJS is a runtime enviroment for creating server-side JavaScript applications
 - <strong>Normalisation</strong> - Is the process of structuring data in a Relational database so data is less redundant by group data into smaller tables that are linked together by relationships
 - <strong>NPM (Node Package Manager)</strong> - is the default package manager from Node.js and handles download & installation of Node modules

### O
 - <strong>OAuth</strong> - is a open standard for authorization to server resources for client applications. It provides a process for end users to authorize third-party access without needing to share their credentials. OAuth is commonly used as a way for users to log into third party web sites using their Google, Facebook or Twitter passwords, without worrying about their access credentials being compromised.
 - <strong>Obfuscation</strong> - Takes minifying JS a step further by shortening variable and function names. But can introduce bugs if not done properly.
 - <strong>Object Literal</strong> - A comma seperated list of name value pairs housing objects properties and methods.

### P
 - <strong>Parsing</strong> - Taking raw data and converting into a formal data structure.
 - <strong>Primitive Data Type</strong> - A data type that can hold only single value i.e. no properties. In JS Primitive Data Types are Number, String, Boolean, Null, Undefined & Symbol(ES6) whereas Objects & Functions can have properties i.e. var a = {"a":1,"b":2}
 - <strong>Progressive Enhancement</strong> - Uses a bottom up approach to development, aiming to meet a minium requirements then enhancing for more modern technologies.
 - <strong>Prototypal Inheritance</strong> - In JavaScript Objects are inherited from other Objects using the 'new' operator, there is no distinguising between a object & the object it inherits from as opposed to a class based language.

### R
 - <strong>Race Condition</strong> - Are issues that arise when software depends on specific timing of threads to be functional i.e. When an AJAX request a seperate thread is created.
 - <strong>Recursion</strong> - a programming concept for when a function calls itself used as an alternative to iteration. In JS, recusion would utilize the 'return' statement or setTimeout function to call itself.
 - <strong>Relational Database</strong> - built on tables, fields & keys e.g MySQL, SQL Server.
 - <strong>REST (REpresentational State Transfer)</strong> - is a Web service design model, conforming to REST constraits is considered RESTful. REST is Resource based rather than Action based as opposed to SOAP. 
 - <strong>Rich Object Model</strong> - 
 - <strong>Rust</strong> - a systems programming language.

### S
 - <strong>Same Origin Policy</strong> - An important security concept used to stop Client-side programming languages accessing methods and properties across different hostnames.
 - <strong>Sass</strong> - Preproccessor for CSS, which allow you to use Variables, Functions & Calcutions, their are 2 formats the standard .Sass format and the more widely used .Scss format.
 - <strong>Segfault (Segmentation Fault)</strong> - Is an error that generally occurs via a systems programming language accessing a memory location which is not allowed
 - <strong>Semantic HTML</strong> - The use of HTML markup(tags & properties) to give meaning to the information displayed rather than just defining its presentation i.e. rather than &lt;i&gt;Yes&lt;i&gt; use "&lt;em&gt;Yes&lt;em&gt;"(emphasis) or "&lt;span class='emphasis'&gt;Yes&lt;span&gt;"
 - <strong>SemVer (Semantic Versioning)</strong> - Is a versioning guideline to help track changes. The SemVar syntax is in the form MAJOR.MINOR.PATCH, where PATCH is backwards-compatible bug fix, MINOR is a backwards-compatible new feature release and MAJOR is 'breaking change' that is not backwards-compatible. Development should start at 0.1.0 as the first feature set and indicate as production ready with version 1.0.0 
 - <strong>SHA (Secure Hash Algorithm)</strong> - 
 - <strong>Shadow DOM</strong> - 
 - <strong>Singleton</strong> - A programming design pattern which limits the number of instances of a particular object to just one effectively creating a system wide object. E.g The JS Module pattern, Angular Factories and Prototypes
 - <strong>SMACSS ( calable and Modular Architecture for CSS)</strong> - A methodology for CSS which resemebles a style guide for structure CSS
 - <strong>SOAP (Simple Object Access Protocol)</strong> - 
 - <strong>Software Development Lifecycle or Systems Development Lifecycle (SDLC)</strong> - is used to describe a process for planning, creating, testing and deploying a information system.
 - <strong>Software Development Methology</strong> - is a ideology for structuring planning, controlling a software project. 
 - <strong>SPA Single Page Application or Single-page interface (SPI)</strong> - The majority of HTML/CSS & JS is obtained in a single page with the goal of providing a more fluid experience akin to a desktop application.
 - <strong>SDK</strong> - Software Development Kit is a toolkit to allow software development on a specific framework or platform.
 - <strong>SSL (Secure Sockets Layer)</strong> - a internet protocol for secure communication.
 - <strong>SSH (Secure Shell)</strong> - is a network protocol for secure communication over an insecure network.
 - <strong>Statement</strong> - A line of code made of expressions that performs a task in a program. Example: GOTO 100. 
 - <strong>Strict Transport Security</strong> - See HSTS.
 - <strong>Strongly Typed</strong> - Describes a programming language that requires a variable be assigned a type as apposed to Loosely Typed and throws a type error when values of different types a evaluated.
 - <strong>Stub or Method Stub</strong> - Code used to simulate behaviour, often a temporary solution or used to demo functionality.
 - <strong>Surface Web</strong> - the World Wide Web that is indexable by conventional search engines as opposed to the Deep Web with is not reachable by conventional search engines.
 - <strong>SVG (Scalable Vector Graphics)</strong> - is a XML based vector graphics format with some support for interactivity and animations
 - <strong>Stylus</strong> - Another CSS preprocessor which brackets, colons, and semi-colons are all optional. Uses the .styl file extension

### T
 - <strong>Test-driven development (TDD)</strong> - Is a software development process, where a test is created to perform a function then the code is developed to make that test valid.
 - <strong>Three Tier Architecture</strong> - Consists of the Presentation layer or Front End, the Middle tier or Business Logic and the Data tier being where the data is stored.
 - <strong>Two Way Data Binding</strong> - A feature of Silverlight & many MV* JS frameworks where changes by the user in the DOM are reflected in the JS model & changes to the model update the DOM seemlessly.
 - <strong>TypeScript</strong> - Is a programming language built ontop of JS adding support for Types and Annotations that transcompiles to JS.

### U
 - <strong>Unit Testing</strong> - Is a testing method where seperate pieces of source code are created to perform tasks which determine whether module of a program produce the desired outcome.
 - <strong>URI (Uniform Resource Identifier)</strong> - A string used to identify a resource. A URL is a subset of a URI.
 - <strong>User Experience(UX)</strong> - User Experience is a broader which is inclusive yet distinct from the User Interface as it encompasses the way a person feels about using a product, system or service.
 - <strong>User Interface(UI)</strong> - The User Interface are the components which users interact with.

### V
 - <strong>VPN</strong> - Allows users to connect to a private network via the internet 

### W
 - <strong>WebSockets</strong> - Is a protocol for realtime two-way communication between a client & server over a standard TCP connection.
 - <strong>WebRTC (Web Real-Time Commnunication)</strong> - Is an API definition which allows peer-to-peer data communication. Which gives supporting browsers the ability to facilitate Video/Audio chat & data transfer via a web application.

### X
 - <strong>XSS/Cross-site Scripting</strong> - Is a security vunerability usually involving client-side script malicioulsy injected into a webpage by not properly escaping form field entry.
