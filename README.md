
# Instagram-API - based on mgp25/instagram-php

  
## How to make it work for Laravel

The dependency symfony-process conflicts with Laravel's symfony-process.
Thus, need to skip installing that. However, sometimes composer is stuck on resolving these dependencies.
So, the correct way that I identified to make this all work is to install the dependencies seprately on your app.

Please consider following composer.json. Note : `repositories`
```
"repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/ammarbrohi/instagram-php.git"
        }
    ],
    "require": {

        "ammarbrohi/instagram-api": "dev-laravel",
        
        // ------------ LOADING DEPENDENCIES INDIVIDUALLY --------
        
        "lazyjsonmapper/lazyjsonmapper": "^1.6.1",
        "ext-curl": "*",
        "ext-mbstring": "*",
        "ext-gd": "*",
        "ext-exif": "*",
        "ext-zlib": "*",
        "ext-bcmath": "*",
        "react/event-loop": "^0.4.3",
        "react/promise": "^2.5",
        "react/socket": "^0.8",
        "binsoul/net-mqtt-client-react": "^0.3.2",
        "clue/socks-react": "^0.8.2",
        "clue/http-proxy-react": "^1.1.0",
        "psr/log": "^1.0",
        "valga/fbns-react": "^0.1.8",
        "winbox/args": "1.0.0"
    },
```
## Run
`composer update` to install these dependencies