## Date Functions

### ADDDATE
ADDDATE( ) adds a time/date interval to a date and then returns the date.
```
ADDDATE(date, INTERVAL, value, addunit)                   # addunit: The type of interval to add:
                                                          # microsecond, second, minute, hour, day, week, month, quarter, year
                                                          # second_microsecond, minute_microsecond, minute_second, hour_microsecond
                                                          # hour_second, hour_minute, day_microsecond, day_second, day_minute
                                                          # day_hour, year_month
```
### ADDTIME
ADDTIME( ) adds a time interval to time/datetime and then returns the time/datetime.
```
SELECT ADDTIME(datetime, addtime)
```
### CURDATE
CURDATE( ) returns the current date. This function is equal to CURRENT_DATE( ). Date is returned as "YYY-MM-DD" as a string or YYYYMMDD as numeric.
```
SELECT CURDATE( )
```
### CURRENT_DATE
CURRENT_DATE( ) returns the current data. The same function as CURDATE( ).
```
SELECT CURRENT_DATE( )
```
### CURRENT_TIME
CURRENT_TIME( ) returns the current time. This function is equal to CURTIME( ).
```
SELECT CURRENT_TIME( )
```
### CURRENT_TIMESTAMP
CURRENT_TIMESTAMP( ) returns the current date and time.
```
SELECT CURRENT_TIMESTAMP( )
```
### CURTIME
CURTIME( ) returns the current time. The same function as CURRENT_TIME( ).
```
SELECT CURTIME( )
```
### DATE
DATE( ) extracts the date part from a datetime expression.
```
SELECT DATE(expression)
```
### DATEDIFF
DATEDIFF( ) returns the number of days between two date values.
```
SELECT DATEDIFF(date1, date2)                                # date1, date2: YYYY-MM-DD
```
### DATE_ADD
DATE_ADD( ) adds a time/date interval to a date and then returns the date.
```
SELECT DATE_ADD(date, INTERVAL value addunit)                # addunit: The type of interval to add.
                                                             # microsecond, second, minute, hour, day, week, month, quarter, year
                                                             # second_microsecond, minute_microsecond, minute_second
                                                             # hour_microsecond, hour_second, hour_minute, day_microsecond
                                                             # day_second, day_minute, day_hour, year_month
```
### DATE_FORMAT
DATE_FORMAT( ) formats a date as specified.
```
SELECT DATE_FORMAT(date, format)                             # %a	Abbreviated weekday name (Sun to Sat)
                                                             # %b	Abbreviated month name (Jan to Dec)
                                                             # %c	Numeric month name (0 to 12)
                                                             # %D	Day of the month as a numeric value, followed by 
                                                               suffix (1st, 2nd, 3rd, ...)
                                                             # %d	Day of the month as a numeric value (01 to 31)
                                                             # %e	Day of the month as a numeric value (0 to 31)
                                                             # %f	Microseconds (000000 to 999999)
                                                             # %H	Hour (00 to 23)
                                                             # %h	Hour (00 to 12)
                                                             # %I	Hour (00 to 12)
                                                             # %i	Minutes (00 to 59)
                                                             # %j	Day of the year (001 to 366)
                                                             # %k	Hour (0 to 23)
                                                             # %l	Hour (1 to 12)
                                                             # %M	Month name in full (January to December)
                                                             # %m	Month name as a numeric value (00 to 12)
                                                             # %p	AM or PM
                                                             # %r	Time in 12 hour AM or PM format (hh:mm:ss AM/PM)
                                                             # %S	Seconds (00 to 59)
                                                             # %s	Seconds (00 to 59)
                                                             # %T	Time in 24 hour format (hh:mm:ss)
                                                             # %U	Week where Sunday is the first day of the week (00 to 53)
                                                             # %u	Week where Monday is the first day of the week (00 to 53)
                                                             # %V	Week where Sunday is the first day of the week (01 to 53). 
                                                                Used with %X
                                                             # %v	Week where Monday is the first day of the week (01 to 53). 
                                                                Used with %X
                                                             # %W	Weekday name in full (Sunday to Saturday)
                                                             # %w	Day of the week where Sunday=0 and Saturday=6
                                                             # %X	Year for the week where Sunday is the first day of the 
                                                                week. Used with %V
                                                             # %x	Year for the week where Monday is the first day of the 
                                                                week. Used with %V
                                                             # %Y	Year as a numeric, 4-digit value
                                                             # %y	Year as a numeric, 2-digit value
```
### DATE_SUB
DATE_SUB( ) subtracts a time/date interval from a date and then returns the date.
```
SELECT DATE_SUB(date, INTERVAL value interval)               # interval: The type of interval to subtract.
                                                             # microsecond, second, minute, hour, day, week, month, quarter, year
                                                             # second_microsecond, minute_microsecond, minute_second
                                                             # hour_microsecond, hour_second, hour_minute, day_microsecond
                                                             # day_second, day_minute, day_hour, year_month
```
### DAY
DAY( ) returns the day of the month for a given date (a number from 1 to 31). This is the same as DAYOFMONTH( ).
```
SELECT DAY(date)
```
### DAYNAME
DAYNAME( ) returns the weekday name for a given date.
```
SELECT DAYNAME(date)
```
### DAYOFMONTH
DAYOFMONTH( ) returns the day of the month for a given date. THis is the same as DAY( ).
```
SELECT DAYOFMONTH(date)
```
### DAYOFWEEK
DAYOFWEEK( ) returns the weekday index for a given date (a number from 1 to 7 with 1 as Sunday).
```
SELECT DAYOFWEEK(date)
```
### DAYOFYEAR
DAYOFYEAR( ) returns the day of the year for a given date (a number from 1 to 366).
```
SELECT DAYOFYEAR(date)
```
### EXTRACT
EXTRACT( ) extracts a part from a given date.
```
SELECT EXTRACT(part FROM date)
```
### FROM_DAYS
FROM_DAYS( ) returns a date from a numeric datevalue. This is opposite of the TO_DAYS( ) function.
```
SELECT FROM_DAYS(number)
```
### HOUR
HOUR( ) returns the hour part for a given date from 0 to 838.
```
SELECT HOUR(datetime)
```
### LAST_DAY
LAST_DAY( ) extracts the last day of the month for a given date.
```
SELECT LAST_DAY(date)
```
### LOCALTIME
LOCALTIME( ) returns the current date and time.
```
SELECT LOCALTIME( )
```
### LOCALTIMESTAMP
LOCALTIMESTAMP( ) returns the current date and time.
```
SELECT LOCALTIMESTAMP( )
```
### MAKEDATE
MAKEDATE( ) creates and returns a date based on a year and a number of days value.
```
SELECT MAKEDATE(year, day)
```
### MAKETIME
MAKETIME( ) creates and returns a time based on an hour, minute, and second value.
```
SELECT MAKETIME(hour, minute, second)
```
### MICROSECOND
MICROSECOND( ) returns the microsecond part of a time/datetime.
```
SELECT MICROSECOND(datetime)
```
### MINUTE
MINUTE( ) returns the minute part of a time/datetime.
```
SELECT MINUTE(datetime)
```
### MONTH
MONTH( ) returns the month part for a given date.
```
SELECT MONTH(date)
```
### MONTHNAME
MONTHNAME( ) returns the name of the month for a given date.
```
SELECT MONTHNAME(date)
```
