# Phospr Fraction

Composer-installable fractions for PHP [![Build Status](https://travis-ci.org/phospr/fraction.svg)](https://travis-ci.org/phospr/fraction)

## Usage

```php
use Phospr\Fraction;
```

#### Simple Fractions

```php
$fraction = new Fraction(1, 2);
echo $fraction; // 1/2

echo new Fraction(5, 2); // 2 1/2
```

#### Auto-simplified

Fractions are simplified at construction

```php
echo new Fraction(4, 6); // 2/3
```

#### Addition

```php
$fraction = new Fraction(2, 7);
echo $fraction->add(new Fraction(3, 11)); // 43/77
```

#### Subtraction

```php
$fraction = new Fraction(6);
echo $fraction->subtract(new Fraction(2, 3)); // 5 1/3
```

#### Multiplication

```php
$fraction = new Fraction(1, 2);
echo $fraction->multiply(new Fraction(1, 2)); // 1/4
```

#### Division

```php
$fraction = new Fraction(6, 13);
echo $fraction->divide(new Fraction(2, 7)); // 1 8/13
```

#### To Float

```php
$fraction = new Fraction(1, 8);
$fraction->toFloat(); // 0.125
```

#### Is Integer?

Check whether a fraction is in fact a whole number.

```php
$fraction = new Fraction(1, 8);
$fraction->isInteger(); // false

$fraction = new Fraction(16, 8);
$fraction->isInteger(); // true
```

## Installation

Add package to your composer.json file

```json

{
    "require": {
        "phospr/fraction": "dev-master"
    }
}
```

## Disclaimer

I googled first to find something similar, but only came across the [pear](https://pear.php.net) [Math_Fraction](https://pear.php.net/package/Math_Fraction) library, and since I'm a lazy arse, that didn't apeal.  If anyone knows of one available on [packagist](http://packagist.com), please let me know.

Cheers,

Tom
