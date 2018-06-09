# push

## Introduction

Third party message push

## Install

```
$ composer require kacha886/push
```

## Demo

```php
<?php

require __DIR__ . '/vendor/autoload.php';

$appKey = 'your-app-key';
$masterSecret = 'your-master-secret';

$alert = 'Hi JPush!';
$extras = [
    'type' => 1,
    'url' => 'http://www.kacha886.com'
];
$platform = ['android', 'ios'];
$audience = [
    'alias' => ['13888888888']
];

$push = new kacha886\Push\JPush($appKey, $masterSecret);
$push->push($alert, $extras, $platform, $audience);
```