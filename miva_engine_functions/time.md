## Time

Most of these functions must be called with two arguments, here designated time_t and time_zone. time_t is the number of seconds since the beginning of C.U.T. (Coordinated Universal Time) at 00:00:00 January 1, 1970. This value can be obtained from the system variables time_t and dyn_time_t (time_t is set when the script starts executing; dyn_time_t is updated at the moment that it is used; which one you use depends on what your program does).

time_zone is the number of hours before or after GMT; this value can be obtained using the built-in function timezone(). Here is an example of how a time function can be called:

**Note:** *These functions cannot be used to process dates earlier than January 1, 1970, or later than January 19, 2038.*


## mktime_t
```
mktime_t( year, month, dayofmonth, hours, minutes, seconds, timezone )
```
Returns the s.time_t value for the time specified. time_zone can be the keyword 'local'

## timezone
```
timezone()
```
Returns an integer which is the number of hours behind or ahead of GMT (not accounting for Daylight Time)

## time_t_dayofmonth
```
time_t_dayofmonth( timet, time_zone )
```
Returns the current month as a number. time_zone can be the keyword 'local'

## time_t_dayofweek
```
time_t_dayofweek( timet, time_zone )
```
Returns the current day of the week as a number (Sunday=1). time_zone can be the keyword 'local'

## time_t_dayofyear
```
time_t_dayofyear( timet, time_zone )
```
Returns the number of days since the beginning of the year, including today. time_zone can be the keyword 'local'

## time_t_hour
```
time_t_hour( timet, time_zone )
```
Returns current hour (using a 24-hour clock). time_zone can be the keyword 'local'

## time_t_min
```
time_t_min( timet, time_zone )
```
Returns the current minute in the hour. time_zone can be the keyword 'local'

## time_t_month
```
time_t_month( timet, time_zone )
```
Returns the current month as a number. time_zone can be the keyword 'local'

## time_t_sec
```
time_t_sec( timet, time_zone )
```
Returns the current second in the minute. time_zone can be the keyword 'local'

## time_t_year
```
time_t_year( timet, time_zone )
```
Returns the current year, time_zone can be the keyword 'local'
