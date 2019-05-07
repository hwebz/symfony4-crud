sudo apt-get install php-xml
sudo apt-get install php-mysql

composer create-project symfony\skeleton symphart.test
composer require annotations
composer require twig
composer require doctrine maker

php bin/console doctrine:database:create
php bin/console make:entity Article

php bin/console doctrine:migrations:diff
php bin/console doctrine:migrations:migrate

php bin/console doctrine:query:sql 'SELECT * FROM article'

composer require form