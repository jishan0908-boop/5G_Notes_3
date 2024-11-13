## What is Network Slics? 
()
* Like we have a Physical 5G Network and on this network we can have many logical network and these logical network are called Network Slice . Each of these slices are the seprate network in itself that has all the necessary resources , they are isolated with each other but may share there resources with each other , the user is using the slice services it  will experience that it is using a complete separate network , the resource use in the slice can may be increase/decrease on the demands. 

## Examples of the Network Slicing in 5G :
( )
The Slices above are called as the Network Slice Instances , and the function that are used in these slices like SMF , NRF PCF are the virtualized fxns that means that we can genrate there instances using the Network function Virtualization .The above three slices have common NSSF and UDM .


## Single Network Slice Selection Assistance Information (S-NSSAI):
( )
A Network Slice Instance is identified using the S-NSSAI , and it has two parts:
1. Slice/Service Type and it is of 8 bits .
2. Slice Differentiator and it is of 24 bits it is used to differentiate any slice which is given to two different UE so there we use slice differentiator.


## Network Slice Subnet Instance (NSSI):
()
A network Slice Instance is further compose of network slice subnet instance .
A NSSI may contain one or multiple virtualized network functions, the NSSI may consist of network function or other NSSIs , they may be shared b/w two or more Network Slice Instances , it may contain the Network Functions of the core network or the access network or both .

## Network Slicing Management Model CSMF , NSMF , NSSMF  :
()
Here is a customer which is using the communication service , and this communication service is provided by the communication service provider and this service is based upon the network slicing , and this communication service provider uses the services of the Network slice Provider , it is the network operator and it is using the services of the Network Slice Subnet Provider it can be the same network operator of the different network operator .

The user gives it requirement to use the communication services ,to the communication service provider , then it uses the Communication Service Management Function (CSMF) to translte these requirement into the requirements of network slice going to be used inorder to provide this services.
Requirements are:
* Network Type
* Network Capacity
* QoS requirements
That would be used for this network slice .

 Then these requirement are then given to the Network Service Provider it takes the requirement and it has the Network Slice Management Function (NSMF) it is used for the overall management of this Network Slice Instance . The Network Slice Provider uses the Network Slice management dfunction inorder to translate the requirement into the requirement of the Network Slice Subnet Function and it gives these requirement to the Network Slice Subnet Provider.

 Now the Network Slice subnet Provider takes these requirement and it uses the Network Slice Subnet Management Function inorder to manage the network slice subnet according to the given requirements.

 ## Network Slice Template (NST):
 A network slice template is list all the necessary attributes of network slice like what are the resources required for a network slice .
 If there is a existing Network Slice template that meets to the customers requirement i.e we can use the template as it is or we can do some updation or can be scaled as per the customers requirement.

 ## Open Network Automation Platform (ONAP) Architecture :
 The network slicing in the O-RAN can be achived using the Open Network Automation Platform, it is a open source software platform that can be used to create , design and manage services like network slicing services .
 And these services are created by the virtualization , by using the virtual network function and the networking function that are achive by using the Software-Defined Networking (SDN).

 This ONAP Architecture has two main components:
 1. Design-time Environment
 2. Run-time Enciornement

(pics)
### Design-time Environment
It consists of the function and the libraries that are required inorder to develop new services .
The main part of this environment is the :
* Service Design Creation (SDC) : this is visual tool that can used in order to desgine and model the assests that are used in the ONAP components.
(pivcs)
### Run-Time Environment
It is used for the execution of the policies and the rules that are prepared using the Design-time Environment.
And in the context of Network Slicing there are two important function :
1. Active and Available Inventory(A& AI) which is a database of all the available resources and the services that are there in the network and the relation b/w those services and resources .
2. Services Orchestrator (SO) is used for the automation of the end-to-end services and instance provisioning of these services . 

































