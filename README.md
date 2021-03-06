# jQuery File Upload for Rails

[jQuery-File-Plugin](https://github.com/blueimp/jQuery-File-Upload) is a file upload plugin written by [Sebastian Tschan](https://github.com/blueimp). jQuery File Upload features multiple file selection, drag&drop support, progress bars and preview images for jQuery. Supports cross-domain, chunked and resumable file uploads and client-side image resizing.

jquery-fileupload-rails is a library that integrates jQuery File Upload for Rails and is based on a version released at: https://github.com/boston-library/jquery-fileupload-rails.

This version of the plugin has support for clientside checksums.

## Installing Gem

    gem 'jquery-fileupload-rails', :git => 'https://github.com/boston-library/jquery-fileupload-rails.git'

## Using the javascripts

Require jquery-fileupload in your app/assets/application.js file.

    //= require jquery-fileupload

The snippet above will add the following js files to the mainfest file.

    //=require jquery-fileupload/vendor/jquery.ui.widget
    //=require jquery-fileupload/vendor/load-image
    //=require jquery-fileupload/vendor/canvas-to-blob
    //=require jquery-fileupload/vendor/tmpl
    //=require jquery-fileupload/jquery.iframe-transport
    //=require jquery-fileupload/jquery.fileupload
    //=require jquery-fileupload/jquery.fileupload-fp
    //=require jquery-fileupload/jquery.fileupload-ui
    //=require jquery-fileupload/locale

If you only need the basic files, just add the code below to your application.js file. [Basic setup guide](https://github.com/blueimp/jQuery-File-Upload/wiki/Basic-plugin)

    //=require jquery-fileupload/basic

The basic setup only includes the following files:

    //=require jquery-fileupload/vendor/jquery.ui.widget
    //=require jquery-fileupload/jquery.iframe-transport
    //=require jquery-fileupload/jquery.fileupload

## Using the stylesheet

Require the stylesheet file to app/assets/stylesheets/application.css

    *= require jquery.fileupload-ui

## Using the middleware

The `jquery.iframe-transport` fallback transport has some special caveats regarding the response data type, http status, and character encodings. `jquery-fileupload-rails` includes a middleware that handles these inconsistencies seamlessly. If you decide to use it, create an initializer that adds the middleware to your application's middleware stack.

    Rails.application.config.middleware.use JQuery::FileUpload::Rails::Middleware

## [Example app](https://github.com/boston-library/jquery-fileupload-rails-paperclip-example)
This app uses paperclip and twitter-bootstrap-rails

## Thanks
Thanks to [Sebastian Tschan](https://github.com/blueimp) for writing an awesome file upload plugin.

Thanks to [Tors Dalid](https://github.com/tors)for the base version of this plugin

Thanks to [Ben Ranker](https://github.com/branker) for making the md5 calculations streamable.

## License
Copyright (c) 2013 Boston Public Library

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
