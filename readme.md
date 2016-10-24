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

@todo

Menggunakan Api Kirim Transaksi Tunggal
------------

@todo

Menggunakan Api Kirim Transaksi Dalam Jumlah Banyak
------------

@todo

TODO
------------

- English documentation.

License
------------

The MIT License (MIT). Please see [LICENSE](LICENSE) for more information.