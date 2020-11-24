
# Installation

###### Using NPM 

``` npm install --save xsrf-cookie ```

# Usage

``` import { getCookie } from 'xsrf-cookie'```

##### Get XSRF Token from browser cookies

```
let xsrfToken = getCookie(); // No need to pass the parameter to get xsrf token.

```
##### Pass XSRF Token in request header

```
$.ajaxSetup({
    beforeSend: function(xhr) {
      xhr.setRequestHeader('X-XSRF-TOKEN', xsrfToken);
    }
})

```
### OR

```
 headers: {
  'Content-Type': ...,
  'X-XSRF-TOKEN': xsrfToken
}

```

##### Get specific cookie from browser Cookies

```
let value = getCookie(cookieName); // Pass the parameter with the specific cookieName

```

##### Pass Specific Cookie in request header

```
$.ajaxSetup({
    beforeSend: function(xhr) {
      xhr.setRequestHeader('key', value);
    }
})

```
### OR

```
 headers: {
  'Content-Type': ...,
  'key': value
}

```
