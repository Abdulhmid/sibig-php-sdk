SI BIG SDK PARKING
==================

Usage : 

//declaration
use SibigParking\Parking;
```

```php
$siparking = new Parking(array(
  'id'  => 'Machine ID',
  'secret' => 'Machine Secret',
));

//retrieve locations
$locations = $siparking->getLocations('json');
```
   - [api documentation](http://192.168.2.2:81/redmine/projects/sibig/wiki/API#Daftar-Lokasi)

```php    
//send single transaction
$parking->singleTrans($operatorId, $operatorSecret, $fields);
```
   - [api documentation](http://192.168.2.2:81/redmine/projects/sibig/wiki/API#Single-Transaksi) for fields parameter

```php
//send many transaction
$parking->multiTrans($operatorId, $operatorSecret, $transactions);
```
 - [api documentation](http://192.168.2.2:81/redmine/projects/sibig/wiki/API#Multi-Transaksi) for transactions parameter

## Help and docs

- [Documentation](http://192.168.2.2:81/redmine/projects/sibig/wiki/API)

## Installing

```bash
composer require sdksibig/sibigparking:v0.1
```

## Updating Repository
```bash
curl -XPOST -H'content-type:application/json' 'https://packagist.org/api/update-package?username=Abdulhmid&apiToken=J3CPYd5EIS52A7Oay6cP' -d'{"repository":{"url":"https://github.com/Abdulhmid/sibig-php-sdk.git"}}'
```

