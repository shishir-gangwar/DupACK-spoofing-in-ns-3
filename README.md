# Implement Duplicate Acknowledgement (DupACK) spoofing in ns-3
## Course Code: CO300
## Assignment: #35
### Overview

DupACK spoofing is an attack where the receiver floods the sender with duplicate
ACKs. This ensures that the receiver recovers quickly after the congestion window has been
reduced to half.

### References

[1] TCP Congestion Control with a Misbehaving Receiver ( https://cseweb.ucsd.edu/~savage/papers/CCR99.pdf )

[2]TCP models in ns-3: https://www.nsnam.org/docs/models/html/tcp.html