Suitable for applications that require a *defined series of independent computations*. A component reads *streams* of data as input and produces a *stream* of data. 

### Components
- *Filters*: apply local transformations to input streams and perform incremental computations so output starts before all info is read
### Connectors
- *Pipes*: serve as communicators for streams, transmitting outputs of one filter to input of other. 
![[Pasted image 20241212174652.png]]


### Pipelines
Restrict topologies to linear sequence of filters

### Batch Sequential 
A degen case of pipeline architecture, where each filter processes all of its input data before producing any output. 

### Advantages
- easy to understand
- support reuse
- easily maintained and enhanced
- specialized analysis
- support concurrent execution
### Disadvantages
- not a good choice for systems with a lot of constant change. 
- loss of performance in writing the filters