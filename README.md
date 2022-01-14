# Project - Skill Swap - Symfony 5.3

## Presentation

**  Skill Swap aims to be a platform for exchanging talents and skills without any funding. Its goal is to put two people in touch with each other, the first one needing a service and the second one being able to provide it.
Each one registers on the site, selects the skills he masters and makes himself available to help those already registered.
The one who needs help selects a skill and is immediately offered all the profiles of swappers who master it.
Once he's chosen a profile, a request for help is sent, and the target profile can accept or refuses it. . The requester is notified of the answer by email. If it's favorable, a swap (i.e. a discussion between two swappers can begin).
At the end, the applicant of the service puts an end to the discussion and can thus leave a comment to the person who made him service. This comment can be moderated by the owner of the profile on which it is left.

**  The site is developed in symfony 5.3 with some additional libraries (webpack, fixtures) and tools to validate the code standards.
GrumPHP, as a pre-commit hook, will launch 2 tools when git commit is launched:
PHP_CodeSniffer to check PSR12.
PHPStan focuses on finding errors in your code (without executing it).
PHPmd checks if you are following PHP best practices.
If the tests fail, the commit is cancelled and a warning message is displayed to the developer.

 
## Getting Started

### Prerequisites

1. Check composer is installed
2. Check yarn & node are installed
3. Check that the upload/avatars folder is in the public directory. If not, create this folder to store the photos of registered users.
4. Create an environment variable `MAILER_FROM_ADDRESS` with the address of the site administrator in the `.env` file.
5. Change the environment variable `DATABASE_URL` in the `.env` file.

### Install

1. Clone this project
2. Run `composer install`
3. Run `yarn install`
4. Run `yarn encore dev` to build assets
5. Run the command `symfony console d:m:m`
6. Run the command `symfony console d:f:l`

### Working

1. Run `symfony server:start` to launch your local php web server
2. Run `yarn run dev --watch` to launch your local server for assets

### Testing

1. Run `php ./vendor/bin/phpcs` to launch PHP code sniffer
2. Run `php ./vendor/bin/phpstan analyse src --level max` to launch PHPStan
3. Run `php ./vendor/bin/phpmd src text phpmd.xml` to launch PHP Mess Detector
3. Run `./node_modules/.bin/eslint assets/js` to launch ESLint JS linter
3. Run `../node_modules/.bin/sass-lint -c sass-linter.yml -v` to launch Sass-lint SASS/CSS linter

### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

## Deployment

Some files are used to manage automatic deployments (using tools as Caprover, Docker and Github Action). Please do not modify them.

* [captain-definition](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/captain-definition) Caprover entry point
* [Dockerfile](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/Dockerfile) Web app configuration for Docker container
* [docker-compose.yml](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-compose.yml) ...not use it's used 😅
* [docker-entry.sh](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-entry.sh) shell instruction to execute when docker image is built
* [nginx.conf](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/nginx.conf) Nginx server configuration
* [php.ini](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/php.ini) Php configuration


## Built With

* [Symfony](https://github.com/symfony/symfony)
* [GrumPHP](https://github.com/phpro/grumphp)
* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
* [PHPStan](https://github.com/phpstan/phpstan)
* [PHPMD](http://phpmd.org)
* [ESLint](https://eslint.org/)
* [Sass-Lint](https://github.com/sasstools/sass-lint)



## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning


## Authors

- Cécile Do Nascimento
- Benjamin Babilliot
- Olivier Gourdonneau
- Sébastien Violante
- Bruno Fernandes


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

