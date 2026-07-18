# array_undot

> [!WARNING]
> This package is retired and no longer maintained. Use [`jord-jd/array_undot`](https://packagist.org/packages/jord-jd/array_undot) instead. The maintained successor supports current PHP versions and preserves the `array_undot()` API.

![Packagist](https://img.shields.io/packagist/dt/rapidwebltd/array_undot.svg)

This package provides a helper function called `array_undot`, which expands a dot notation array into a full multi-dimensional array. 
It is, therefore, the opposite of the `array_dot` helper function provided by Laravel.

# Installation

To install, just run the following composer command.

```
composer require rapidwebltd/array_undot
```

The `array_undot` helper function will then be available globally in your project.

# Usage

The following basic examples show how to use the `array_undot` helper function.

```php
$dotNotationArray = ['products.desk.price' => 100];

$expanded = array_undot($dotNotationArray)

// ['products' => ['desk' => ['price' => 100]]];
```

```php
$dotNotationArray = ['products.desk.price' => 100, 
                     'products.desk.name' => 'Oak Desk',
                     'products.lamp.price' => 15,
                     'products.lamp.name' => 'Red Lamp'];

$expanded = array_undot($dotNotationArray)

/*
[
    'products' => [
        'desk' => [
            'price' => 100,
            'name' => 'Oak Desk'
        ],
        'lamp' => [
            'price' => 15,
            'name' => 'Red Lamp'
        ]
    ]
]
*/

```
