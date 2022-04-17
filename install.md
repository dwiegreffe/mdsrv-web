---
title: MDsrv
---

<center><img src='images/architecture.png'></center>

<a name="install"></a>
## How do I install a MDsrv instance on my machine (Setting up your own streaming server and frontend)?
We provide up-to-date images of the viewer (frontend) and streaming server available at Dockerhub. 

- [Viewer (frontend)](https://hub.docker.com/r/dwiegreffe/mdsrv-viewer)

Start it with "docker run  -p 80:4242   dwiegreffe/mdsrv-viewer https://remote.sca-ds.de"

If you want to use a different streaming server as default, start it with

"docker run  -p 80:4242   dwiegreffe/mdsrv-viewer your-url.here"

- [Streaming Server](https://hub.docker.com/r/dwiegreffe/mdsrv-remote)

Start it with "docker run -p 8080:1337 dwiegreffe/mdsrv-remote"

If the data should be persistent, the container must be started with the following command:

"docker run  -p 8080:1337  -v /path/on/the/host:/mdsrv/server dwiegreffe/mdsrv-remote"

If you want to stop the containers, the most reliable way is to use the command 'docker stop container-id". 

You can get the container ID for example with the command 'docker ps'. An example output is

CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
6a98b42df4c8 dwiegreffe/mdsrv-viewer "/change-url.sh http..."   12 seconds ago Up 11 seconds 0.0.0.0:424->4242/tcp, :::424->4242/tcp nostalgic_lumiere

The first column contains the required container ID.

The images can also be created with the following instructions: 

- [https://github.com/dwiegreffe/mdsrv](https://github.com/dwiegreffe/mdsrv)

A description of Docker and how to use it can be found here: 

- [Docker](https://docs.docker.com/get-started/)

<a name="import-tr-md"></a>
<details>
    <summary>How do I manually add a trajectory to my own MDsrv streaming server? </summary>
<p><div markdown="1">
If you do not want to add the trajectory via the GUI, you can also do this by adjusting the configuration of the streaming server.

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

Whereas the id ```example_id``` must be the name of the trajectory file in the trajectory directory, and the id must be unique.
Currently, only trajectories in the XTC format can be streamed.
</div></p></details>

<details>
    <summary>How do I manually add a session to my own MDsrv streaming server?</summary>
<p><div markdown="1">
If you want to add a saved session to the server without using the GUI, you can also do so by customizing the streaming server configuration.

1. Add your session into the session folder of your server.
2. Update the session_index.json. 
An entry has the following format:
```
{
    "timestamp": 123,
    "id": "example_id",
    "name": "example_name",
    "description": "example_description",
    "version": "3.4.0",
    "isSticky": true
}
```

Whereas the id ```example_id``` must be the name of the session file in the session directory, and the id must be unique.

The ```version``` parameter describes the version of the viewer in which the session was created. It is important to specify the correct version so that you can open the session later with the correct version of the viewer in case some functions are deprecated.

The ```isSticky``` parameter allows you to put a session on the server which cannot be deleted by another user via the GUI using the delete button. This parameter is optional and must be added only if it is set to true.
</div></p></details>