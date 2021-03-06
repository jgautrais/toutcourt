# Tout court - Symfony 5.\*

## Project

Tout court was built during a 3-days final exam at Wild Code School. It reproduces as simple tennis court booking system.
In order to reduce complexity, it was assumed for this project that all court are open 7 days per week, from 9am to 23pm. Each booking slot is 1 hour long.
The project is built with Symfony 5. Data is handled with mySQL DB and the application is styled using Tailwind CSS framework.

## Presentation

This starter kit is here to easily start a repository for Wild Code School students.

It's symfony website-skeleton project with some additional library (webpack, fixtures) and tools to validate code standards.

-   GrumPHP, as pre-commit hook, will run 2 tools when `git commit` is run :

    -   PHP_CodeSniffer to check PSR12
    -   PHPStan focuses on finding errors in your code (without actually running it)
    -   PHPmd will check if you follow PHP best practices

    If tests fail, the commit is canceled and a warning message is displayed to developper.

-   Github Action as Continuous Integration will be run when a branch with active pull request is updated on github. It will run :

    -   Tasks to check if vendor, .idea, env.local are not versionned,
    -   PHP_CodeSniffer, PHPStan and PHPmd with same configuration as GrumPHP.

## Getting Started for Students

### Prerequisites

1. Check composer is installed
2. Check yarn & node are installed

### Install

1. Clone this project
2. Run `composer install`
3. Run `yarn install`
4. Run `yarn encore dev` to build assets
5. Run `php bin/console d:d:c` to create DB (configure `DATABASE_URL` in your .env.local, set db_name to **toutcourt**)
6. Run `php bin/console d:m:m` to execute migrations
7. Run `php bin/console d:f:l` to load fixtures
8. Configure your `MAILER_DSN` and `MAILER_FROM_ADDRESS` in your .env.local (Mailtrap was used for development)

### Working

1. Run `symfony server:start` to launch your local php web server
2. Run `yarn run dev --watch` to launch your local server for assets

### Testing

1. Run `php ./vendor/bin/phpcs` to launch PHP code sniffer
2. Run `php ./vendor/bin/phpstan analyse src --level max` to launch PHPStan
3. Run `php ./vendor/bin/phpmd src text phpmd.xml` to launch PHP Mess Detector
4. Run `./node_modules/.bin/eslint assets/js` to launch ESLint JS linter
5. Run `../node_modules/.bin/sass-lint -c sass-linter.yml -v` to launch Sass-lint SASS/CSS linter

### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

## Built With

-   [Symfony](https://github.com/symfony/symfony)
-   [GrumPHP](https://github.com/phpro/grumphp)
-   [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
-   [PHPStan](https://github.com/phpstan/phpstan)
-   [PHPMD](http://phpmd.org)
-   [ESLint](https://eslint.org/)
-   [Sass-Lint](https://github.com/sasstools/sass-lint)

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

## Authors

Wild Code School trainers team

## License

MIT License

Copyright (c) 2019 aurelien@wildcodeschool.fr

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Acknowledgments
