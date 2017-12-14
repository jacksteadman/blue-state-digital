# blue-state-digital

[![Generated with nod](https://img.shields.io/badge/generator-nod-2196F3.svg?style=flat-square)](https://github.com/diegohaz/nod)
[![NPM version](https://img.shields.io/npm/v/blue-state-digital.svg?style=flat-square)](https://npmjs.org/package/blue-state-digital)
[![Build Status](https://img.shields.io/travis/robertsonsamuel/blue-state-digital/master.svg?style=flat-square)](https://travis-ci.org/robertsonsamuel/blue-state-digital) [![Coverage Status](https://img.shields.io/codecov/c/github/robertsonsamuel/blue-state-digital/master.svg?style=flat-square)](https://codecov.io/gh/robertsonsamuel/blue-state-digital/branch/master)

A node module for accessing the blue state digital api service

## Install

    $ npm install --save blue-state-digital

## Usage

```js
import myModule from 'blue-state-digital';

const blueStateDigital = new BSD(options)
```

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### BSD

Create a new BSD rest client.

**Parameters**

-   `options` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** The BSD API Options.
    -   `options.baseUrl` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The base url of your bsd instance. IE: <https://XYZ>
    -   `options.apiID` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The App ID for your BSD API Secret.
    -   `options.apiSecret` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The API Secret for your BSD API App.
    -   `options.apiVer` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** The API version, default is 2 and 2 is only supported for now.

**Examples**

_The <b>BSD</b> constructor takes a API
  ID, if specified it will be used as default value for all endpoints that
  accept a API ID. The default is 2 but is required
  so you are aware of what version you are using._

```javascript
const blueStateDigital = new BSD({
  baseUrl: 'legislator.bsd.net',
  apiID: 'MyApiID',
  apiSecret: '43875utihgkfj38563y4uig',
  apiVer: 2,
})
```

#### authenticate

Returns **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Returns authentication response

#### searchEvents

Searches all the events and returns the future events unless specified by date_start.

REF: <https://secure.bluestatedigital.com/page/api/doc#-------------Event-API-Calls--------->

**Parameters**

-   `params` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** The BSD API Options.
    -   `params.event_id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by Event ID
    -   `params.event_type` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by Event Type
    -   `params.host_name` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the Host of the Event
    -   `params.day` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the day of the Event
    -   `params.date_start` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the start date of the Event
    -   `params.date_end` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the end date of the Event
    -   `params.create_day` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the created day of the Event
    -   `params.create_date_start` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the created start date of the Event
    -   `params.create_date_end` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by the created end date of the Event
    -   `params.country` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by events country
    -   `params.zip` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by events zipcode
    -   `params.city` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search by events by city
    -   `params.state` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events by state
    -   `params.zip_radius` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events in a given zipcode radius
    -   `params.radius_unit` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events in a given radius
    -   `params.attendee_cons_id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events by a consituent's ID who is attending
    -   `params.creator_cons_id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events by the consituent that created the Event
    -   `params.order_field` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Search events by order field

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** BSD JSON Response Promise

#### listForms

This method lists all signup forms and relevant data about those forms.
<https://secure.bluestatedigital.com/page/api/doc#---------------------list_forms-----------------0.7883351277818669>
No Params

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** BSD XML Response

#### getFormByID

This method gets all properties of the specified signup form.
<https://secure.bluestatedigital.com/page/api/doc#---------------------get_form----------------->

**Parameters**

-   `params` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Params Object
    -   `params.signup_form_id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** BSD Form ID

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** BSD XML Response Promise

### listFormFields

Retrieves a list of all form fields associated with a specified signup form.

<https://secure.bluestatedigital.com/page/api/doc#---------------------list_form_fields----------------->

**Parameters**

-   `params` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Params Object
    -   `params.signup_form_id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** BSD Form ID

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** BSD XML Response Promise

### utils

## License

MIT © [Samuel Robertson](https://www.robertsonsamuel.com)
