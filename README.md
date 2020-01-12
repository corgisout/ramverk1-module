Anax weather-module
==================================

Install and setup Anax
------------------------------------

You need a Anax installation to use this module. You can create an Anax installation
using the [`anax-cli`] that  an be found at (https://github.com/canax/anax-cli).

create an Anax installation `anax-site-develop` into the directory `test/` with bash.

```
anax create test ramverk1-me-v2
cd test
```

you can now test it by pointing your webserver to `test/htdocs` this should bring you to an anax frontpage

Install the weather module via composer
------------------------------------

1.  Install using composer.

```bash
composer require sihd17/weather
```

2.  rsync files.

```bash
rsync -av vendor/sihd17/weather/config/ ./config/
rsync -av vendor/sihd17/weather/src/ ./src/
rsync -av vendor/sihd17/weather/view/ ./view/
rsync -av vendor/sihd17/weather/test/ ./test/

```

3.  create config/apiKey.php to contain api keys


```text
<?php

return ["ipstack" => "xxx",
"darksky" => "xxx",
"locationiq" => "xxx"
];
