[rxjs-retry-extra](../README.md) › [Globals](../globals.md) › ["retryExtra"](_retryextra_.md)

# External module: "retryExtra"

## Index

### Interfaces

* [INotifier](../interfaces/_retryextra_.inotifier.md)

### Functions

* [retryExtra](_retryextra_.md#retryextra)

## Functions

###  retryExtra

▸ **retryExtra**<**T**>(`count?`: undefined | number, `interval?`: undefined | number): *MonoTypeOperatorFunction‹T›*

Defined in retryExtra.ts:34

**`description`** Use only two numeric parameters to control the number and
interval of retries simply.

**Type parameters:**

▪ **T**

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`count?` | undefined &#124; number | The maximum number of retry attempts. The default is -1 and it will continue to retry until there are no errors.  |
`interval?` | undefined &#124; number | Optional, in milliseconds. Ignored if the `Notifier` is assigned to the countOrNotifier parameter. Default is -1, and it's will run a retry immediately in sync. If it's greater than or equal to zero, an asynchronous timer is used as the time interval.  |

**Returns:** *MonoTypeOperatorFunction‹T›*

The source Observable modified with the retry logic.

▸ **retryExtra**<**T**>(`notifier?`: [INotifier](../interfaces/_retryextra_.inotifier.md)): *MonoTypeOperatorFunction‹T›*

Defined in retryExtra.ts:48

**`description`** Inject a `Notifier` function to perform more complex operations.

**Type parameters:**

▪ **T**

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`notifier?` | [INotifier](../interfaces/_retryextra_.inotifier.md) | Receive a `Notifier` function that is applied to each error and index emitted by the source Observable.The function returns a notifier Observable, which can be replaced with Promise or Async-Await to set whether and when to try again.  |

**Returns:** *MonoTypeOperatorFunction‹T›*

The source Observable modified with the retry logic.
