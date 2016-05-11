# Serialize
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/byjg/serialize/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/byjg/serialize/?branch=master)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/6375df04-b1f8-4f5f-94f8-a375f630250a/mini.png)](https://insight.sensiolabs.com/projects/6375df04-b1f8-4f5f-94f8-a375f630250a)
[![Build Status](https://travis-ci.org/byjg/serialize.svg?branch=master)](https://travis-ci.org/byjg/serialize)

Serialize any object into array and format it JSON or XML

## Basic Usage

Just use the Serialize class with any kind of object, stdClass or array;

```php
$serializer = new \ByJG\Serialize\SerializerObject($data);
$result = $object->build();
```

`$result` is an array. You can use a Formatter to transform it in JSON or XML.

## Create a *bindable* object

```php
// Create the class
class MyClass extends BinderObject
{}

// Bind any data into the properties of myclass
$myclass->bind($data);

// You can convert to array all properties
$myclass->toArray();
```

or

```php
// Set all properties from $source that matches with the property in $target
BinderObject::bindObject($source, $target);

// Convert all properties of any object into array
BinderObject::toArrayFrom($source);
```

## Install

```
composer require "byjg/serialize=1.0.*"
```

## Test

```
phpunit
```

