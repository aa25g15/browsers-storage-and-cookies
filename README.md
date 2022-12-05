# Browser Storage And Cookies

## Local Storage
* 10mb size
* Infinite life, even after browser close, till manually deleted or cleared
* Local to browser only
* Is not sent with requests
* HTML5 support
* Accessible from any window

```javascript
localStorage.setItem('name', 'Abhinav'); // Note - only strings can be stored
localStorage.setItem('name', 'Rahul'); // Will set a new value for 'name' key
localStorage.removeItem('name');
```

## Session Storage
* 5mb size
* Gets deleted after tab close or if manually deleted or cleared
* Local to browser only
* Is not sent with requests
* HTML5 support
* Accessible from same tab

```javascript
sessionStorage.setItem('name', 'Abhinav'); // Note - only strings can be stored
sessionStorage.setItem('name', 'Rahul'); // Will set a new value for 'name' key
sessionStorage.removeItem('name');
```

## Cookies
* 4kb size
* Need to manually set expiry date
* Local to browser and is also sent to server
* Do not use cookies unnecessarily because they can slow down requests as they are sent to the server on each request
* HTML4/5 support
* Accessible from any window
* Due to their native manipulation syntax, it is best to use a library for managing cookies
* To make a cookie that never expires, just set a ridiculously large year

```javascript
document.cookie = "firstName=Abhinav; expires=" + new Date(9999, 0, 1).toUTCString();
document.cookie = "lastName=Aggarwal; expires=" + new Date(9999, 0, 1).toUTCString();

/*
Will create 2 cookies - firstName and lastName which never expire
*/

console.log(document.cookie); // Output - "firstName=Abhinav; lastName=Aggarwal"

/*
Notice the tedious syntax for handling cookies, natively, so we should use a library
*/
```
