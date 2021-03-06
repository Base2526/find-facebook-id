# find-facebook-id

[![npm version](https://badge.fury.io/js/find-facebook-id.svg)](https://badge.fury.io/js/find-facebook-id)
[![CircleCI](https://circleci.com/gh/pradel/find-facebook-id.svg?style=svg)](https://circleci.com/gh/pradel/find-facebook-id)

Find a facebook id given a Facebook name.

Support:
- users
- pages
- groups (You will need a valid facebook access token)

### Install
```
yarn add find-facebook-id
npm i --save find-facebook-id
```

### Usage
```javascript
import findFacebookId from 'find-facebook-id';

// Find facebook id return a promise

const id = await findFacebookId('zuck');

findFacebookId('zuck').then((id) => {
  console.log(`facebook id of zuck is: ${id}`);
}).catch((err) => {
  console.log(err);
});

// To query a group you must pass a valid facebook access token
findFacebookId('groupsatopenuniversity', facebookAccessToken).then((id) => {
  console.log(`facebook id of groupsatopenuniversity is: ${id}`);
}).catch((err) => {
  console.log(err);
});
```

### Cli
Install:
```
yarn global add find-facebook-id
npm i -g find-facebook-id
```

Usage:
```
$ find-facebook-id <username/pagename>
$ find-facebook-id <groupname> <facebook-access-token>
```
