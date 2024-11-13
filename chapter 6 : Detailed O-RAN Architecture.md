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
(pics)
* The Near RT-RIC is used for the control/optimization of the RAN radio resources , like we can do Adimission control , Mobility management and the Interfereence Management etc.
* Ex of the Adimission Control : like there is UE which is in the coverage area of the O-RU base station, and UE want to use the data services of this base station , using the Admission control, we can resitrict the base staion , to provide a certain type of data services to this UE . For the other data services the UE may need to connect to other base station .
* ex of the Mobility Management : if the UEs are at the edge of a cell , and also there is load in this cell , by using the mobility management we can modify the handover parameters of this cell in such away that these UE , make handover to the other base station , this way we do load balancing in these cell .
* Ex of interface management :it mean that we can adjust the transmitting power or the beamforming of these base station in such a way that there is min interference b/w these base station .
* These Radio resource Functionality are inn the xAPPs, and these apps may be provided by the third party , these xapps may be based upon the microservices based architecture , these apps may use the AI/ML trained model and these apps use it to control and optimize the RAN fxns or the radio resources.
(pics)
* Messaging infrastructure , it is used for the communication b/w the xAPPs, and b/w the xAPPs and other functional blocks .
* Then we have the secuirty block , which provide the security to the xAPPs and to handle the security relate fxns to the xAPPs .
* Then we have the Conflict Mitigation block , it is possbile that two xAPPs can proceduce conflicting request , so these conflicts are resolved by the Conflict Mitigation block .
* Then we have the XAPP Subscription Management , these xapps need to register to the nearRT-RIC so they are register with the XAPP Subscription block , and it also used to provide Unified Data distribution to these apps .
* Now we also have the Database in the near-RT-RIC this database stores the data of the E2 Nodes also data of the xAPPs are stored in this database , and the Shared Data Layer is the interface b/w the database .
* Then we have the Management Services , which is used for the configuration , fault and performance management of the Near-RT-RIC block , these services are also used for the Life-Cycle management of xApps , if we want to debug error in these xapps then we logs , traces and the metrics collection for these xAPP, and store in the database.

## Centralized and Distributed Near-RT RIC :
### Centralized Near RT-RIC :
(pics)
* There are Multiple fxns are connceted to these Near-RT RIC with the help of E2 interface , also it collects the data from all these E2 nodes in the form of Key Perfromance Indicator and based upon these KPIS for different cells the near-RT-RIC takes the action to optimize the perfromance of these cell together .

### Distributed Near-RT RIC 
(pics)
* In this case we can see that One Near-RT-RIC is control one E2 node , these Near realtime RIC consist of one or more Logical Near-RT-RIC that are virtulaized on the same server . 





















































