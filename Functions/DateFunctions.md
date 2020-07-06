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
