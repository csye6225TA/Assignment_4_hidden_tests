## Test Case: `create, save, undefine`

## Overview

This test case aims to create 2 types apples and oranges.

### Test Details

Each type should be redirected to a different server based on the range. Lastly, the snapshot ID is recorded to be used in the next test case.

```
define_stuff,apples,healthy
define_stuff,oranges,refreshing
add,7,apples
add,3,oranges
save_data,
undefine,apples
undefine,oranges
```

### Note

All the APIs are to work as expected. Incase client_file.py does not handle save, load - subsequent calls are made to client.py directly to try making it work and verify results.
