## Вимоги
* Magento Community Edition 2.4.x

## Встановлення через composer
* Відкрийте командний рядок
* За допомогою команди "cd" перейдіть до кореневої директорії вашої magento2
* Виконайте команди:

```
composer require maguru/module-monocheckout
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```