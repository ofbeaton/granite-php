# granite
Strict PHP Coding Style enforced by [CodeSniffer 3.x](https://github.com/squizlabs/PHP_CodeSniffer). Can also process javascript and css files if configured.

## Installing via Composer

The recommended way to install Granite is through
[Composer](http://getcomposer.org). Ensure you have it installed first.

Next, run the Composer command to install the latest stable version:

```bash
composer require ofbeaton/granite
```

Edit your `composer.json` and add a `config` section:

```json
{
  ...
  
  "config": {
    "bin-dir": "vbin"
  },
  
  ...
}
```

And update your project:

```bash
composer update ofbeaton/granite
```

After updating, you can now run PHP_CodeSniffer:

```bash
vbin/phpcs --Standard=vendor/granite/Granite
```

## License

This software is distributed under the MIT License. Please see [License file](LICENSE) for more information.
