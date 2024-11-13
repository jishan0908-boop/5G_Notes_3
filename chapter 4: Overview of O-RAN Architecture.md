## Difference Between Open RAN and O-RAN :
![1](https://github.com/user-attachments/assets/4bbe28ff-ac5d-4852-955c-0c4a35624404)
![2](https://github.com/user-attachments/assets/2870b830-f062-4342-a83a-94e0d1b8889e)


## Control Plane & User Plane Dis-aggregation in O-RAN :
* In the O-RAN the O-DU is divided into CP& UP .
![3](https://github.com/user-attachments/assets/962de469-ad21-44ba-a4c4-f19394c9deba)
## Entities & Interfaces Introduced in O-RAN Alliance Architecture Function :
![4 q](https://github.com/user-attachments/assets/c1d661f1-ddbc-4081-87d5-47ca6cbe7ae5)

* Service Management and Orchestration (SMO):
* The O-DU & O-CU-CP & O-CU-UP are deloyed on the cloud , so in other to manage these enitiy on the cloud we use SMO entity it has interface O2 with the cloud in order to manage and configured the O-cloud and it also have interface O1 , in order to configure and manage the other entities . O1 interface is also use in the collection of key performance indicators (KPIS), form the RAN entities eg of block call rate , drop call rate these KPSI are collected by the O1 . This O1 interface also used to collect the configured data like how many slices are  there in the RAN .
*  SMO has another interface with the O-RU , which is Open Fronthaul M-Plane interface , this interface used by the SMO to manage the fronthaul of O-RU & O-DU
![4 2](https://github.com/user-attachments/assets/e1e3b159-c960-44dd-b8c2-dbfce5af7276)

*  RAN Intelligent Controller (RIC):
*  RIC is responsbile for the controlling and optimizing RAN functions, it also has two parts :
*  Non-Realtime RIC(NON-RT RIC): It is inside the SMO , it is responsbile for making the policies for the controlling and optimizing RAN functions , these policies are be derived form expert knowledge or may be derived form the AI/ML on the KPIS that have been collected in the SMO . This RIC sends the policies inform the A1 interface to the Near Real Time RIC.
*  Near Real Time RIC (nRT RIC): It has the policies also , it get the feedbacks form the O-RAN nodes using the E2 interface , using the poloices and feedbacks , send the Directives to these nodes by the E2 interface inorder to controlling and optimizing RAN functions, these E2 is also used to collect the Fine Grain or the real time KPIS from the O-RAN network 
![4 3](https://github.com/user-attachments/assets/de6eb87d-a0f9-45fd-8edc-07415bc3424d)
* Then we have the 3rd party apps that are used to managed the O-RAN functions there are two such apps , rApp which works on the Non-Realtime RIC they work independently because of the open interface b/w apps and Non-Realtime RIC .
* Then we have the xApps, they are deployed on the Near Real Time RIC and using the open interface b/w the Near Real Time RIC and xapp they communicate one another .

## Options For Aggregation of O-RAN Nodes :
![5 1](https://github.com/user-attachments/assets/416e59bb-1165-4c2c-b3e9-b8017dbbb26a)

![5 2](https://github.com/user-attachments/assets/c82f83c5-6d0d-4094-b596-60e947f5c07d)

![5 3](https://github.com/user-attachments/assets/d5a3b3a3-c6a9-4cd5-b481-0c46a8652f85)

![5 4](https://github.com/user-attachments/assets/8dc0add4-d0fa-4657-a9b7-a6d0ea7cbe2e)

## O-RAN Control Loops :
![6](https://github.com/user-attachments/assets/d0f8a385-cdc3-4bad-a362-b649b8d1b9c6)

 * These loops operates at the three level , first we have real time loops that operates at the level of nodes and these loops must execute within 10ms due to the real time nature of loops .
 * Then we have the near real time loops these loops can execute b/w 10-100ms .
 * Then we have the non real time loops , these loops can execute greater than 1s .
 * According to the O-RAN specification these real time loops execute within 10ms , while the execution time of other two loops depends upon specific use case for which these loops are being loops
 * These loops are based upon the action feedbacks like if the basestation is using the beamforming and it is steering the beams in the particular direction so this basestaion performs connection and then it gets the feedbacks analytics baseupon it this base station modifies its action .
 * All these loops run parallel to one-another or these loops may or may not interact with each depending upon the use case .

## Major Entities in O-RAN Ecosystems :
![7](https://github.com/user-attachments/assets/f977175a-ec13-4d73-93d5-17e204fa981a)
* The O-RAN Alliances considers those specificsation to the baseline specification , and O-RAN Aalliance build upon those specification inorder to define the Architecture and Specification or O-RAN .
* Then we have the O-RAN Software Community , which is working under the Linux Foundation and it works with the collaboration of O-RAN Alliances and it is involve in the refernence design for whole O-RAN software
* Then we have Software Defined (SD) - RAN , this project is under the Open Networking Foundation , as apart of this project there is a project micor-ONOS-RIC , in this project and  open source RIC example platform being develop .
* Then we have the Telecom Infra Project which is founded by the facebook , and it takes the micor-ONOS-RIC platform and it test different xAPP on that platform and this project is also invole in the implementation of the RAN on the COTS hardware 




























