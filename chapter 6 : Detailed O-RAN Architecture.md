## Service Management and Orchestration (SMO):
(pics)
* The O-DU , O-CU-CP/UP are virtulaized on O-cloud , SMO is an intelligent automation platform that is used to manage these entities on the cloud . It is invole in the automation and the Lifecycle of these entities , these SMO has the O1 interface with these entities , and it supports the FCAP operation.
* FCAPS is a abbreivation of 5 words :
* 1. F = Fault detection and correction , which means SMO use O1 to detect and coreect the faults in the entities .
  2. C = Configuration and Operation , which means SMO use O1 to configur and operate these entities .
  3. A = Accounting and the Billing of these entitis also done bu SMO .
  4. P = Also the Key performance indicator are collected by O1 interface and then they are assess by the SMO .
  5. S = Security assurance and the protection , of these entities are also assure by SMO .
   
(pics)
 * In order to manage O-Cloud , the SMO use O2 interface , and SMO also has the database which is used to collect the information , Storing the information from the another database to the SMO's database for any functionality like , any UAV uses the O-RU for the direction , so its destination in the external database , so SMO takes information from the that database and store it in it's database ,this called Enrichment information .
* Similarly the Key Performance Inddicator of the entites , are also collected by the SMO , and store in the database .
* SMO also has the AI/ML framework in order to run he analytics on these KPIS .
* Than we have the open fronthaul managemaent interface , this interface is used by the SMO , in order manage the open fronthaul b/w O-RU & O-DU.
 
## Non Real Time RIC (non-RT-RCI):
(PIUCS)
* It controls and Optimizes the O-RAN fxns , It does do by sending infromation through Real Time -RIC by the A1 interface .
* 1. Policy Based Guidance : It is the first information that non-RT-RCI sends . Inorder to guide the RT-RCI to optimize and control the fnxs , these policies may be dervied using the expert knowledge or by the AI/ML analytics on the database of the KIPS in the SMO . Also the policy is in the JSON formate .
  2. AI/ML Models: It is the second information that non-RT-RCI sends, that it has dervied by running the analytics in the database , it may sended to the RT-RCI . This model may be used by the xAPPS which are in  the RT-RIC , inorder to optimize and control the network .
  3. Enrichment Info : It is the third information send by the non-RT-RIC to RT-RIC , through the A1 interface , it is Enrichment Infomation , the information is any type of additional information that may be used by the RT-RIC for the resource Optimization , this information may be form the external server , it may the other information that may be dervied form the other network functions inside the network .

(pics )
*  The rAPPs are the third party apps that are used to add the Value Added Services (VAS) for the RAN optimization , they are deployed on the non-RT-RIC and it run inside the SMO .
*  Eg : A rAPP that is based upon the O1 measrurements, which is connected to the database of the SMO , , which may predect the future load, and may be the location of the UE in the future and what would be there Receieved power level based upon these predection the rAPP may provide policy guidance to the RT-RIC , also there may be the conflict , so to avoid that there is , non-RT-RIC .
*  These rAPPs operate at the very high level and they effect the large number of users and the large numbeer of the network nodes as compare to the xAPPs.

## JSON (JavaScript Object Notation):
(pics)
* The poilicies based guidance are which are send to RT-RIC by the non-RT-RIC are in the JSON formate . In the language of the json the empid is the name and it is followed by its value togethere these are called name-value pair .Also json object can be nested in one-another.

## A1 Policy Format and Examples:
(pics)
*  The poilicies based guidance are which are send to RT-RIC by the non-RT-RIC are called the A1-Policy because they are send on the A1 interface . There are three main attribute of this A1 policy .
*  1. Policy Identifier (PolicyID): It is the first attribute , it is the ID which is assigned by the non-RT-RIC .
   2. Scope ID :  It is the second attribute , which is the scope ID of the policy , this scope defines that whether the policy is valid for a particular cell , in that case we have the cellid , or it is valid for the singal UE in that case we have to give the UEID , or if it is valid for the groups of UEs in that case we have to give the groupid , or if this policy is valid for a particular slice in that case we have to give the sliceid or if this policy is valid for a particular Traffic type in that case we have to give the qosId which is related to that traffic type .
   3. Policy statement : It is the third attribute , it is the actual directive related to the policy that is send by the non-RT-RIC to the Near-RT-RIC , so that it can optimize and control of the performance of  the O-RAN .

 ### A1 Policy Examples:
 (pics)


 ## Near Real Time RIC:
 

 






















































