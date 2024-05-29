# refactored-chainsaw

Random thoughts about concurrency in java, python and beyond

I am supposed to give short talk on concurrency in java and python, and that seem to be canceled or postponed not sure. But I already did research so I decided to capture it here anyway. If I have tt do that talk on later date I will have this to start with.

Some definitions to start:

Concurrency - the ability of program to handle multiple tasks simultaneously.

Parallelism - (according to wikipedia Parallel computing article) is a type of computation in which many calculations or processes are carried out simultaneously.

[Difference](https://stackoverflow.com/questions/1050222/what-is-the-difference-between-concurrency-and-parallelism) is subtle, but concurrency is what you want, Parallelism is one of the ways to achieve that.

Rob Pike is arguing if you have long task where you wait for some external operations. You have opportunity for concurrency, “just break up this long sequential task so that you can do something useful while you wait.”  

I first time I run into concurrency was  [Windows 1](https://en.wikipedia.org/wiki/Windows_1.0). It could run on [8088](https://en.wikipedia.org/wiki/Intel_8088) cpu not capable of parallel execution, yet it was able to handle multiple "windowed" applications at once. Applications have to [cooperate](https://en.wikipedia.org/wiki/Cooperative_multitasking) giving each other chance to run. Big downside of cooperative multitasking in windows that one misbehaving app could cripple whole system.

New CPUs was developed that allow [Preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)#PREEMPTIVE) multitasking, unlocking true parallel execution.

### multiprocessing

Multiprocessing is loaded term and here I will use in in-context of OS ability tu run multiple concurrent processes in a system. OS processes typically use separate processors to minimize context swithching.

### multithreading

(Wikipedia) multithreading is the ability of a CPU to provide multiple threads of execution. There are two common approaches for multi threading: parallel multithreading and concurrent multithreading.

### Compute Kernel (GPU)

Compute kernels roughly correspond to inner loops when implementing algorithms in traditional languages (except there is no implied sequential operation), or to code passed to internal iterators.




