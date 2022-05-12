# ServiceProvider

## Пакет, который нужен для дебага egal моделей

### Для использования пакета, создайте файл config/debug.php и заполните его нижеприведенными данными:

```php
<?php

return [

    "include" => (bool)env("DEBUG_MODE", true),
    "debugDir" => env("DEBUG_PATH", 'app/DebugModels/'),

];
```

### и в bootstrap/app добавьте:

```php
$app->configure('debug');
$app->register(killyouare\ServiceProvider\ServiceProvider::class);
```
