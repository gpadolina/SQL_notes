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
