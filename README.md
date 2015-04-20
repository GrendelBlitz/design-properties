Design Properties
=================

Salesforce1 Design Properties covers text colors, background colors, font sizes, font faces, spacing, borders, etc.
The Design Properties are stored in an abstract JSON format and can be transformed with [theo](https://github.com/salesforce-ux/theo) into other formats like:
- [Sass](http://sass-lang.com)
- [Less](http://lesscss.org)
- [Stylus](http://learnboost.github.io/stylus)
- Android XML
- iOS JSON
- [HTML documentation](http://salesforce-ux.github.io/design-properties)

This first public release of the Design Properties reflects the current [Spring '15 release](http://www.salesforce.com/customer-resources/releases/spring15/). It will be updated with new releases while older ones will be branched off.

## Setup

### Dependencies

Please make sure to have [gulp.js](http://gulpjs.com/) installed globally:

    $ sudo npm install -g gulp

### Clone and Run

    $ git clone https://github.com/salesforce-ux/design-properties.git
    $ cd design-properties
    $ npm install .
    $ gulp

Please check the `./dist` directory for the output.

### NPM

The Design Properties are available via NPM:

    $ npm install design-properties

### Gulp

You can make the Design Properties part of your gulp.js build script:

    var gulp = require('gulp');
    var theo = require('theo');

    gulp.task('default', ['clean'], function(){
      var path = './node_modules/design-properties/variables/*.json'

      theo.convert(path, './dist', {
        templates: ['styl', 'html', 'less', 'scss', 'ios.json', 'android.xml'],
      });
    });

## License

Copyright (c) 2014, salesforce.com, inc. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
Neither the name of salesforce.com, inc. nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
