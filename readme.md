SDK SI BIG PARKING
=======================

sibigparking.com API Documentation
------------

[API Doc](https://doc.sibigparking.com/)

Available API
------------

- API Daftar Lokasi
- API Kirim Transaksi Tunggal
- API Kirim Transaksi Dalam Jumlah Banyak

Requirements
------------

- PHP >=5.5
- Composer

Installation
------------

The recommended way to install Cybozu HTTP is with [Composer](https://getcomposer.org/).
Composer is a dependency management tool for PHP that allows you to declare the dependencies your project needs and installs them into your project.

```{.bash}
    $ curl -sS https://getcomposer.org/installer | php
    $ mv composer.phar /usr/local/bin/composer
```

You can add SDK Sibig Parking as a dependency using the composer

```{.bash}
    $ composer require sdksibig/sibigparking:v0.1
```

Alternatively, you can specify SDK Sibig Parking as a dependency in your project's existing composer.json file:

```{.json}
    {
       "require": {
          "sdksibig/sibigparking": "v0.1"
       }
    }
```

After installing, you need to require Composer's autoloader:

```{.php}
    require_once __DIR__ . '/../vendor/autoload.php'; 
```

Quick start
------------

```{.php}
    $siparking = new Parking(array(
      'id'  => 'Machine ID',
      'secret' => 'Machine Secret',
      'url' => 'url',
      'version' => 'v1',
    ));
    
```

Menggunakan Api Daftar Lokasi
------------
- format :
    ```
       JSON => "json" / XML => "xml"
    ```
- contoh : 
    ```
       $parking->getLocations("json")
    ```
- Response
```{.json}
    {
       "locations": [
         {
           "location_id": "4d565e1a-bcff-4ae4-92d9-2a23cff67e27",
           "name": "Mall Bekasi Sumarecon",
           "address": "Jalan Boulevard Ahmad Yani Blok M",
           "city": "BEKASI" 
         }
       ],
      "count": 1
    }
```

Menggunakan Api Kirim Transaksi Tunggal
------------

- Response
```{.json}
    {
        "message": "Successfully add transaction."
    }
```

Menggunakan Api Kirim Transaksi Dalam Jumlah Banyak
------------

- Response
```{.json}
    {
        "message": "Successfully add transactions.",
        "sent": 2,
        "succeed": 1,
        "failed": 1
    }
```

TODO
------------

- English documentation.

License
------------

The MIT License (MIT). Please see [LICENSE](LICENSE) for more information.