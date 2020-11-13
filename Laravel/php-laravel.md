**PHP-LARAVEL STRUCTURE**
```php
// dd for debugger
{{dd($panier)}}

// Array
$panier = ["dfez", "sdz"]

// Object
$panier = (object) ["keyname1" => "sdz", "keyname2" => "aze"]

// foreach loop version laravel
@foreach($panier as $element)
	{{$element}}
@endforeach

// for loop version laravel
@for($i = 0; $i < 3; $i++)
	{{$i}}
@endfor

// HELPERS
view()    = view folder
compact() = in view() method, send $var to html view
env()     = .env folder
asset()   = public folder

$loop is a var that can be called in any loop

@section('my content') = select the content to be field in the appropriate yield
@yield('my content')   = placeholder for the appropriate section
@extends("my view")	   = étends à partir de tout en haut
@include("my view")	   = inclus là où est le "@include"
```
**ROUTE**
```php
// view/pages/home.blade.php
Route::get('/', function () {
	return  view('pages.home');
});
// Name the route
Route::get('/', function () {
	return  view('pages.home');
})->name('myRoute');
```


**CONTROLLER**
```php
// TO CREATE A CONTROLLER
php artisan make:controller ViewnameController

// IN CONTROLLER CLASS
public function index(){
	return view('viewname');
}

// IN ROUTE
use App\Http\Controllers\ViewnameController
route::get("/", [ViewnameController::class, "index"]);

// Controller w/ all function needed (r for ressource)
php artisan make:controller ViewnameController -r

```

**MODELS**
```php
// With dbName capital letter
// "-c" make a controller with it
php artisan make:model <tableName> -c
// "-cms" make a controller, a seeder and a model
php artisan make:model <tableName> -cms
// "-cms" make a controller, a seeder and a model
php artisan make:model <tableName> -cmsr
// then in route
use App\Models\<modelName>;
// in model 
$var = <modelName>::all('*');
```
**MIGRATION**
```php
// migrate files to ur db
php artisan migrate
// reload all migrations files (to update files)
php artisan migrate:fresh
// Create migration file (create first & table last)
php artisan make:migration create_<tableName>_table
```
**CRUD**
```php
INDEX
CREATE
STORE
SHOW
EDIT
UPDATE
DESTROY
```

**CONTROLLER CRUD**
```php
public  function  index()
{
return  view("pages.home");
}
public  function  create()
{
return  view("pages.home");
}
public  function  store()
{
return  view("pages.home");
}
public  function  show()
{
return  view("pages.home");
}
public  function  edit()
{
return  view("pages.home");
}
public  function  update()
{
return  view("pages.home");
}
public  function  destroy()
{
return  view("pages.home");
}
```

**SEEDER**
```php
php artisan make:seeder <tableName>Seeder
// databaseSeeder.php call every seeder files
<tableName>Seeder::class
// then in console
php artisan migrate:fresh --seed
```
**NEEDED FILES IN A LARAVEL PROJECT (membre table exemple)**
```php
Membre.php -- MODEL
MembreController.php -- CONTROLLER
create_membres_table.php -- MIGRATION
MembreSeeder.php -- SEEDER
```


https://cdn.discordapp.com/attachments/724551677939679233/772738294680256542/Capture_decran_du_2020-11-02_09-25-12.png

https://cdn.discordapp.com/attachments/724552181138587739/775276627016941578/Capture_decran_du_2020-11-09_09-31-12.png
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMTQ5MDY0NzAsLTMyNzA0ODkxMywzNz
k5OTc0MTQsMTcyNzI3NzU1LDc3MDM3NjUyMCwxOTU4MDQ2NTcw
LC0yOTQ5Njg3OTEsNDA4NzE1MjYzXX0=
-->