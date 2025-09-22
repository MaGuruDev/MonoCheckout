## Requirements
* Magento Community Edition 2.4.x

## Installing via composer
* Open command line
* Using command "cd" navigate to your magento2 root directory
* Run the commands:

```
composer require maguru/module-monocheckout
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```