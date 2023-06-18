### Get only numbers from the string.
```Javascript
const numberPattern = /\d+/g;
'something102asdfkj1948948'.match(numberPattern);
```

### Get array from the href
```Javascript
const reURLInformation = new RegExp(
    [
        "^(https?:)//", // protocol
        "(([^:/?#]*)(?::([0-9]+))?)", // host (hostname and port)
        "(/{0,1}[^?#]*)", // pathname
        "(\\?[^#]*|)", // search
        "(#.*|)$" // hash
    ].join("")
);
const match = item.url.match(reURLInformation);
```

### Email Validation
```Javascript
const re = /^\S+@+\S+\.+\S+/;
return re.test('a@gmail.com');

const emailReg = RegExp(
    /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/gm
);
if (!emailReg.test(email)) {}
```

### Phone Varification
```Javascript
const re = /^[(][0-9]{3}[)][0-9]{3}-[0-9]{4}/;
return re.test(9033558036);
```

### Username must be between 4-12 characters & Can only contain letters, numbers, dashes or underscores
```Javascript
    const usernameReg = RegExp(/^[a-z0-9_-]{4,12}$/);
    if (!usernameReg.test(username)) {}
```

### Password must contain a minimum eight characters, at least one letter and one number
```Javascript
    const passwordReg = RegExp(/^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$/);
    if (!passwordReg.test(password)) {}
```