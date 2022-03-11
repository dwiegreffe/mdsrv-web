---
title: MDsrv
---

<a name="install"></a>
## How do I install a MDsrv server on my machine (Setting up your own server and viewer)?

See: [https://github.com/dwiegreffe/mdsrv](https://github.com/dwiegreffe/mdsrv) README.md

<a name="import-tr-md"></a>
## How do I add a trajectory to my own MDsrv server?

1. Add your trajectory into the trajectory folder of your server.
2. Update the trajectory_index.json. 
An entry has the following format:
```
{
    "timestamp": 123,
    "id": "example_id",
    "name": "example_name",
    "description": "example_description"
}
```

Whereas the id (example_id) must be the name of the trajectory file in the trajectory directory, and the id must be unique.
Currently, only trajectories in the XTC format can be streamed.