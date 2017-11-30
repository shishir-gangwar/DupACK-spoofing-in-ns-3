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

### Instructions
This is ns-3-allinone.

If you have downloaded this in tarball release format, this directory contains some released ns-3 version, along with 3rd party components necessary to support all optional ns-3 features, such as Python bindings and the Network Animator.  In this case, just run the script build.py; all the components, plus ns-3 itself, will thus be built.  This directory also contains the bake build tool, which allows access to several additional modules including the Network Simulation Cradle, Direct Code Execution environment, and click and openflow extensions for ns-3.

If you have downloaded this from mercurial, the download.py script will download bake, netanim, pybindgen, and ns-3-dev.  The usage to use basic ns-3 (netanim and ns-3-dev) is to type:
./download.py
./build.py
and cd into ns-3-dev for further work.  Consult the bake documentation on how to use bake to access optional ns-3 components.

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
