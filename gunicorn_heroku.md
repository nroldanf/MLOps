# Deploy ML with Gunicorn, Flask and Heroku

## WSGI (Web Server Gateway Interface)

Standard interface which allows to separate server code from application code.

### Limitations of WSGI

- Does not have the ability to deal with __Websockets__.
- Takes a single request and return a response at a time. Synchronous calls, Can't use __async/await__
- Can't work with __HTTP/2__ (HTTP2 can encapsulate all messages in binary format maintining semantics, verbs, etc.)

WSGI frameworks:

- Bottle
- Flask
- Djando

WSGI Servers:

- Gunicorn
- uWSGI
- Apache

## ASGI (Asynchronous Server Gateway Interface)

Asynchronous web framework standard.

Client sends a message to the server, in the meantime, can go and do other stuff. When the server returns the response, the client knows what to do and handles it.

### Advantages of ASGI

- All calls are asynchronous by default. Allows __multiple incoming events and outgoing events__ for each application.
- Allows background coroutine so the application is able to do other things. WSGI back compatibility implementation.

__Async__ frameworks:

- aiohttp and asyncio (client/server) - async requests
- blacksheep

ASGI frameworks:

- FastAPI
- Quart (most Flask-like)
- Starlette (used by FastAPI)
- responder

ASGI Servers:

- Uvicorn (used by starlette)
- Mangum (use ASGI applications with AWS Lambda and API Gateway - serverless), compatible with FastAPI, Quart and Starlette.
Works with Serverless Framework and AWS SAM.
- Daphne
- Hypercorn

## Gunicorn

Ligth-weight WSGI server that works well with Flask.

Can use multiple threads to handle load balancing and can perform additional server configuration that is not available when using only Flask.
