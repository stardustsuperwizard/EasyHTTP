# EasyHTTP

## Overview
 Library for making HTTP requests. This library can be loaded into a web app and imported into a javascript file and used.


## Example Usage
With Promises:
 ```javascript
const http = new EasyHTTP;


// Get Users
http.get('https://jsonplaceholder.typicode.com/users')
    .then(data => console.log(data))
    .catch(err => console.log(err));
```

As a function:
```javascript
const http = new EasyHTTP;

// POST and then PUT
async function main(http, data) {
    const postData = await http.post('https://jsonplaceholder.typicode.com/users', data);
    const putData = await http.put('https://jsonplaceholder.typicode.com/users/2', data);

    console.log(postData);
    console.log(putData);
}

main(http, data);
 ``` 


## Credits
Projects and excercises from Udemy course ["Modern JavaScript From The Beginning"](https://www.udemy.com/modern-javascript-from-the-beginning/) by Brad Traversy.