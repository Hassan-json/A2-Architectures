### What is the difference between latency and throughput? ###

Latency is the time required to perform some action or to produce some result. Latency is measured in units of time -- hours, minutes, seconds, nanoseconds or clock periods. Throughput is the number of such actions executed or results produced per unit of time.
What would you design a AP or a CP System?
### What would you design a AP or a CP System? ###

![AP and CP](https://raw.githubusercontent.com/Hassan-json/A2-Architectures/master/images/CAP-theorem-with-databases-that-choose-CA-CP-and-AP.png)

### What is replication, failover and how does Redis replication work? ###

- Redis implements replication in two ways
	- With a single shard that contains all of the cluster's data in each node—Redis (cluster mode disabled)
	- With data partitioned across up to 90 shards—Redis (cluster mode enabled)                  
- Each shard in a replication group has a single read/write primary node and up to 5 read-only replica nodes. You can create a cluster with higher number of shards and lower number of replicas totaling up to 90 nodes per cluster. This cluster configuration can range from 90 shards and 0 replicas to 15 shards and 5 replicas, which is the maximum number of replicas allowed.

### What would be the perfect database / database model for your SWT PET project if you would have to scale large and having some 10.000 clients? ### 

The MongoDB NoSQL database can underpin many Big Data systems, not only as a real-time, operational data store but in offline capacities as well. With MongoDB, organizations are serving more data, more users, more insight with greater ease — and creating more value worldwide.

### What are the advantages and disadvanteges of (web) caching? ###

First, stale data; this means that when you use cached content/data you are at risk of presenting old data that's no longer relevant to the new situation. If you've cached a query of products, but in the mean time the product manager has delete four products, the users will get listings to products that don't exists. There's a great deal of complexity in figuring out how to deal with this, but mostly it's about creating hashes/identifiers for caches that mean something to the state of the data in the cache, or business logic that resets the cache (or updates, or appends) with the new data bits. This is a complicated field, and depends very much on your requirements.

Then overhead is all the business logic you use to make sure your data is somewhere between being fast and being stale, which lead to complexity, and complexity leads to more code that you need to maintain and understand. You'll easily lose oversight of where data exists in the caching complex, at what level, and how to fix the stale data if you get it. It can easily get out of hand, so instead of doing caching on complex logic you revert to simple timestamps, and just say that a query is cached for a minute or so, and hope for the best (which, admittedly, can be quite effective and not too crazy). You could give your cache life-times (say, it will live X minutes in the cache) vs. access (it will live for 10 requests) vs. timed (it will live until 10pm) and variations thereof. The more variation, the more complexity, of course.

### What is the difference between RPC and Rest? ###

RPC-based APIs are great for actions (that is, procedures or commands).

REST-based APIs are great for modeling your domain (that is, resources or entities), making CRUD (create, read, update, delete) available for all of your data.

REST is not only CRUD, but things are done through mainly CRUD-based operations. REST will use HTTP methods such as GET, POST, PUT, DELETE, OPTIONS and, hopefully, PATCH to provide semantic meaning for the intention of the action being taken.

RPC, however, would not do that. Most use only GET and POST, with GET being used to fetch information and POST being used for everything else. It is common to see RPC APIs using something like POST /deleteFoo, with a body of { “id”: 1 }, instead of the REST approach, which would be DELETE /foos/1.

This is not an important difference; it’s simply an implementation detail. The biggest difference in my opinion is in how actions are handled. In RPC, you just have POST /doWhateverThingNow, and that’s rather clear. But with REST, using these CRUD-like operations can make you feel like REST is no good at handling anything other than CRUD.

Well, that is not entirely the case. Triggering actions can be done with either approach; but, in REST, that trigger can be thought of more like an aftereffect.

For example, if you want to “Send a message” to a user, RPC would be this: 

```
POST /SendUserMessage HTTP/1.1
Host: api.example.com
Content-Type: application/json

{"userId": 501, "message": "Hello!"}
```
But in REST, the same action would be this:

```
POST /users/501/messages HTTP/1.1
Host: api.example.com
Content-Type: application/json

{"message": "Hello!"}
```
### What is the difference between RPC and Rest? ###
### How many cores does the Stackoverflow Servers have, with what chip Hz and how many MB L2 cache? ### 

### GPU and TPU ###
Architecturally? Very different. A GPU is a processor in its own right, just one optimised for vectorised numerical code; GPUs are the spiritual successor of the classic Cray supercomputers. A TPU is a coprocessor, it cannot execute code in its own right, all code execution takes place on the CPU which just feeds a stream of microoperations to the TPUHello World with Google Colab using Python language running on GPU. 

You can write your code with Google Colab will run on GPU / TPU, take a look. 

![Hello World](https://raw.githubusercontent.com/Hassan-json/A2-Architectures/master/images/Capture.PNG)
