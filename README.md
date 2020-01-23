### Symfony 5 BoilerPlate ETH

Basic Symfony 5 application setup with [EasyAdminBundle](https://github.com/EasyCorp/EasyAdminBundle), additional [EasyAdminExtensionBundle](https://github.com/alterphp/EasyAdminExtensionBundle) and members management (Login, Register, Lost Password, ...).

#### Setup

1 - Clone, run `composer install` and `composer update "symfony/*" --with-all-dependencies` "for update".
2 - Edit .env for database connexion
3 - `php bin/console do:sc:cr` or `php bin/console doctrine:schema:create` for database creation.
4 - `php bin/console do:fi:lo -n` or `php bin/console doctrine:fixtures:load -n` for some fixtures.
5 - Run project with `php -S 127.0.0.1:8888 -t public -d display_errors=1`.

#### Users

[Doctrine Single table inheritance](https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/inheritance-mapping.html#single-table-inheritance) is used to manage user types. There are two predefined types/entities, `Admin` and `Editor`

#### Easy Admin Config

Configuration YAML files are located under `config/packages/easyadmin` folder, and automatically loaded in main config. Add additional YAML files in this folder, for your new entities etc.

#### Useful
