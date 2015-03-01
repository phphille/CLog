# CLog

## About
A class for logging and debugging the loading time

    PHP 5 >= 5.3.0

## Introduction

Instantiate an object of CLog like  $clog = new \phpe\log\CLog();

Then you write $clog->Timestamp(__CLASS__, __METHOD__, 'A description');  where you want to start the logging and continue to deploy several other $clog->Timestamp(__CLASS__, __METHOD__, 'Another description'); in different places.

When you have deployed your timestamps you can print out the result with $clog->TimestampAsTable();


# Using anax-mvc

Make it apart of $Di like:

$di->setShared('clog', function() {
   $clog = new \phpe\log\CLog();
   $clog->Timestamp(__CLASS__, __METHOD__, 'a comment'); 
   return $clog;
});

Then can you, depenending where in the code you want to reach CLog, reach the class whit either $app or $di;
$app->clog->Timestamp(__CLASS__, __METHOD__, 'a comment'); 
or
$this->di->clog->Timestamp(__CLASS__, __METHOD__, 'a comment');



[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/phphille/CLog/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/phphille/CLog/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/phphille/CLog/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/phphille/CLog/?branch=master)
[![Build Status](https://scrutinizer-ci.com/g/phphille/CLog/badges/build.png?b=master)](https://scrutinizer-ci.com/g/phphille/CLog/build-status/master)
