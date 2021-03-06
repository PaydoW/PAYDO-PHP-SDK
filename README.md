# Paydo PHP-SDK
Php sdk for [Paydo](https://paydo.com) 

### Payment integration using Paydo Api

```php
<?php
header('Content-Type: text/html; charset=UTF-8');

// Paydo data
$publicKey = '';
$secretKey = '';

// Order params
$params['amount'] = 1;
$params['currency'] = 'RUB';
$params['orderId'] = 1;
$params['paymentType'] = 'app';
$params['payment'] = 'ALL';

require_once('../Paydo.php');

$paydo = new Paydo($publicKey,$secretKey);
$response = $paydo->api('initPayment', $params);

if(!empty($response->result->payUrl)){
    header("Location: " . $response->result->payUrl);
}
```

### Direct download

Download [last version ](https://github.com/Paydo/PAYDO-PHP-SDK/archive/master.zip) , unzip and copy to your project folder.

## Contributing ##

Please feel free to contribute to this project! Pull requests and feature requests welcome!
