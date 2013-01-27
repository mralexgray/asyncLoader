# asyncLoader

### asyncLoader - simple asynchronous script and stylesheet loading with callback.


##### live examples:
[async.soluch.at](http://async.soluch.at/)
The live example page heavy utilizes Twitter Bootstrap & Font Awesome 3.0

##### usage:

The only script you need to load ( in head ) is asyncLoader.js :
```html
<script src="asyncLoader.js"></script>
```

Then load everything else you need & initialise via callback ( which is, by the way, optional ).
```javascript
asyncLoader(
    [
        'css/bootstrap.min.css',
        'css/bootstrap-responsive.min.css',
        'css/font-awesome.css',
        'http://yandex.st/highlightjs/7.3/styles/pojoaque.min.css',
        '//ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js',
        '//ajax.googleapis.com/ajax/libs/jqueryui/1.10.0/jquery-ui.min.js',
        'http://yandex.st/highlightjs/7.3/highlight.min.js'
    ],
    {
        'callback':function() {
            $('body').fadeIn( 800 );
            $('#test').delay(800).fadeIn();
            $('pre code').each(function(i, e) {hljs.highlightBlock(e)});
        }
    }
);
```
##### Copyright and License
asyncLoader is licensed under the terms of the MIT License, see the included MIT-LICENSE file.
