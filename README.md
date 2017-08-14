
# Laravel Paperclip: File Attachment Solution

Allows you to attach files to Eloquent models.

This is a re-take on [CodeSleeve's Stapler](https://github.com/CodeSleeve/stapler). It is mainly intended to be more reusable and easier to adapt to different Laravel versions. Despite the name, this should not be considered a match for Ruby's Paperclip gem.

Instead of tackling file storage itself, it uses Laravel's internal storage drivers and configuration.

This uses [czim/file-handling](https://github.com/czim/file-handling) under the hood, and any of its (and your custom written) variant manipulations may be used with this package.


## Installation

Via Composer:

``` bash
$ composer require czim/laravel-paperclip
```

Add the service provider to the `app.php` config file:

``` php
Czim\Paperclip\PaperclipServiceProvider::class,
```

Publish the configuration file:

``` bash
php artisan vendor:publish
```


## Usage

### Attachment Configuration

To Do:
- How to set up attachments on Eloquent models
- Brief comparison with Stapler

### Variant Configuration

For the most part, the configuration of variants ('styles') is nearly identical to Stapler, so it should be easy to make the transition either way. 

[Get more information on configuration here](CONFIG.md).

#### Custom Variants

The file handler comes with a few common variant strategies, including resizing images and taking screenshots from videos.
It is easy, however, to add your own custom strategies to manipulate files in any way required.

Variant processing is handled by [the file-handler package](https://github.com/czim/file-handling).
Check out its source to get started writing custom variant strategies.

### Storage configuration

To do: 
- Laravel storage configuration,
- Public path recommendation?

 

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.


## Credits

- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/czim/laravel-paperclip.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/czim/laravel-paperclip.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/czim/laravel-paperclip
[link-downloads]: https://packagist.org/packages/czim/laravel-paperclip
[link-author]: https://github.com/czim
[link-contributors]: ../../contributors
