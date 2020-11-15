## What is the difference between Promises and Observables?
|Promise|Observables|
|-------|-----------|
|A promise can only handle one event|Observables are for streams of events over time|
|Emits a single value | Emits multiple values over a period of time|
|Not Lazy | Lazy. An Observable is not called until we subscribe to it|
|Can not be cancelled | Can be cancelled by using the unsubscribe() method|
|It does not provide any operators | provides the map, forEach, filter, reduce, retry, retryWhen operators|

https://medium.com/@mpodlasin/promises-vs-observables-4c123c51fe13
