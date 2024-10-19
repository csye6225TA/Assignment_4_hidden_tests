## Test Case: `load and get count`

## Overview
This will test the load functionality.

### Purpose
It is crucial that save and load are handled well. Since, we are dealing with 2 servers and data is being sent across both - this should be abstracted from the user. Hence, save and load functionalities must be handled in such a way that the user still believes they are sending requests to a single server.

### Test Details

The returned ID from the previous snapshot it copied. A client container is made to sleep for a while during which, the container is logged into and a new csv file is created and manually run.

It is expected that both oranges and apple types are loaded back with the correct count.

```
getting into container and creating a csv file as below

load_data,<snapshot_returned>
get_count,apples
get_count,oranges
```

OR

```
client.py

client.load_data(snapshot_id)
client.get_count("apples")
client.get_count("oranges")
```

### Note
#### It is ensured that the servers are still running when this test is being run.

Another way this was tested if client_file.py was not performing as expected was to create subsequent requests in client.py, save the ID and call load API and verify results.
