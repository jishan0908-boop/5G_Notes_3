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

## Flow Diagram NSSI Resource Allocation Optimization :
![nssi](https://github.com/user-attachments/assets/d437df72-ca23-4a52-84e4-ad738ce95a00)

1. For each NSSI , KPI or the performace data is collected from the E2 node to the NonRT RIC , then the Non RT RIC analysis this data , to train the AI/ML model and then it is used to predict data what will be the traffic demand in future for NSSI for diff time and location . Based upon these prediction the NSSI resources are updated , then the Non RT RIC updates the E2 nodes by the O1 interface and at the same time we need to update the O-cloud , so non-RT RIC contact the SMO inorder to update this O-CLOUD resources and then this SMO sends this request of O-Cloud management and operation to updated he O-cloud resource , then the O-Cloud management and operation send the O-cloud over the O2 interface inorder to scale in/out these resources


## Use Case Flight Path Based Dynamic UAV Radio Resource Allocation:
![uav ](https://github.com/user-attachments/assets/13c2f837-352a-4250-8ef8-934d8fbda3b9)

On the grounds things are simple like O-RU provide coverage to a cell , normally for a UE the closet BS is the Best server , which provide the best coverage .
At the level of the UAV the slide lobes of the beamfroming by the basestations are visible to UAV ao we will not have a continouse coverage areaas we see on the ground , so the coverage is not continues . As a result there is the degradation of KPIs du to the uplink interferbce  the basestation antenna side lobes due to the certain drop in signal strength because the coverage or the altitude is ont continues .

##   Flow Diagram Flight Path Based Dynamic UAV Radio Resource Allocation :
![uav flow](https://github.com/user-attachments/assets/b635648b-99d0-4acf-a6e5-0198ddb8f20b)

The nonRT RIC is reciveing the information the Network Nodes by the O1 connector and it also reciving the information form the Application server useing these two types of information , it is traing the AI/ML models and it is deploying this models in the near RT RIC and near RT RIC also reciving the Enrichmenet information the infpormation that the Non RT RIC is recivig from the application server and the non RT RIC sending the additional resource policies for the UAV to the near RT RIC based upon this information the near RT RIC updates the configuration of the basestation resources for the optimal coverage for the UAV , same time the non RT RIC is collecting informtion form the network nodes and evaluating the perfromance of the UAV or it may retrain the AI/ML model for the optimal coverage of the UAV.

## Use Case 5G Massive MIMO Beamforming Optimization :
![mimo](https://github.com/user-attachments/assets/3da74572-5df5-41c3-a08a-343be7abb002)

In the case of 5G we know we uses the beamforming to increase the SINR the throughput of the UE these beamforming can be based uponb the codebook as in the case we using the frequency devient Duplexing or it can be non-codebook based when we are using the time devient Duplexing and normally we have the Grid Of Beam that is serving different UE in the case of intial acces the grid of beam is used in with the beam sweeping . 

Now the codebook and the GoB deteremine that what will be the horizontal and vertical beam width of these beams , what would be the coverge area these beams are covering and what would be the shape of the cells.

Inorder to provide coverage to a cell different vendors use different number of beams, different horizonatl and vertical beam width and different azimuth(horizontal angle) and downtilt(angle with the horizonatal axis) range for these beams.
In the case of multi-vendors scenario when we are using the basestaion form different vendors we need to optimize the beamforming , also optimize the transmit power and physical resource Blocks need to be allocated , so for these optimization we need centralized monitoring and control to the beamfroming and this can easisly be provided by the O-RAN .

If we not do the beamforming optimization for the massive mimo , then in traditional mimo have to suffer , because of the non-harmoniousation b/w the beamsin the neighbouring cells there may be problems like , high inter cell-interference , unbalanced traffic b/w neighbouring cells, the low performance of the cell edge users because of the interfernce and coverage gap and the poor handover performance .

## Massive MIMO Beamforming Optimization Procedure :

The data that is used for the Beamforming Optimization like the cell site information like location of a cell site, inter site distance b/w these cell site and the basestation configuration like the operating frequency that is used by each basestation , bandwidth that is used by each basestation, frame structure that is used by each basestation, transmite power of each basestation and the beam configuration that is horizontal and vertical beamwidth azimuth(horizontal angle) and downtilt(angle with the horizonatal axis) of these beams in each cell .

This measurement data is collected in SMO through the O1 interface ,  then the non RT RIC uses this data to train the AI/ML models .
AI/ML than predict the beam configuration and then the SMO sends this beam configuration through the O1 interface to the E2 NODES and this configuration includes horizontal/ vertical beam width , beam azimuth and downtilt, max and average transmit power per beam the latency of the non RT RIC is greater than 1s so the configuration decision can be taken with the time resilance greater than 1s so these decision can easily be done in non RT RIC and we do not need to invole the Near RT RIC.





























































