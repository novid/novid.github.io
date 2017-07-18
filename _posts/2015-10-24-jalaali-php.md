---
layout: post
title: Jalaali PHP
---

## Gregorian to Jalaali Date Convertion and Vice Versa.

In software engineering field there are many terms that people talk about them. Two of them are **scratch your own itch** and _whether or not_ to **reinvent the wheel**. I think in many times it depends on your project needs and what you are trying to solve in real world and there is no global answer about it. The goal of this project and others in [Jalaali Organiztion](http://github.com/jalaali) is to provide a robust and powerful API for different programming languages and platforms in order to solve the problem of Gregorian to Jalaali calendar system convertion and vice versa. Although there are several third party libraries to cover this topic such as [jDateTime](http://sallar.me/projects/jdatetime) by _Sallar Kaboli_ but these tools are different in both algorithm implementation and support for different programming languages.

> Jalaali calendar is a sidereal calendar that was used in Persia, variants of which today are still in use in Iran as well as Afghanistan.
> - [Wikipedia](https://en.wikipedia.org/wiki/Jalali_calendar)

The population of these two country reaches more than 100 million people who uses Jalaali calendar in every day life. In contrast to world population which is more than 7 billion people, that number is just about 1% of people who use this calendar in real life. But there is not an easy way to somehow calculate this percent in digital life, specially after 2010 and growth of data in just five years. Tired of theory and history? me too, let's :unlock: the API.

### Examples

    // Convert PHP 3.0.x release date to Jalaali
    \Jalaali\Jalaali::toJalaali(2000, 10, 20)

    // Convert library release date to Jalaali
    \Jalaali\Jalaali::toJalaali(2015, 10, 10)

### API for v1.0.0

First release of [Jalaali PHP](http://github.com/jalaali/jalaali-php) is constructed within the same namespace and class name of the library and contains 10 static methods described bellow. For reference of each method describtion, parameteres and return value have a look at `docs/api` folder in project root.

    // Converts a Gregorian date to Jalaali
    toJalaali($gy, $gm, $gd)

    // Converts a Jalaali date to Gregorian
    toGregorian($jy, $jm, $jd)

    // Checks whether a Jalaali date is valid or not
    isValidJalaaliDate($jy, $jm, $jd)

    // Checks whether this is a leap year or not
    isLeapJalaaliYear($jy)

    // Number of days in a given month in Jalaali year
    jalaaliMonthLength($jy, $jm)

    // Base Algorithm
    jalaaliCalendar($jy)

    // Converts a date of the Jalaali calendar to the Julian Day Number
    j2d($jy, $jm, $jd)

    // Converts the Julian Day Number to a date in the Jalaali calendar
    d2j($jdn)

    // Calculates the Julian Day number from Gregorian or Julian calendar dates
    g2d($gy, $gm, $gd)

    // Calculates Gregorian and Julian calendar dates from the Julian Day number
    d2g($jdn)

### TODO

* Extend the functionality of PHP's [DateTime](http://php.net/manual/en/class.datetime.php) class.
* Prepare to port this library into Python and Perl in order to provide a robust library for LAMP stack.
