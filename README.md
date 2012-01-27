TwitterBootsrapBundle
=====================


This bundle provides the assets from the twitter bootstrap and the twig theme for forms using the twitter bootstrap.


## Installation

Include this repository in your `app/deps` file:

``` php

[PaellaTwitterBootstrapBundle]
    git=http://github.com/Paella/TwitterBootstrapBundle.git
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
## Usage

Publish the assets of your application : 

``` php app/console assets:install ```

Add the assets in you template:

```html+jinja
{% block stylesheets %}
<link rel="stylesheet" href="{{ asset('bundles/paellatwitterbootstrap/css/bootstrap-1.4.0.min.css') }}" type="text/css" media="all" >
{% endblock %}

{% block javascripts %}
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-modal.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-alerts.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-twipsy.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-popover.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-dropdown.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-scrollspy.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-tabs.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/bootstrap-buttons.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/jquery.tablesorter.min.js') }}"></script>
{% endblock %}
```

