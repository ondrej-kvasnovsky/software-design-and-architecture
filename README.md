# Software Design and Architecture

When we are developing a software system, we need to implement _functional requirements_. But we also need to think about _non-functional requirements_: 

* _reliable_ - so it works even when there are errors
* _stable_ or _performant_ - so it handles specified load of data and requests
* _maintainable_ - low complexity, easy to operate

### Reliability, Scalability and Maintainability

The main goal is to make software that is reliable, scalable and maintainable. _Reliable_ system works correctly even there are hardware, software or human errors. _Scalable_ systems can deal with growth of data, traffic or complexity. _Maintainable_ systems enable engineering and operations to fix issues or add new features in productive manner.

### Intensity

We can think about intensity of applications from compute or data point of view.

_Compute intensive_ applications need to be able to use all available CPU power and thus it is crucial to distribute tasks in the most efficient way.

_Data intensive_ applications need to be able to store and access data in the most efficient way. We use databases, caches, search indexes and stream or batch processing to manipulate the data.

### Performance

When system grows, we need to be able to describe the load. The load can be described with load parameters. Load parameters are ration of read and writes in a database, number of simultaneously active connections, hit cache rate or something else.

Also, we need to have clear understanding of these terms:

* _Response time_ - is what client experiences
* _Service time_ - actual time to process the request
* _Latency_ - duration that request is waiting to be handled
* _Tail latencies_ - requests that take most of time and are e.g. 99.99th percentile, so 1 of 10 000
* _Head of line blocking_ - slow request that slow down other requests

When measuring performance, the test client needs to send request independently of response times. 

What can be done when performance is bad: 

* _scaling up_ - vertical scaling, moving to more powerful machine
* _scaling out_ - horizontal scaling, distributing load to more machines \(doable with share-nothing architecture\). Often used on elastic systems, that can add machines as the load increases.

### Maintainance

Maintenance includes bug fixing, keeping the system operating, investigating failures, adapting new platforms and technologies, paying technical debt and adding new features. 

Usually, we spend more money on maintainance then on initial development of a product. That means we need to think about: 

* _operability_ - make it easy to operate the system, to keep it running smoothly, includes monitoring, logging, keeping systems and platforms up to date, predicting future problems, automation
* _simplicity_ - make it easy to understand for new engineers, avoid complexity
* _evolvability_ - make it easy to change the system in future











 



