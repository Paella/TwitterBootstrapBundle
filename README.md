TwitterBootsrapBundle
=====================


This bundle provides the assets from the twitter bootstrap and the twig theme for forms using the twitter bootstrap.


## Installation

Include this repository in your deps file:

``` php

[PaellaTwitterBootstrapBundle]
    git=http://github.com/guilleferrer/PaellaTwitterBootstrapBundle.git
    target=/bundles/Paella/Bundle/TwitterBootstrapBundle
```
Register the Namespace in the `app/autoload.php` file : 


``` php
$loader->registerNamespaces(array(
    'Paella'        => __DIR__.'/../vendor/bundles',
));
```

Register the bundle in `app/AppKernel.php`
``` php

    public function registerBundles() {
        $bundles = array(
            new Paella\Bundle\TwitterBootstrapBundle\PaellaTwitterBootstrapBundle(),
        );
```


