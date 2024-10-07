# Laravel DB refresh

This package contains Trait to refresh and seed database before running test scope.

## Why do you need that

When you work in local environment. It sometimes appears that you want to run tests agains clean database (for example you have record count somewhere in tests).
Running each test on clear database is bad idea in general, because:

1. You check only that your code works only when there is no records;
2. **It is insanely time consuming**;

## Installing

1. `composer require --dev ezitisitis/laravel-refresh-database-once`;
2. Add `MigrateFreshSeedOnce` use to `TestCase` class;
3. Congratulations, you are done.

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

## Credits

- [Marks Bogdanovs](https://www.ezitisitis.com)
