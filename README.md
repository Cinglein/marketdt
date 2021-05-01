# marketdt


[![image](https://img.shields.io/pypi/v/marketdt.svg)](https://pypi.python.org/pypi/marketdt)


**A python package that connects to a market-focused datetime API**


-   Free software: MIT license
-   Documentation: https://Cinglein.github.io/marketdt
    

## Features

# **In NYSE**

The `Nyse` class deals with the dates of securities traded on the 
New York Stock Exchange. 

To access: `from marketdt import Nyse`

To call the below functions: `Nyse.function_name(args)`

### trading_day(d,e=0) -> bool
  
       d is a datetime date, e is an int representing a year
  
       Returns True if d is a NYSE trading day, and false otherwise.
       Omit e or set it to 0 if dealing with actual dates; for expected
       dates, set e to the year from which you are projecting.
       Use dates after 1 January 1971! The function may be inaccurate
       with earlier dates.

### td(d,e=0) -> bool

       alias of trading_day

### holiday(d,e=0) -> bool

       d is a datetime date

       Returns True if d is a NYSE holiday, and false otherwise.
       Omit e or set it to 0 if dealing with actual dates; for expected
       dates, set e to the year from which you are projecting.
       Use dates after 1 January 1971! The function may be inaccurate
       with earlier dates.

       (Note that if a holiday falls on a weekend, its actual observance 
       may fall on a different date!)

### days_between_actual(a,b) -> int
  
       a and b are both datetime dates
       
       Returns the number of actual NYSE trading days between a and b.

### dba(a,b) -> int

       alias of days_between_actual

### days_between_expected(a,b) -> int

       a and b are both datetime dates
  
       Returns the number of expected NYSE trading days between a and b.
       Projects from a's year, assuming that a's calendar schedule will continue forever

### dbe(a,b) -> int

       alias of days_between_expected

## Credits

This package was created with [Cookiecutter](https://github.com/cookiecutter/cookiecutter) and the [giswqs/pypackage](https://github.com/giswqs/pypackage) project template.