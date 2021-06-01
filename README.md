Symfony SMS Command Sample
==========================

A sample application to demonstrate sending of an SMS reminder using Twilio's SDK.


>composer create-project symfony/framework-standard-edition Appointments
>$ php bin/console server:run

- add entity user and appointement

>$ php bin/console doctrine:schema:update --force   // to creat table in database


install bundle
>$ composer require --dev doctrine/doctrine-fixtures-bundle


To load our fixtures into the database
>$ php bin/console doctrine:fixtures:load

install twilio
>$ composer require twilio//sdk

execute the command
>$ php bin/console myapp:sms

creat conjob:

crontab -e

>0 0 * * * php ~~/www/Appointments/bin/console myapp::sms --env=prod
