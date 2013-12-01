# RequireYou

Applying requirejs thoughts to the whole front-end project , and reduce the knowledge pressure to developers .

the project maybe develop with b++(a new language ) concurrently, so I wish requireYou can stand a height of language and machine.

RequireYou loads all kinds of functionality frameworks as well as more defined modules. It is
optimized for in-browser use, including in
[a Web Worker](http://requirejs.org/docs/api.html#webworker), It implements the
[DRY](https://en.wikipedia.org/wiki/Don't_repeat_yourself).

RequireYou uses requirejs syntax to load frameworks, so it should be asynchronous defaultly. It can be used
[simply to load existing JavaScript files](by bower).

RequireYou includes [an optimization tool](by requirejs)
you can run as part of your packaging steps for deploying your code. The
optimization tool can combine and minify your JavaScript files to allow for
better performance.

If the JavaScript file defines a JavaScript module via
[define()](http://requirejs.org/docs/api.html#define), then there are other benefits
RequireYou can offer: [improvements over traditional CommonJS modules](http://requirejs.org/docs/commonjs.html)
and [loading multiple versions](http://requirejs.org/docs/api.html#multiversion)
of a module in a page. RequireYou should be extensible so a plugin system is feasible.

RequireYou has dependencies on some front-end tech like coffeescript , jquery, qunit etc. it is inspired and converted from requirejs, i.e. it is a fork of requirejs.
It is dual-licensed -- new BSD or MIT.

The standard requireYou file is around KB when minified via Grunt-contrib-jsmin. the project is managed by yeoman including yeoman generator, bower and grunt.

some code is developed on ipad. editor is Fastkeyboard sometimes. code sharing website is jsbin. you can file bugs or contact author by issue tracker of GitHub , or email to qcgm197874@gmail.com 

RequireYou is future-oriented, so it plans to support the newest browsers especially Chrome because it updates fast and debug easily, and coast by Opera should be compatible . of course it depends on the invoked frameworks also.

downloading tool:bower

system compatible: windows8

cli: powershell 3

doc generation : grunt-contrib-yuidoc, and it perhaps use other generation tool like what coffeescript does.

test framework: qunit. it can be reference in jsbin, but it is to integrate into webstorm.

[Latest Release](plan time: before 2013-12-31)

## Directories

* **dist**: Scripts and assets to generate the requirejs.org docs, and for
generating a require.js release.
* **docs**: The raw HTML files for the requirejs.org docs. Only includes the
body of each page. Files in **dist** are used to generate a complete HTML page.
* **tests**: Tests for require.js.
* **testBaseUrl.js**: A file used in the tests inside **tests**. Purposely
placed outside the tests directory for testing paths that go outside a baseUrl.
* **updatesubs.sh**: Updates projects that depend on require.js Assumes the
projects are siblings to this directory and have specific names. Useful to
copy require.js to dependent projects easily while in development.

## Tests

This repo assumes some other repos are checked out as siblings to this repo:

    git clone https://github.com/requirejs/text.git
    git clone https://github.com/requirejs/i18n.git
    git clone https://github.com/requirejs/domReady.git
    git clone https://github.com/requirejs/requirejs.git

So when the above clones are done, the directory structure should look like:

* domReady
* i18n
* text
* requirejs (this repo)

You will need to be connected to the internet because the JSONP and
remoteUrls tests access the internet to complete their tests.

Serve the directory with these 4 siblings from a web server. It can be a local web server.

Open requirejs/tests/index.html in all the browsers, click the arrow button to run all
the tests.
