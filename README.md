# laravel-smartystreets

[![Author](http://img.shields.io/badge/author-@mhetreramesh-blue.svg?style=flat-square)](https://twitter.com/mhetreramesh)
[![Latest Version on Packagist](https://img.shields.io/packagist/v/gliterd/laravel-smartystreets.svg?style=flat-square)](https://packagist.org/packages/gliterd/laravel-smartystreets)
[![Software License][ico-license]](LICENSE.md)
[![Build Status](https://img.shields.io/travis/gliterd/laravel-smartystreets/master.svg?style=flat-square)](https://travis-ci.org/gliterd/laravel-smartystreets)
[![Coverage Status][ico-scrutinizer]][link-scrutinizer]
[![Quality Score][ico-code-quality]][link-code-quality]
[![Total Downloads](https://img.shields.io/packagist/dt/gliterd/laravel-smartystreets.svg?style=flat-square)](https://packagist.org/packages/gliterd/laravel-smartystreets)

Visit (https://secure.backblaze.com/b2_buckets.htm) and get your account id, application key.

The Laravel Backblaze B2 Storage Service Provider give provision for for laravel storage to use blackblaze as their storage system. It uses the [Backblaze B2 SDK](https://github.com/gliterd/backblaze-b2) & [Flysystem Adapter](https://github.com/gliterd/flysystem-backblaze) to communicate with the Backblaze b2 API.

## Install

Via Composer

``` bash
composer require gliterd/laravel-smartystreets
```
In your app.php config file add to the list of service providers:

``` php
\Gliterd\SmartyStreets\SmartyStreetsServiceProvider::class,
```
Add the following to your .env file:

```
AUTH_ID=xxxxxxx
AUTH_TOKEN=xxxxxxx
```

## Usage

Just use it as you normally would use the Storage facade.

``` php
    public function yourHandsomeFunction(Request $request, SmartyStreets $smartyStreets)
    {
        return $smartyStreets->getInspectedLocation([
            'street'        => $request->street,
            'street_number' => $request->street_number,
            'place'         => $request->place,
            'postal_code'   => $request->postcode,
        ]);
    }
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email mhetreramesh@gmail.com instead of using the issue tracker.

## Credits

- [Ramesh Mhetre][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/gliterd/laravel-smartystreets.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/gliterd/laravel-smartystreets/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/gliterd/laravel-smartystreets.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/gliterd/laravel-smartystreets.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/gliterd/laravel-smartystreets.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/gliterd/laravel-smartystreets
[link-travis]: https://travis-ci.org/gliterd/laravel-smartystreets
[link-scrutinizer]: https://scrutinizer-ci.com/g/gliterd/laravel-smartystreets/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/gliterd/laravel-smartystreets
[link-downloads]: https://packagist.org/packages/gliterd/laravel-smartystreets
[link-author]: https://github.com/mhetreramesh
[link-contributors]: ../../contributors
