# loopback-object-acl
Loopback provides great "class-level" ACL's for restricting access to a whole Model or its mehods, but greatly lacks the ability to restric access to individual objects. This project tries to solve this, by setting object-level ACL's on each object, and manipulates Loopback's Query to only return objects the requesting user has access to.

## Install

```
npm install loopback-object-acl
```

In `model-config.json` add `../node_modules/loopback-object-acl` to mixins

```js
  "_meta": {
    "sources": [
      "loopback/common/models",
      "loopback/server/models",
      "../common/models",
      "./models"
    ],
    "mixins": [
      "loopback/common/mixins",
      "loopback/server/mixins",
      "../common/mixins",
      "./mixins",
      "../node_modules/loopback-object-acl"
    ]
  }
```

## TODO

### Read-permissions
- [x] Do only return objects from database that the requesting user has access to.

### Write-permissions
Version 2.0

### Client
- [ ] Set ACL on object-creation
- [ ] Set permissions on user creation


### Tests
- [ ] ObjectAcl.js
- [ ] CurrentUserUtil.js
