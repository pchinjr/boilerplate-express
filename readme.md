# Backend Challenges Boilerplate - Basic Express

experimental serverless deploy

Using Architect (arc.codes), move entire app into `get-index`, this is not suggested best practice if total payload is over 5MB, but showing proof of concept. In order to do it, I moved `server.js` into `get-index/index.js` and running the Express instance with `@architect/functions` helper method, `arc.http.express()`. The port is set manually to `3000` to allow the FCC tester access to the underlying server.

So to review: This is a mega Lambda function, with 2 express instances running in it. The main process is for FCC to test against, and the second is the app that it is testing. Wild. 