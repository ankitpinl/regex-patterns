### Explanation of regular expression
- \s - \s matches any whitespace character
- . - match any character
- + - matches the previous token between one and unlimited times.
- ^ - asserts position at start of a line
- \w - matches any word character (equivalent to [a-zA-Z0-9_])
- \d - matches a digit (equivalent to [0-9])

| Command | Description |
| --- | --- |
| `\d` | Match for a single digit |
| `\D` | Do not match \d |
| `\w` | Match for a single letter or digit (0-9 or a-z or A-Z) |
| `\W` | Do not match \w |
| `\s` | Match a single space (space, tab, newline characters included) |
| `\S` | Do not match \s |
| `[A-D]` | Match a single character in the A-D range |
| `[^A-D]` | Don't match a single character in the A-D range |
| `.` | A single wildcard |
| `?` | Match previous character 0 or 1 time |
| `*` | Match previous character 0 or more times |
| `+` | Match previous character 1 or more times |
| `{3}` | Match previous character 3 times |
| `{1,3}` | Match previous character between 1 and 3 times |

| Command | Description |
| --- | --- |
| `4?986` | Here the 4 is optional but now you see we are matching on anything that either has 4 or doesn't have it. |
| `a{2, 4}` | matching 2 or 3 or 4 times but not matching one time. |


### match 6 digit number
```Javascript
const numberPattern = /\d{6}/gm;
return numberPattern.test(123456);
```

### match a single character 3 times
```Javascript
const numberPattern = /[a]{3}/gm;
'aaah, this is practice place'.match(numberPattern);
```

### match start with H and end with !
```Javascript
const numberPattern = /^H.+!/gm;
'Hello world! This is regex.'.match(numberPattern);
```

### match a single character in the range between a and h
```Javascript
const numberPattern = /[a-h]/gm;
'aaah, this is practice place'.match(numberPattern);
```

### match a single character either a or h
```Javascript
const numberPattern = /[a|h]/gm;
'aaah, this is practice place'.match(numberPattern);
```

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

### Phone Varification xxx-xxx-xxxx pattern
```Javascript
const re = /d{3}-\d{3}-\d{4}/;
return re.test(903-355-8036);
```

### Phone number with minimal false positives
```Javascript
const re = /^(?:\+1[-. ]?)?(?:\(?([0-9]{3})\)?[-. ]?)?([0-9]{3})[-. ]?([0-9]{4})$/gm;
return re.test(903-355-8036);
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

### Meta character matching (match five characters with space)
```Javascript
const re = /\w{5}\s\w{5}\!/;
return re.test('Hello World!');
```

### To match the start and of the string
```Javascript
const re = /^Hello World!$/;
return re.test('Hello World!');
```