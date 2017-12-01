# Implemention of Duplicate Acknowledgement (DupACK) spoofing in ns-3

## Course Code: CO300

## Assignment: #35

### Overview
DupACK spoofing is an attack where the receiver floods the sender with duplicate ACKs. This ensures that the receiver recovers quickly after the congestion window has been reduced ​to ​half.

### References
[1] TCP Congestion Control ​with ​a Misbehaving Receiver (https://cseweb.ucsd.edu/~savage/papers/CCR99.pdf) ​
[2] TCP models in ns-3: https://www.nsnam.org/docs/models/html/tcp.html

### Team Members
* Saurabh Yadav 15CO145
* Shishir Gangwar 15CO147
* Prateek Kembhavi 15CO223

### Instructions for running DupAckSpoof.cc

1. Change directory to ns-3.27

   	`cd ns-3.27`

2. Configure the files in ns3

   	`./waf configure`

3. Run DupAckSpoof.cc in scratch folder by passing arguments for enabling the attack 
   and the number of dupAcks to be sent
   
   	`./waf --run "scratch/dupAckSpoof --dupAckSpoof=true --dcount=100"` 
	
				OR
				
   	`./waf --run "scratch/dupAckSpoof --dupAckSpoof=false"`
   
   NOTE: default value of dupAckSpoof=false , dcount=10 

4. Generate the graph after running both the commands above
   
	`xgraph SpoofEnabled SpoofDisabled`
