## O-RAN Traffic Steering (TS) APP Example-Problem of Traditional:
![ts app exapnme](https://github.com/user-attachments/assets/fe5930a0-f8ff-4757-acd1-e7fc47b1d032)
* It already exsist perviously before the O-RAN in the UE , before O-RAN the base station monitor the UE and then information about these Monitor radio conditions were passed to the gNB then it pass to OMC in it the parameters of the cell were varied , where handover margins where changed , or the cell reselection parameter would be chnaged or the cell priorty would be changed so that UE syeer to the desire cells . The problem is that all the UE were treated same , in that case policies were not UE centric , but in the case of O-RAN we can make UE centric policy we have more fine grain control over the UE and the services they are using .

## O-RAN Traffic Steering (TS) App Example :
![advantades](https://github.com/user-attachments/assets/a9742225-960e-46a6-aa0a-a7d65612aa1c)
* Advantages of TS using O-RAN:
* We can make the traffic steering policies for the individual UE or for the group of UE's , and we can make these policies based upon the services that the UE is using ,and we can use the ML techniques to optimize these policies , thus we can Optimize the network and we can also optimize the UE perfromance at the same time.

## Required Data (KPI) collection for TS:
![kpis](https://github.com/user-attachments/assets/0154266a-8424-4b3e-b14e-37b7a69620ba)
* 1. Measurement report : This  reports are genrated by the ue , the UE measures the power that it recives from the current base station ,as well as the power reciving form the neighbouing base station and the recives power is called RSRP , and these information are send to the current base station from basestation it goes to the SMO , the UE also measures the quality of the signals reciveing from its basestation and this measurement is called RSRQ then it is send to the basestation then to SMO using the O1 interfaces.
  2. Handover Statistics  like the ping-pong effect , when the UE is at the edge of the cell then it back-forth to the current and the target basestation , the switching back-forth is called ping-pong effect , which is not a good thing . Then we have failed handover statistics , then these information sends to the basestation then to SMO.
  3. Cell load : that how much load is there on the cell then these information sends to the basestation.
  4. UE services stats, type of services the UE is using and with what QoS they are using these services then these information sends to the basestation then to SMO.
* These information are also collected by the Near-RT-RIC by the E2 interface , however the KPIs that are collected by the near-RT-RIC they are real time KPIs that means that are collected at much faster frequency , while the KPIs that are collected by the SMO with the O1 interface they are collected at much lower frequency these KPIs are average for a longer duration .


## Role of NON-RT RIC in TS  :
![role non rt rics](https://github.com/user-attachments/assets/9ab9dcdc-fe47-4a45-83eb-786cbf71a903)
* The non-RT RIC makes the policies then it is send to the xapp in the near RT RIC that is used in the Traffic Steering , the non RT RIC also sends the Enrichment information to near RT RIC , and these information may be genrated using the statistical analysis , like measurment of RSRP/RSRQ in a cell ,these measerement are collected in the data base , and the NON-RT RIC may run the analytic to genrate the RF fingerprint it is the coverage map of the cell in terms of power and quality .
* The KPIs that are collected in the SMO the nonRT RIC also send KPIs that need to be collected in the database and alos with what frequency that it connect to the O2 interface .

## Role OF Near RT RIC:
![near rt ric](https://github.com/user-attachments/assets/ff33a737-a328-4a47-97f6-a7a2f6cf0bc5)
* The near RT-RIC recives policies from the non RT RIC and it implement that policies , it also use the enrichmenet information that it recives from the Non RT RIC like the RF fingerprint which is the coverage and quality map of the cell by using these both information Near RT RIC decides what is the best cell for a UE or for the services of the UE .
* Inorder to implenment these policy the near RT RIC then send the control messages to E2 node , inorder to handover execute or set the primary or the secondary Cell selection .

## Role OF E2-Node :
![E2 node](https://github.com/user-attachments/assets/09727d23-6afd-4343-84e7-8f10f0534251)
* Once these E2 nodes recives these control messages they execute these messages , these E2 nodes also collected the real time KIPs , then these real time KIPs are send to near RT RIC by the E2 interface , based upon these real time KIPs the near RT-RIC assess or execute or modify its action .

## TS Scenario Example :
![example od ts](https://github.com/user-attachments/assets/8ff6bf2f-d36c-4c84-a2cf-fe33bde932df)
* In this example we have two gNB , gNB A and gNB B , with there specification limits or capacity .
* Like gNBA has low frequency , low bandwidth and low latency
* gNB B has high frequency , high bandwidth and high latency
* The UE is in the edge of both the gNBs and it is using two services ,
* Voice Connection services of 5G Quality of Services Identifier is  1 and Data services of 5G Quality of Services Identifier is 9.
* The UE use the data services from the gNB B where there is high frequency and the voice connection service form the gNB A where , frequency is low which is more reliable and it is using FDD , which means there is very less latency .
![example 2 ](https://github.com/user-attachments/assets/da46a3fd-7905-487a-8259-7d8409b9019f)
* Once these policies are recived by the Near RT RIC these policies would be implemented by the xAPPs and the xAPPs sends the control messagee to the E2 Nodes of the two gNB these control mssg says that cell A provide the voice connection services 1 and cell B will provide the eMBB enhanced Mobile Broadband service .
* Once these msg are recived by the E2 Nodes of the two cells then they implement these two msges .





































































