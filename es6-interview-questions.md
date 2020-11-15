## What is the difference between Promises and Observables?
|Promise|Observables|
|-------|-----------|
|A promise can only handle one event|Observables are for streams of events over time|
|Emits a single value | Emits multiple values over a period of time|
|Not Lazy | Lazy. An Observable is not called until we subscribe to it|
|Can not be cancelled | Can be cancelled by using the unsubscribe() method|
|It does not provide any operators | provides the map, forEach, filter, reduce, retry, retryWhen operators|

https://medium.com/@mpodlasin/promises-vs-observables-4c123c51fe13

## Why and when to use forEach, map, filter, reduce, and find in JavaScript.
|Method|Use|
|.forEach()| it has advantages over the `for` with regards to scoping & clean code |
|.map()| to **transform** elements in an array|
|.filter()| to **select** a subset of multiple elements from an array|
|.find()| to **select** a single elememt from an array|
|.reduce()| to **derive** a single value from multiple elements in an array.|

https://medium.com/@JeffLombardJr/understanding-foreach-map-filter-and-find-in-javascript-f91da93b9f2c
