# HTTP

HTTP works as a request-repsonse protocol between client and server.

### HTTP Methods
* get 
* post
* put
* head
* delete
* patch
* options

The two most common are `:get` and `:post`.

### :get
Is used to request data from a specified resource.
Requests can be:
* cached
* remained in the browser history
* bookmarked
* should never be used when dealting with sensistive data
* have length restrictions
* are only used to request data (not modify)


### :post
Is used to send data to a server to create/update a resource.
Requests:
* never cached
* do not remain in browser history
* cannot be bookmarked
* have no restrictions on data length

