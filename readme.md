SI BIG SDK PARKING
==================

```bash
composer require sdksibig/sibigparking:v0.1
```

Usage : 

```php    
//Declaration
use SibigParking\Parking;
```

```php    
// Using Constructor
$siparking = new Parking(array(
  'id'  => 'Machine ID',
  'secret' => 'Machine Secret',
));
```
```php    
// Lokasi
$parking->getLocations($format);
```
   - [api documentation](http://doc-sandbox.sibigparking.com/#lokasi)

```php    
//send single transaction
$parking->singleTrans($location, $vehicle, $payment,$enter, $exit,$plate_number, $amount, $format);
```
   - [api documentation](http://doc-sandbox.sibigparking.com/#transaksi-tunggal) for fields parameter

```php
//send many transaction
// transactions : Array JSON
$parking->multiTrans($transactions, $format);
```
 - [api documentation](http://doc-sandbox.sibigparking.com/#transaksi-jumlah-besar) for transactions parameter

## Help and docs

- [Documentation](http://doc-sandbox.sibigparking.com/)

## Installing


## Updating Repository
```bash
curl -XPOST -H'content-type:application/json' 'https://packagist.org/api/update-package?username=Abdulhmid&apiToken=J3CPYd5EIS52A7Oay6cP' -d'{"repository":{"url":"https://github.com/Abdulhmid/sibig-php-sdk.git"}}'
```

