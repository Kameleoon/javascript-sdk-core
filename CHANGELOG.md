# Change Log

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
