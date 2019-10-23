[rxjs-retry-extra](../README.md) › [Globals](../globals.md) › ["retryExtra"](../modules/_retryextra_.md) › [INotifier](_retryextra_.inotifier.md)

# Interface: INotifier

**`description`** A function is applied to each error and index emitted by the
source Observable. It returns a notifier Observable, which can be replaced
with Promise or Async-Await to set whether and when to try again.

## Hierarchy

* **INotifier**

## Callable

▸ (`params`: object): *Observable‹any›*

Defined in retryExtra.ts:9

**Parameters:**

▪ **params**: *object*

The error of params is emitted by the source Observable.
The index of params is the number i for the i-th emission that has happened
since the subscription, starting from the number
0.

Name | Type |
------ | ------ |
`error` | any |
`index` | number |

**Returns:** *Observable‹any›*

If that Observable calls complete or error then this method will
aborting the retry. Otherwise, the error will be thrown.
