curl-ember-handlebars [![Build Status](https://travis-ci.org/jsedlacek/curl-ember-handlebars.png)](https://travis-ci.org/jsedlacek/curl-ember-handlebars)
=========

Ember Handlebars plugin for curl.js

Usage
-----

This plugin allows to loading handlebars templates using AMD syntax.

```
define(['ehbs!application'], function() {
    // Now we have application.hbs loaded and registered as application template in Ember.TEMPLATES
});
```

Installation and Setup
----------------------
Download curl-ember-handlebars using bower.
```
bower install curl-ember-handlebars --save
```

To allow `ehbs!` usage add the following snippet to your curl.config.
```
"packages": {
    "ehbs": {
        "location": "bower_components/curl-ember-handlebars/src",
        "main": "ehbs.js"
    }
}
```

Also make sure you have correctly set up locations of ember, handlebars and jquery.
```
"packages": {
    "ember": {
        "location": "bower_components/ember",
        "main": "ember.js",
        "config": {
            "exports": "Ember",
            "loader": "curl/loader/legacy",
            "requires": ["jquery", "handlebars"]
        }
    },
    "handlebars": {
        "location": "bower_components/handlebars",
        "main": "handlebars.js",
        "config": {
            "dontWrapLegacy": true,
            "exports": "Handlebars",
            "loader": "curl/loader/legacy"
        }
    }
},
"paths": {
    "jquery": "bower_components/jquery/jquery.js"
}
```
