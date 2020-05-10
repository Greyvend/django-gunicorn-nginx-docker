# MVE for PyCharm debugger attach timeout for docker-compose based interpreters

Assuming, docker-compose is installed, you're logged in [Docker Hub](https://hub.docker.com/), here's how to run this locally.

```
docker-compose up --build
```

After that, set up PyCharm.
1. Create project in the repo directory.
2. Add project interpreter as the **Docker Compose** -> Select **Service** as *app* from dropdown. **Python interpreter path** should be just *python*.
3. Click OK, exit.
4. Create running configuration if not autocreated.
    1. Click **Edit configurations...**
    2. Click **+**
    3. Select **Django Server**
    4. Type host `0.0.0.0`
    5. Save, quit.
5. Run the configuration with debugger (F9). Wait a minute, debugger won't attach and show the error: *"Connection to Python debugger failed: Connection to the debugger script at 127.0.0.1:55522 timed out"*
