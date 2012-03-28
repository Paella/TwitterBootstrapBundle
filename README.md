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

Add the assets in you template (available version 1.4.0, 2.0.0, 2.0.2) :

```html+jinja
{% block stylesheets %}
<link rel="stylesheet" media="all" href="{{ asset('bundles/paellatwitterbootstrap/[VERSION]/css/bootstrap.[min.]css') }}">
<link rel="stylesheet" media="all" href="{{ asset('bundles/paellatwitterbootstrap/[VERSION]/css/bootstrap-responsive.[min.]css') }}">
{% endblock %}

{% block javascripts %}
<script src="{{ asset('bundles/paellatwitterbootstrap/js/jquery-1.7.min.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/jquery-ui-1.8.16.custom.min.js') }}"></script>

<script src="{{ asset('bundles/paellatwitterbootstrap/js/[VERSION]/bootstrap[*].js') }}"></script>

<script src="{{ asset('bundles/wilogmaintenance/js/jquery.treeview.js') }}"></script>
<script src="{{ asset('bundles/paellatwitterbootstrap/js/jquery.tablesorter.min.js') }}"></script>
{% endblock %}
```