# Magento 2 OwlCarousel2 module

[![PHP version](https://badge.fury.io/ph/msp%2Fowlcarousel2.svg)](https://badge.fury.io/ph/msp%2Fowlcarousel2)

This module lets you use [OwlCarousel2](https://github.com/OwlCarousel2/OwlCarousel2) with Magento 2 through requirejs.

## Installation
```
composer require msp/owlcarousel2
bin/magento setup:upgrade
```
## Usage
### Initialization
You can init the slider with `data-mage-init`:
```
<div id="your-slider" class="owl-carousel" data-mage-init='{
    "OwlCarousel": {
      "autoPlay"          :   true,
      "autoplayTimeout"   :   1500,
      "loop"              :   true,
      "items"             :   1,
      "dots"              :   false
    }
}'>
    <img src="kitten1.jpg" />
    <img src="kitten2.jpg" />
    <img src="kitten3.jpg" />
    <img src="kitten4.jpg" />
</div>
```
or with a `<script type="text/x-magento-init">`:
```
<div id="your-slider" class="owl-carousel">
    <img src="kitten1.jpg" />
    <img src="kitten2.jpg" />
    <img src="kitten3.jpg" />
    <img src="kitten4.jpg" />
</div>
<script type="text/x-magento-init">
     {
         "#your-slider": {
             "OwlCarousel": {
                "autoplay"        : true,
                "autoPlayTimeout" : 1500,
                "loop"            : true,
                "items"           : 1,
                "dots"            : false
             }
         }
     }
 </script>
```
### OwlCarousel theme css
This module loads only the base css from OwlCarousel, but no theme.
The default theme is included, and you can add it to your theme layout ```default.xml``` (or whatever layout file) with:
```
...
    <head>
        ...
        <css src="Msp_OwlCarousel2::css/owl.theme.default.min.css" />
        ...
    </head>
...
```
