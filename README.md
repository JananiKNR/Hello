# This is a Test

## <a id="index"></a>Index

* [BPDU]( #bpdu )
* [Convergence]( #convergence )
* [STP]( #stp )

[Back]( #index )

---

## <a id="bpdu"></a>BPDU
[BPDU]: #bpdu

Bridge Protocol Data Unit are frames that contain informaiton about Spanning
tree protocol([STP]). Switches send BPDUs using a unique MAC address form it't
__original port__ and a multicast address as destination MAC __(01:80:C2:00:00:00)__ or
(01:00:0C:CC:CC:CD for Pre VLAN Spanning Tree)

There are three kind of BPDU's:
* Configuration BPDU, used by Spanning tree protocol to provide information to
  all switches.
* TCN (Topology Change Network), tell about changes in topology.
* TCA (Topology Change Acknowledgement), confirm the reception of TCN.

By default the BPDUs are sent every 2 seconds.

If any change occur in the layer2 network, such as when a link goes down, a new
link is added, a new switch is added, or a switch fails, the switchs share this
information by transmitting BPDU's, causing the STP algorithm to be re-executed
and a new loop-free technology is then created. STP and BPUD's speed up
[convergence].

[Back]( #index )

---


## <a id="convergence"></a>Convergence
[Convergence]: #convergence

Convergence is a term used in networking to describe the amount of time it takes
to deal with changes and get the network back up and running. The default BPSU's
advertisement time of 2 seconds allows changes to be quickly shared with all the
other switches in the network, reducing the amount of downtime any disruption
would create.

[Back]( #index )

---


## <a id="stp"></a>STP
[STP]: #stp

For Spannig Tree Protocol to function, the switches need to share the
information about themselves and their connections. What they share are
[BPDU]'s. BPDU's are sent as multicast frames to which only other layer 2
switches and bridges are listening. If any loop (multiple possible paths between
switches) are found in the network topology, the switches will cooperate to
disable a port or ports to ensure that there are no loops; that is, from one
device to any other device in the layer 2 network, only one path can be taken.

[Back]( #index )

---

