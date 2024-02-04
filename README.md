# Laravel DB refresh

This package contains Trait to refresh and seed database before running test scope.

## Installing

1. `composer require --dev ezitisitis/laravel-refresh-database-once`

Add use to `TestCase` class. Congratulations, you are done.

Example:
```php
<?php

namespace Tests;

use EzitisItIs\LaravelRefreshDatabaseOnce\MigrateFreshSeedOnce
use Illuminate\Foundation\Testing\TestCase as BaseTestCase;

abstract class TestCase extends BaseTestCase
{
    use CreatesApplication;
    use MigrateFreshSeedOnce;
}
```
