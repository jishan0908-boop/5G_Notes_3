## Difference Between Open RAN and O-RAN :
(PICS )
(pics )

## Control Plane & User Plane Dis-aggregation in O-RAN :
* In the O-RAN the O-DU is divided into CP& UP .
(PICs )

## Entities & Interfaces Introduced in O-RAN Alliance Architecture Function :
(pic)
* Service Management and Orchestration (SMO):
* The O-DU & O-CU-CP & O-CU-UP are deloyed on the cloud , so in other to manage these enitiy on the cloud we use SMO entity it has interface O2 with the cloud in order to manage and configured the O-cloud and it also have interface O1 , in order to configure and manage the other entities . O1 interface is also use in the collection of key performance indicators (KPIS), form the RAN entities eg of block call rate , drop call rate these KPSI are collected by the O1 . This O1 interface also used to collect the configured data like how many slices are  there in the RAN .
*  SMO has another interface with the O-RU , which is Open Fronthaul M-Plane interface , this interface used by the SMO to manage the fronthaul of O-RU & O-DU
(pics)
*  RAN Intelligent Controller (RIC):
*  RIC is responsbile for the controlling and optimizing RAN functions, it also has two parts :
*  Non-Realtime RIC(NON-RT RIC): It is inside the SMO , it is responsbile for making the policies for the controlling and optimizing RAN functions , these policies are be derived form expert knowledge or may be derived form the AI/ML on the KPIS that have been collected in the SMO . This RIC sends the policies inform the A1 interface to the Near Real Time RIC.
*  Near Real Time RIC (nRT RIC): It has the policies also , it get the feedbacks form the O-RAN nodes using the E2 interface , using the poloices and feedbacks , send the Directives to these nodes by the E2 interface inorder to controlling and optimizing RAN functions, these E2 is also used to collect the Fine Grain or the real time KPIS from the O-RAN network 
(Pics)
* Then we have the 3rd party apps that are used to managed the O-RAN functions there are 





























