# granite
Strict PHP Coding Style enforced by [CodeSniffer 2.x](https://github.com/squizlabs/PHP_CodeSniffer). Can also process javascript and css files if configured.

## Installing via Composer

The recommended way to install Granite is through
[Composer](http://getcomposer.org).

```bash
# Install Composer
curl -sS https://getcomposer.org/installer | php
```

Next, run the Composer command to install the latest stable version:

```bash
composer.phar require ofbeaton/granite
```

Edit your composer .json and add a config section:

```json
{
  ...
  
  "config": {
    "bin-dir": "bin"
  },
  
  ...
}
```

And update your project:

```bash
composer.phar update ofbeaton/granite
```

After installing, you can now run PHP_CodeSniffer:

```bash
bin/phpcs --Standard=vendor/granite/Granite
```

## Support Me

Hi, I'm Finlay Beaton ([@ofbeaton](https://github.com/ofbeaton)). This software is made possible by donations of fellow users like you, encouraging me to toil the midnight hours away and sweat into the code and documentation. 

Everyone's time should be valuable, please consider donating.

[Donate through Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=RDWQCGL5UD6DS&lc=CA&item_name=ofbeaton&item_number=granite&currency_code=CAD&bn=PP%2dDonationsBF%3abtn_donate_LG%2egif%3aNonHosted)

## License

This software is distributed under the MIT License. Please see [License file](LICENSE) for more information.
