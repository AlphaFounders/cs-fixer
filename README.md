# PHP Coding standard fixer

This package is based on https://github.com/FriendsOfPHP/PHP-CS-Fixer with addition of git pre-commit hook installation.

The hook will prevent the commit if the code does not comply with the coding standard rules

Default set of rules that are fully extendable

## Installation

#### Require a package
```
composer require --dev rabbitinternet/cs-fixer
```

#### Add composer commands
```
"scripts": {
    "post-install-cmd": [
        "composer run-script post-install-cmd -d ./vendor/rabbitinternet/cs-fixer"
    ]
}
```

#### Install the git hook
```
composer run-script post-install-cmd
```

## Manual Usage

```
vendor/bin/cs-fixer help
```

**Note: Composer can install the binaries in custom dir instead of vendor/bin/ (sylius installs in bin/)**


## Rules configuration

To override default rules add `.php_cs_rules.php` file in the root of the project

```
<?php

return [
    // override rules
    'single_blank_line_at_eof' => true
];

```
