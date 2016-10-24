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

If you want to use Garoon API, please send Pull Request.

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

You can add Cybozu HTTP as a dependency using the composer

```{.bash}
    $ composer require ochi51/cybozu-http
```

Alternatively, you can specify Cybozu HTTP as a dependency in your project's existing composer.json file:

```{.json}
    {
       "require": {
          "ochi51/cybozu-http": "0.1.*@dev"
       }
    }
```

After installing, you need to require Composer's autoloader:

```{.php}
    require 'vendor/autoload.php';
```

Quick start
------------

```{.php}
    $api = new \CybozuHttp\Api\KintoneApi(\CybozuHttp\Client::factory([
        'domain' => 'cybozu.com'
        'subdomain' => 'your-subdomain'
        'login' => 'your-login-name'
        'password' => 'your-password'
    ]));
    
    // get record that kintone app id is 100 and record id is 1.
    $record = $api->record()->get(100, 1);
```

Usage
------------

@todo

Testing
------------

To run the tests, you need to following process.

- Prepare your kintone account.
    - Free trial is [here](https://www.cybozu.com/jp/service/com/trial/?fcode=F00000081)
- Create kintone space template. (Enable multiple thread)
- Create graph.
- Edit `parameters.yml`.

Run the following command from the project folder.

```{.bash}
    $ php ./bin/phpunit
```

TODO
------------

- Japanese documentation.

License
------------

The MIT License (MIT). Please see [LICENSE](LICENSE) for more information.