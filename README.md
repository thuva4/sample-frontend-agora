### Running

sbt run
```

Play will start up on the HTTP port at http://localhost:9000/.
You don't need to reploy or reload anything -- changing any source code while the server is running will automatically recompile and hot-reload the application on the next HTTP request. 

### Usage

If you call the same URL from the command line, you’ll see JSON. Using httpie, we can execute the command:

```
http --verbose http://localhost:9000/v1/posts
```

and get back:

```
GET /v1/posts HTTP/1.1
```

Likewise, you can also send a POST directly as JSON:

```
http --verbose POST http://localhost:9000/v1/posts title="hello" body="world"
```

and get:

```
POST /v1/posts HTTP/1.1
```
