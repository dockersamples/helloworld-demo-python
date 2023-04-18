# A Simple Hello World Python Demo 

Example used to demonstrate ```docker init``` CLI for a simple Hello World Python Program


## Run the application





You can simply use `python3 app.py` command.


This code defines a handler that responds to GET requests with the specified text and starts an HTTP server listening on port 8080. When you run the script, you can access the server at http://localhost:8080 and see the same message as the Python program.

Those commands will start a http server listening on port `8080` 
and if your request `http://localhost:8080` you'll see the following output: 
```shell
❯ curl http://localhost:8080

          ##         .
    ## ## ##        ==
 ## ## ## ## ##    ===
/"""""""""""""""""\___/ ===
{                       /  ===-
\______ O           __/
 \    \         __/
  \____\_______/


Hello from Docker!

```


