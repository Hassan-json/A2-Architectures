### A2-Architectures ###

### What is the difference between latency and throughput? ###

Latency is the time required to perform some action or to produce some result. Latency is measured in units of time -- hours, minutes, seconds, nanoseconds or clock periods. Throughput is the number of such actions executed or results produced per unit of time.
What would you design a AP or a CP System?

### What is replication, failover and how does Redis replication work? ###

- Redis implements replication in two ways
	- With a single shard that contains all of the cluster's data in each node—Redis (cluster mode disabled)
	- With data partitioned across up to 90 shards—Redis (cluster mode enabled)                  
- Each shard in a replication group has a single read/write primary node and up to 5 read-only replica nodes. You can create a cluster with higher number of shards and lower number of replicas totaling up to 90 nodes per cluster. This cluster configuration can range from 90 shards and 0 replicas to 15 shards and 5 replicas, which is the maximum number of replicas allowed.




### GPU and TPU ###
Architecturally? Very different. A GPU is a processor in its own right, just one optimised for vectorised numerical code; GPUs are the spiritual successor of the classic Cray supercomputers. A TPU is a coprocessor, it cannot execute code in its own right, all code execution takes place on the CPU which just feeds a stream of microoperations to the TPUHello World with Google Colab using Python language running on GPU. 

You can write your code with Google Colab will run on GPU / TPU, take a look. 

![Hello World](https://raw.githubusercontent.com/Hassan-json/A2-Architectures/master/images/Capture.PNG)
