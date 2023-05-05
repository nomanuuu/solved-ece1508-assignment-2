Download Link: https://assignmentchef.com/product/solved-ece1508-assignment-2
<br>
In this assignment you will write a controller application using ONOS’s REST API. You can use C/C++, Java, Python or Bash (right now we have these four in the testing environment; if there is a compelling need to use any other language then please consult with the TA) for completing the assignment. The application will proactively setup a bi-directional path between a pair of hosts, monitor the network topology, and re-setup the path if any link on the existing path fails. In other words, the application behaves in a way similar to a host-based intent.




<h1>Description</h1>

The application will take exactly two command line arguments. The arguments represent a pair of host identifiers (the identifiers will be the same as the one from running hosts command in ONOS). Once the application starts, it will use ONOS’s REST API to obtain the network topology, find shortest path between the specified pair of hosts and install flow rules in the switches to setup a bi-directional path between the hosts. Then, the application will periodically (every 5 second) monitor the port status of the switches along the path. If any link goes down on the path then the application will recompute a new path between the specified pair of hosts, remove old flow entries from the switches, and install new flow rules on the appropriate switches to re-establish the bii-directional path between the specified host pair. You can assume that no no forwarding application will be loaded as part of ONOS controller during testing, <em>i.e.</em>​, there is no other way of setting up a path other than using your application. You can assume the following applications will be loaded during testing: ​<strong>hostprovider, lldpprovider, </strong>​and<strong> openflow-base</strong>.​





