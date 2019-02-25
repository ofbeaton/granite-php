# granite-php
Opinionated coding style enforcement for PHP.

## Contains
We make use of the following programs:
* [PHP-Parallel-Lint](https://github.com/JakubOnderka/PHP-Parallel-Lint)
* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

## Installing via Composer

The recommended way to install granite-php is through
[Composer](http://getcomposer.org). Ensure you have it installed first.

Next, run the Composer command to install the latest stable version:

```bash
composer require ofbeaton/granite-php
composer require squizlabs/php_codesniffer
composer require jakub-onderka/php-parallel-lint jakub-onderka/php-console-highlighter
```

Edit your `composer.json` and add or modify `scripts` section:

```json
{
  ...
  
  "scripts": {
    "check": [
      "parallel-lint . --exclude vendor",
      "phpcs -p --Standard=vendor/ofbeaton/granite-php/phpcs/granite"      
    ],
    "fix": [
      "phpcbf -p --Standard=vendor/ofbeaton/granite-php/phpcs/granite"
    ],
    "check-tests": [
      "parallel-lint . --exclude vendor",
      "phpcs -p --Standard=vendor/ofbeaton/granite-php/phpcs/granite-syntax"      
    ],
    "fix-tests": [
      "phpcbf -p --Standard=vendor/ofbeaton/granite-php/phpcs/granite-syntax"
    ],
    "test": [
      "@check",
      "@check-tests"
    ]
  },
  
  ...
}
```

And update your project:

```bash
composer update ofbeaton/granite-php
```

After updating, you can now run granite-php:

```bash
composer test
```

## Running granite-php on test suites

You usually want to relax some requirements for test suites, in that case run:

```bash
composer check-tests
```

## License

This software is distributed under the MIT License. Please see [License file](LICENSE) for more information.
