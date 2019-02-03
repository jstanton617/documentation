---
title: MY API ENDPOINT
type: apicontent
order: XX.1
---

## LIST

List endpoint returns logs that match a log search query. Results are paginated.


##### ARGUMENTS

* `query` [*required*]:  
    the search query - following https://docs.datadoghq.com/logs/explorer/search/#search-syntax syntax
* `time.from` [*required*]:  
    minimum timestamp for requested logs. Format can be either
    - an ISO-8601 string
    - a unix timestamp (number representing the elapsed millisec since epoch)
* `time.to` [*required*]:  
    maximum timestamp for requested logs. Format can be either
    - an ISO-8601 string
    - a unix timestamp (number representing the elapsed millisec since epoch)
* `time.timezone` [*optional*, *default*=**None**]:
   Can be specified both as an offset (eg "UTC+03:00") or a regional zone (eg "Europe/Paris")
* `time.offset` [*optional*, *default*=**None**]:
   Equivalent to time.timezone. But value in seconds.
   If both timezone and offset are specified, timezon is ignored.
* `startAt` [*optional*, *default*=**None**]:  
   For pagination purpose. Hash of the first log returned. 
   Response includes hash of the first non-returned log.
* `sort` [*optional*, *default*=**desc**]:  
    Time-ascending or time-descending results.
* `limit` [*optional*, *default*=**10**]:  
    Number of logs return in the response (maximum is 1000)
