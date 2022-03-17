############# Elements of jMeter ############

(1) Thread group: Its a collection of thread. Thread represents real time single user access simulation to the system.

(2) Samplers: Samplers provide any kind of protocol (HTTP,FTP etc) to the thread according to the need.

(3) Listeners: It displays the result in any format(graph,chart,tree,logs etc)

(4) Configuration: It setup defaults and variables for later use by samplers.

(5) Assertions: Its a process where expected result can be verified with actual result for the request that has been
sent to the server. Popular assertion that has been used is response assertion. It can be used to add and compare 
patter strings against one or many values of server response.

############# Timers in jMeter ############### 

jMeter send request without any delay between samplers and listeners.
It will fail to give realistic results for real world user traffic experience on load and stress testing. 

Two commonly used timer: constant timer and uniform random timer.

(1) Constant timer takes constant delay time for every thread.

(2) In uniform random timer, delay time has been calculated based on two things, random delay max and constant delay offset. 
Equation to calculate random delay time is:
-> 0.X * random delay max + constant delay offset. Here, X = 0 to 99.

Some other type of timers are: gaussian random timer, BeanShell timer, BSF timer etc.

############# Logic Controller ##############
Logic controller handles the order of executing samplers and listeners.

Multiple type of logic controllers such as : 
If, switch, loop, forEach etc.

Loop controller defines the number of time to execute any samples or listeners.

############# Recording Controller ##############
1) Adding NonTestElement - http recording
2) Setting proxy on browser
3) Starting recording in different recording controller
4) starting scenario recording
5) stopped recording and saved