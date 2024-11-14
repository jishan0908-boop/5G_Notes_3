# Traditional Basestation Architecture :
## Traditional Basestation :
* This Traditional Basestation was first introduce in 2G , then in 3G and in the earlier part of the 4G depolyment , the core network is connected to the base station ,where we have a cabinate where inside it we have the Baseband Unit and the Radio Unit , suppose if the core network is sending data to the base station , the data is not modulated , so we call the data as the baseband signal, so first this signal is process by the baseband unit , and it process it and it give it to radio unit it modulate the baseband signal to carrier band , then it sends it to the antenna through RF-cable , there was a porblem in RF cable that there is the significant powerloss in it .


 ## Evolution to the Contemporary Basestation:
 
![2 11](https://github.com/user-attachments/assets/198da82e-8986-462b-aaa6-07dd1bdaa0e7)

* Because of the loss of powers in RF cables in Traditional Basestation , we move to Contemporary Basestation , so in this case the Radio unit is moved form baseband unit to near the antenna know it is called as the Remote Radio Unit(RRU), and we have now optical fiber cables in the baseband unit , but in RRU it consist of Proprietary Hardware , and in the baseband unit we have the proprietary hardware which is running because of proprietary software.

![2 1](https://github.com/user-attachments/assets/37473499-7d0a-449a-8c1a-c213990f8004)

 * The connection b/w baseband unit and the remote radio unit , is called Fronthaul, which is based upon the opticafiber cable and the protocol is used is CPRI protocol (Common Public Radio Interface) , this connection b/w them is a proprietary interface , then we have the transmission link b/w Baseband unit and the Coe network , this is called as the Backhaul .

## Evolution to Virtualized RAN (vRAN):

* Then Contemporary Basestation evolves into Virtualized RAN , this is called so because the hardware and the software are decoupled , which does not use the proprietary hardware , rather we use the Commercial Off-The Shelf (COTS) server , which is much cheaper and it is easlily aviable to the evry vendors.
* All the fxn of the BBU , like hardware and software fxn are implemented in software, then these fxn are called Virtualized Baseband Unit Function, because of the Virtualized Layer these fxn runs on the same pods hardware .
* It is called Virtualized RAN because it is possbile to run the VBBU form different basestation on the same pods server using the , Virtualized layer , so in this way these fxn can run more efficently and they only use the resource that are required , we can call the Open RAN beacuse of the Fronthaul proprietary interface b/w BBU and RRU , and RRU hardware is also the proprietary hardware .

## From Virtualized RAN to Open RAN :

![2 2](https://github.com/user-attachments/assets/59fc96ec-6053-43bd-8ff9-3a65309bc4df)

* From Virtualized RAN towards the Open RAN , instead of using RRU proprietary hardware we use Software Defined Radio (SDR) and it is based upon the COTS . This SDR takes data from the BBU and modulates it into carrier frequency , and after wards it is transmitted through antenna.
*  Secondly the proprietarfy interface b/w BBU & RRU where also replaced by the Open Interface .

## Difference B/W Distributed RAN and the Centralized RAN:

![2 3](https://github.com/user-attachments/assets/b083b228-e1a7-4461-a0ad-6fa0d3b3ae31)

* In D-RAN the BBU are placed near to the antenna , while in the case of C-RAN the BBU are placed at the central loaction of the core network .
### D-RAN :
* As the data from the core network moves to BBU it processes that data and additional over head to the data , So the data rate Increases , and in the fronthaul , we use optical fiber cable, which supports high data rate and have low latency that means the fornthaul , it more expensive than the backhaul , but the BBU is near the antenna so the cost of fronthaul , is less .
### C-RAN:
* Since the BBU are placed at the central loaction near the core network , so the fornthaul is longer , so the cost of fronthaul is high .
* But this approach has advantages , like the pooing of the BBU always us the optimal shareing of BBU resources , which are in the basestation near network.


## Difference B/W Centralized RAN amd Cloud - RAN :

![2 44](https://github.com/user-attachments/assets/f1273714-93c3-4bf9-a648-0c002b1cd2d6)

* The concept of these two RAN are similarl because the baseband unit are placed at the central location near the core network , However in the case of cloud RAN , the BBU functionality is implemented in the software as virtual network function and these fxn are deployed on the cloud and depending upon the demand these fxn can be increase or decrease and also the resources alocated to these fxns are also be increased or decreased depending upon the demand and it can happene that these virtual network function can cooperate resources with one-another and share resources with one-another for the optimal use of cloud in the network .

## Path to 5G Open RAN Horizontal Dis-aggregation :

![2 4](https://github.com/user-attachments/assets/ccc6c8dd-db07-4711-b8a6-6ff59b59be79)

* Now in the 5G the 3GPP is the main body that defines the standards of the 5G system and 3GPP recommandation of 398.801 has splite the baseband unit into the centralized unit and to the distributed unit and b/w them we have Midhaul transmission link , the purpose of this splite is to maximise the perfromance of the network . FXN which need more computaional work can be placed in the CU near the core network so that they can share resources one-another , while the other fxn are placed into the distributed unit (DU ) and DU may be placed near to the Remote Radio Unit so that the fornthaul fiber is less expensive .
* The loaction of the CU / DU can be change we can loacted both them near to the Core network or near the remote radio unit , it depends upon the deployment senario , CU/DU are virtualized on the COTS or they are virtualized on the Cloud .
* This spliting of the baseatation into CU/DU is called the Horizontal Disaggregation , the BBU functionality is divided into the OSI layers .  





























