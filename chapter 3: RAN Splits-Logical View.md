## Different RAN Functional Splits:
![1](https://github.com/user-attachments/assets/f66fc62a-44f7-4152-b97b-28180d181624)
* Lets assume that the DU/CU are virtualized on the same codes hardware , and RRU is the different hardware entity , and we have considering the spiling of the functionality b\w these fronthaul , and the functionality we are talking about , like Packet Data Convergien Protocol Functionality , Radio Link Control Functionality ,Medium Access control Functionality the Physical layer Functionality and the Radio Frequency Functionality .

## RAN Split Option 1 :
![2](https://github.com/user-attachments/assets/98431779-9509-4aa8-ae7d-31b645049d51)
* RAN split Option1 : In this option all the functionality are implemented inside the RRU , so all the processing is done in the RRU , so in the fronthaul the requirement of the data rate is low , also high latency tolerance and can even use microwave link .
* Since all the functionalaity is done in RRU then RRU became complex , it consumes more power , more size and more costly .

## RAN Split Option 2 :
![3](https://github.com/user-attachments/assets/fce93e41-f035-4c96-b1d0-f66385b1cc8a)
* In the option 2 , the PDCP fxn is in the CU/DU , while all the other layers are implemented inside the RRU , in this case majority of the fxns are loacted in the RRU , so there is less aggresive demand on the fronthaul , in terms of maximum bit rate and allow able lateancy , that means there is  lesser bit rate in fronthaul , and allow able latenacy is more .
* In this option , the Radio Link Control is in the RRU , and Automatic Repeat Request (ARQ) mechanism is implelmented in the RLC layer and this mechanism works b/w RRU and UE , scence the distance b/w them is less , so the latency of the ARQ mechanism is less .
* This option also allows the dual connectivity, in this case a UE can connected to basestation a time and it is reciving apart of data from one basestation and another part of data from another basestation , the data split is made in the PDCP layer , because the PDCP layer is present in the CU so , we can easily allow the dual connectivity .
* In this option , the PDCP layer is implemented in the CU , so there will be less centralization and virtualization benifits .
* Coordinated Multipoint (CoMP), in this the same data is send to different cells , and this is implemented in the MAC layer so, nd it is in the RRU , so it is difficult to send same data all the other basestation , so ability to implelment CoMP , is lost in thie Split 2 . 
## RAN Split Option 8 :
![4](https://github.com/user-attachments/assets/086fe72e-2086-4d2c-879f-9ea444c3f19b)

* In split 8 , the four fxns are presernt in the CU/DU , while the Radio Frequency is implemented in the RRU . The data is moved form CU/DU to RRU , so the PDCP header is appended into the data , the  header of RLC, MAC and PHY , are added to the data , as a result the data rate in the fronthaul increases as the data increases the latency allowable is decreases , in this option there is the high demand of the fronthaul , there is another prblm the Hybird ARQ became time-sensitive .
* Example: When transmiter sends the data to the reciver and the it recives it correctly then it acknowldge it to the transmitter, but if the data transmitted by the transmitter is corupted , during the transmission procedure , then reciver sends the not acknowldgement to the transmitter , then it sends data again this procedure is called , " Automatice Repeat Request procedure " this procedure is implemented in the Radio Link Control layer , since this layer is in the CU/DU , so it is the transmitter and the UE is the recibver , so the distance b/w them is more ,so this procedure became more time-sensitive , in other to run this procedure works correctly so the Round Trip Delay time should be less than 5ms , it is the time , form the transmission delay to the reciver plus the transmission delay from the reciver to the transmitter .
* Disadvantge of this option is tht , we have High data rate and low latency on the fronthaul.
*  Advantage : The fxns of all the four layers can be implemented as a software on the COTS server or in other words they are virtualized on the COTS .
*  These virtualized fxn can be shared b/w different RRU , in the load-balancing manner , it easy to upgrad these fxn because it only require software .
*  Another Advantages is that the RRU is very simplified , it occupy the less space , less power and less cost , this RRU can be used with other Radio Access technologies .
*  Coordinated Multipoint can be used , because of this technique the data is transfer to different RRU , and these cells coordinate and send same data to the UE , because of same data is reciveing by the UE so the signal quality and the strength improves , and recive data rate Increases .

## RAN Split Option 6:
![5](https://github.com/user-attachments/assets/7832f2be-413a-4f3a-b0d3-204e4438edf6)
* This option is adopted by the small cell forum the PDCP . RLC & MAC are implemented at data centralised unit , while the PHY & RF are implemented in the RRU . In the RAN the scheduling in the MAC layer , scheduling decission about the Radio Resources like , what channels are to be given to diff UE and the Data rate also , these decisions are centralized at the center location and the interface b/w MAC & PHY is standardise by the small cell fourm, and this interface is called nFAPI , the purpose of the standardizeing this , because any CU / DU can interface with any RRU also the Interoperability increases b/w them .  

## RAN Splits Logical View:
![6](https://github.com/user-attachments/assets/f50f08dc-4bd1-4cac-a4cd-78ad6d85c6f9)
* In the Coverage use cases we have large cells , in which we have small number of user , and these users have low data rate , and the latency requirements is less , so we can use microwave link or cheaper optical fiber for the data rate and latency .
* In the capacity Use cases are used in the dense urban area , where cells are small , so the distnace b/w the basestation and CU/DU is less but in this link we required higher data rate and low latency , we need to use expensive fibers , since more virtualized fxns and are loacted in CU/DU so we have more virtualization . Also we have small RRU because of less fxn , then size of RRU is small and they are easily implemented in urban area.

## Option 7.2x for Open RAN :
![7 1](https://github.com/user-attachments/assets/20c5f8d2-80cf-411a-b0e7-84a3b9ef23de)
* O-RAN Alliance is the main body that are responsbile for developing the specification of the O-RAN , in the termilogy of O-RAN Alliance the CU is called O-CU and DU is called O-DU and the RRU is called as the O-RU . The Split option adopted by the O-RAN alliance is 7.2 , it means that b/w the O-DU and O-RU the split option 7 is implemented and b/w O-DU & O-CU in midhaul the split option that has been implemented is the 2 also there is a RRC layer in the O-CU , which is above the PDCP layer .
* There are two varint of this option 
* 7.2a: The Precoding that is done in the PHY which is done in the O-DU , while the Fxn of beamforming in the PHY layer is handle by the O-RU .
* 7.2b:Precoding and Beamforming is done in O-RU , as a result in the fornhaul , the requirement of data rate and latency decrases .
![7 2](https://github.com/user-attachments/assets/dbae3625-a3b1-43c9-b3ea-7520b468d95c)

 ## Enhanced CPRI (e-CPRI) protocol :

* The protocol used b/w O-RU & O-DU is called Enhanced CPRI (e-CPRI) protocol it is packet based protocol , this protocol can be framed inside the etherenet packets . So we get less dependence on the availablity of fiber in the fornthaul .
* The Enhanced CPRI (e-CPRI) protocol is a successor of CPRI protocol and it develop by the e-CPRI forum , it is a open interface and this uses the bandwidth in the fronthaul very efficiently . 


















































































































