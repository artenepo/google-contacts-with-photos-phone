# google-contacts-with-photos-phone

A promise based API to fetch contacts from Google with OAuth tokens **and photos and phone**.

This project is based on fork of https://github.com/stevelacy/google-contacts-oauth.

## Install
```sh
$ npm install google-contacts-with-photos-phone
```

## Usage


```js
var googleContacts = require('google-contacts-with-photos-phone');

var opts = {
  token: 'google oauth token'
};

googleContacts(opts)
    .then(function (data) {
        console.log(data);
    })
    .catch(function (err) {
        console.log(err);
    });

//=>[{email: 'me@slacy.me', name: 'Steve Lacy', phone: '99999999', photo: 'http://...'}, ... ]
```

## Options

**token**

OAuth token received from Google's OAuth API.
```
  type: 'String'
  default: null
  required: true
```

**max-results:**

Max results returned
```
  type: 'String'
  default: '500'
```


 - - -
*Lower level API*

**type**
```
  type: 'String'
  default: 'contacts'
```
**projection**
```
  type: 'String'
  default: 'full'
```

 - - -

## LICENSE

[MIT License](https://github.com/hadynz/google-contacts-with-photos/blob/master/LICENSE)
