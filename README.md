# uuid4
A tiny C library for generating [uuid4](http://www.ietf.org/rfc/rfc4122.txt)
strings.

### Usage
[uuid.c](src/uuid.c?raw=1) and [uuid.h](src/uuid.h?raw=1) should be dropped into
an existing project. The library contains one function to generate a uuid4
string and store it in a buffer of at least `UUID4_LEN` in size.

```c
char buf[UUID4_LEN];
uuid4_generate(buf);
printf("%s\n", buf);
```

`uuid4_generate()` is not thread-safe.

### License
This library is free software; you can redistribute it and/or modify it under
the terms of the MIT license. See LICENSE for details.
