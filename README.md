# CLog

## About
A class for logging and debugging the loading time

    PHP 5 >= 5.3.0

## Introduction

Instantiate an object of CLog like  $clog = new \phpe\log\CLog();

Then you write $clog->Timestamp(__CLASS__, __METHOD__, 'A description');  where you want to start the logging and continue to deploy several other $clog->Timestamp(__CLASS__, __METHOD__, 'Another description'); in different places.

When you have deployed your timestamps you can print out the result with $clog->TimestampAsTable();
