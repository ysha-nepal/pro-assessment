### Environment

- **[Laravel v8](https://laravel.com/docs/8.x)**
- **[Composer v2](https://getcomposer.org/)**
- **[Mysql v8](https://www.mysql.com/)**
- **[Node v 16](https://nodejs.org/en/)**

### Installation Steps

- **Initialize Submodule** ```git submodule init```
- **Update Submodule** ```git submodule update```
- **Master Branch Submodule** ```git submodule foreach git checkout master```
- **Copy .env.example as .env**
- **Configure database**
- **Install composer dependencies** ```composer install``` *composer may fail*
- **Install composer again** ```composer install``` *To merge composer**
- **Generate Key** ```php artisan key:generate```
- **Run package migrate** ```php artisan package:migrate``` 
- **Generate Permission** ```php artisan generate:permission```
- **Generate Menus** ```php artisan generate:menu```
- **Generate Super User** ```php artisan generate:super-user```
- **Generate Setting** ```php artisan generate:setting```
- **Compile Core Packages** ```PACKAGE=core npm run compile```
- **Install Npm** ```npm install```
- **Generate Assets** ```npm run dev```
- **Server the Project** ```php artisan serve```


### Commands

- #### Generating Package
    First we need to create a new repository for the module.
    Then add the submodule to the current repo.
    ```git submodule add <GIT_URL> PATH```
    *For eg. ```git submodule add git@bitbucket.org:Sunil-YM/core.git packages/core```*
    Then run command ```php artisan generate:package PACKAGE_NAME``` *For eg. ```php artisan generate:package page```*.
    This will generate the necessary folders and files for the module
- #### Generating Model
    To generate a new model for package run ```php artisan generate:model MODEL_NAME PACKGAE_NAME```
    *for eg. ```php artisan generate:model Page page```
- #### Generating Migration
  To generate a new migration for package run ```package:migration {name} {package}```
  *for eg. ```php artisan package:migration pages page```
  This will created the migration file inside the package.


*Note:: In case of new package addition or changes in permission or menu. Please generate the permission and menu again.
In case of changes in settings. Please generate the settings again. All the routes file should be written separately for clean and minimal architecture.*  

***Warning : Do not change anything in the modules which you have not created. This may break other system*** 


