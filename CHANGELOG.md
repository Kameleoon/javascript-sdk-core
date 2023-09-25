# Change Log

# 2.9.0 (2023-09-25)


### Features

* Added `getClientConfigurationUrl` utility

# 2.8.3 (2023-09-05)


### Bug fixes

* `UserAgent` was not exported from SDK

# 2.8.2 (2023-08-31)


### Bug fixes

* `Custom Data Condition` now handles index `0` properly

# 2.8.1 (2023-08-25)


### Bug fixes

* Multiple `Real Time Update` connections are no longer created
* `Custom Data Condition` now handles all exceptions properly

# 2.8.0 (2023-08-11)


### Bug fixes

* Empty Custom Data is now sending activity tracking event

### Features

* Added [Tracking requests rate limit](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/nodejs-sdk#tracking-rate-limit) capabilities
* Added [Cross Device Custom Data Synchronization](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#cross-device-custom-data-synchronization) capabilities

# 2.7.1 (2023-07-26)


### Bug fixes

* [`flush`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#flush) now sends offline tracking requests even if there's no new data to track.
* Timestamps for offline requests are set correctly.

# 2.7.0 (2023-07-21)


### Features

- `flushData` has been deprecated in favor of [`flush`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#flush).
- [`flush`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#flush) sends failed tracking requests that were stored locally during the offline mode at first and then proceeds with the latest request.

# 2.6.0 (2023-07-17)


### Bug fixes

- Typescript `.d.ts` files have proper relative path resolution.
- Unused tracking parameters are no longer sent.
- Real-time update events now get the latest configuration.

### Features

- When the client is initialized in offline mode, in case of network issues failed tracking requests made by [`flushData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk/#flushdata), [`trackConversion`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk/#trackconversion), [`triggerExperiment`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk/#triggerexperiment), [`getFeatureFlagVariationKey`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk/#getfeatureflagvariationkey) or [`getFeatureFlagVariable`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk/#getfeatureflagvariable) will be sent anew once the client is back online.
- Minor optimization for checking [targeting conditions](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#list-of-supported-targeting-conditions) of a segment.

# 2.5.1 (2023-06-30)


### Bug fixes

* tracking data duplications

# 2.5.0 (2023-06-28)

### Bug fixes

- Improve error handling for [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api)
- Visitor code is now validated correctly in every method that uses it.
- Result bundle is now compatible with systems not using `ESM` and `CommonJS`. It's minimized and uses code splitting for `crypto-js` `sha256` function.
- Parameter `revenue` for [`Conversion`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#conversion) is now optional.
- Each visitor can now only have one type of associated [`Kameleoon Data Type`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#data-types), except for [`CustomData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#customdata), that a visitor can have one per `customDataIndex`.

### Features

- New conditions are now supported: `Device`, `Browser`, `SDKLanguage`, `Page Title`, `Page View`, `Visitor Code`, `Conversion`. See the [full list of supported conditions](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#list-of-supported-targeting-conditions).
- [`Browser`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#browser) now has new optional parameter `version`.
- [`flushData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#flush-tracking-data) `visitorCode` parameter is now optional.
- Custom data that is marked as `local only` on Kameleoon Platform is now only used for targeting (not flushed with tracking requests).
- JavaScript SDK is now available as a single file from the static server, see the [details](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#installation)

# 2.4.6 (2023-06-02)


### Bug fixes

* Custom data true/false match type should work when condition value is `null`

# 2.4.5 (2023-06-01)


### Bug fixes

* Empty visitor code is no more allowed
* Incorrect tracking body upon triggering an experiment

# 2.4.4 (2023-05-31)


### Bug fixes

* Improve targeting data cleanup interval handling

# 2.4.3 (2023-05-24)


### Bug fixes

* Fixed issue for sending unique `Nonce` parameter on tracking requests

# 2.4.2 (2023-05-21)


### Bug fixes

* [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api) current visits not being up-to-date

# 2.4.1 (2023-05-20)


### Bug fixes

* [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api) data parse error

# 2.4.0 (2023-05-19)


### Bug fixes

* more meaningful URL names for requester
* `updateInterval` was set to 30 minutes instead of 60 in some places

### Features

* New method `getRemoteVisitorData`
* New offline mode for `initialize` method

# 2.3.0 (2023-04-28)


### Bug fixes

* Unused optional chaining operator in `KameleoonUtils` was removed
* Experiments methods no more persist assigned variations

### Features

* Added retries for client initialization

# 2.2.1 (2023-04-24)


### Bug fixes

* Tracking feature flag rule with variation `off` wasn't displayed on result page

# 2.2.0 (2023-04-21)


### Features

* `getEngineTrackingCode` method is now public

# 2.1.1 (2023-04-18)


### Bug fixes

* visitor code cookie header

# 2.1.0 (2023-04-14)


### Bug fixes

* variation calculation logic
* remove sdk true parameter
* test regexp

### Features

* targeting cleanup interval
* get experiment variation data
* get engine tracking code
* api-ssx migration
* tracking requests and conditions

# 2.0.0 (2023-04-05)


### Bug fixes

* use correct top level domain for data
* remove kameleoon client headers

### Features

* integration of compute edge
* api-ssx migration
* tracking requests and conditions

# 1.1.1 (2023-03-24)


### Bug fixes

* change broken dependency

# 1.1.0 (2023-03-22)


### Features

- License changed from `GPL3.0` to `ISC`

# 1.0.0 (2023-03-21)


### Bug fixes

* remove xhr

### Features

* add feature flags v2

# 0.0.2 (2022-11-01)


### Bug fixes

* remove boolean case condition

# 0.0.1 (2022-10-13)

### Initial release
