## Use Case NSSI Resource Allocation Optimization :
A network slice instance hav different usage patterns like different times , different location , we have different UE and the different types of Applications.

eg most of the IoT runs during the of-peak hours or during the weekends 

eg for certain Special events like sports game or concert , we know that the traffic demand at ceration times and location increases .

So the AI/ML models are used to predict the traffice demand per slice for different location and time .This AI/ML model trained using data 
collected form the O-RAN nodes and this data is collected form the days and weeks or months .

In this way O-RAN reallocates the network resources for the network slices before there is a change in the traffic demand

## NSSI Resource Allocation Optimization Procedure:

We know that a NSI is compose of NSSI , if we optimize the NSI it effects the NSSI , first-of-all the KPIS are collected to per NSSI via the O1 interface. The KPIs that are connected 
1. DLPRB Downlink Physical Resource Block tht are used for the data Traffic in the gNB .
2. ULPRB Uplink Physical Resource Block tht are used for the data Traffic in the gNB .
3. Average DL UE throughput in tht gNB.
4. Average UL UE throughput in that gNB .
5. Number of PDU session that were requesetd to setup in a gNB.
6. Number of PDU session that were successfully setup in a gNB.
7. Number of PDU session that were failed to setup in a gNB.

Now the KPIs data is now analyis and this data is used to train the AI/ML model, after that this model is used to predict for the NSSI that for a given time and location for this subnet what are the capacity resources , what are the VNF resources and what are the slice subnet attribiute  . The subnet resources are optimize by the reconfiguring these nodes, because of the reconfigration we have to update the O-cloud to , for that we use O-Cloud management and operation block this blocks updates the resources of O-Cloud with the help of O2 interface.

































































