# Distributed-API-first-
A distributed system including a central API and a Worker but currently no client.

I made this project at the age of 15. 

It is currently including two solutions. 

One of them is a central API (it has Scalar installed. To access its UI add /scalar to the link).
It recieves new jobs,
gives a job to a requesting Worker,
recieves updates/heartbeats from a Worker,
recieves the result of the job by a Worker,
posts all information about a job (job id required),
it queues the jobs in a concurrent queue, 
it saves the queue and jobs to a local file in the bin folder so the data isn't lost on a crash/take down,

The second solution is the Worker.
It requests the jobs,
works on the job (in this project just a simulation with a delay and the input gets turned around e.g.: abc -> cba),
posts the job result to the API,
posts updates/heartbeats to the API.
