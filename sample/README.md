## Neomerx JSON API sample application

### Install

Via Composer

```
$ composer install
```

### Run sample

```
$ php sample.php
```

The application will output a few encoding results for

* a resource with no relationships
* a resource with included relationships
* sparse and field set filters usage sample
* top level links and meta information usage sample

For more details see [the app source code](sample.php)

## Performance test

This application includes performance test as well. It can be run with default parameters

```
$ php sample.php -t
```

or with execution time measurement and specified number of iterations

```
$ time php sample.php -t=10000
```

If your system has debug assertions enabled it is recommended to turn them off. Just to give you an idea that debug assert are not free here is the execution time comparison

|Debug asserts mode   |Command                                           |Execution time|
|---------------------|--------------------------------------------------|--------------|
|Enabled              |```$ php -d assert.active=1 sample.php -t=10000```|7.589s        |
|Disabled             |```$ php -d assert.active=0 sample.php -t=10000```|2.884s        |
