# Implementation-of-DSRED-in-NS3
## Course Code: CS704
## Network Engineering
## Overview

Double Slope RED (DSRED) [1] is a variant of Random Early Detection (RED) [2] in which the packets are dropped aggressively only when average queue size and instantaneous queue size is greater than Maxth . This repository provides an implementation of DSRED in ns-3.26 [3]. 

## Simulating DSRED

To simulate DSRED algorithm, the attribute DSRED must be set to true, as shown below:

Config::SetDefault ("ns3::RedQueueDisc::DSRED", BooleanValue (true));

## DSRED Example

An example program for DSRED has been provided in

src/traffic-control/examples/red-vs-dsred.cc

and should be executed as

./waf --run "red-vs-DSRED --queueDiscType=DSRED"

./waf --run "red-vs-DSRED --queueDiscType=RED"

## References

[1] Bing Zheng and Mohammed Atiquzzaman (2004). DSRED: An Active Queue Management Scheme for Next Generation Networks.

[2] Floyd, S., & Jacobson, V. (1993). Random early detection gateways for congestion avoidance. IEEE/ACM Transactions on networking.

[3] https://www.nsnam.org/ns-3-26/
