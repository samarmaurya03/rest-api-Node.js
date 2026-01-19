


<div style="height: 150px"></div>

# Basic Redis Caching Demo

This app returns the number of repositories a Github account has. When you first search for an account, the server calls Github's API to return the response. This can take 100s of milliseconds. The server then adds the details of this slow response to Redis for future requests. When you search again, the next response comes directly from Redis cache instead of calling Github. The responses are usually returned in a millisecond or so making it blazing fast.
