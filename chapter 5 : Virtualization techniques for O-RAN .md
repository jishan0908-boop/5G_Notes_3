## Evolution of Virtualization Physical Network Function (PNFs):
![1 1](https://github.com/user-attachments/assets/b00c4efc-a525-4969-be63-4a101ff31420)
* Physical Network Function (PNFs):
* There is the BBU hardware which consist of hardware cards and each cards are custom hardware or proprietary harware aand upon these cards we have Custom Operating System and the functionality of these cards run on the application.

![1 2](https://github.com/user-attachments/assets/75264443-14c4-4439-b583-9cfe31e6bf1f)
* Virtual Network Function (VNFs):
* In this case using the custom hardware we are using the COTS serves on this server we have the Hypervisor , it create and manges the VM and these VMs also called as Virtual Server , like it converts the physical server into multiple virtual server , and each on these server it has OS and on these OS we can run different BBU and these fnxs or apps or application are also called as the Virtual Network Functions . These VM includes a full copy of an OS with associated libraries , and they are slow to boot , and they required lot of disk storage but this approach is less costly than the previois ones .

![1 3](https://github.com/user-attachments/assets/c5cb0070-a071-4b2d-af74-148863f6128e)
* Monolithic Application as VNFs:
* These apps that run on the VMs are called Monolithic Application , because these apps are complex in which the different modules are tightly coupled with one another , that meanse there is tight dependencies btw them , so if single modules fails all the apps fails.If we have to update the modules then we have to update the whole app .
* Monolithic apps difficult and inefficient to manage , deploy and scale up/down.

![1 4](https://github.com/user-attachments/assets/e4cc686d-5a27-44c1-b4e0-74d7cadb0603)

* Cloud Native Network Function- Disributed Application :
* These application consist of microservices are loosely coupled with one-another , and each of these microservices have there own database . They run inside lightweight containers , containers is a stripped down version of OS , it has the required libraries that are required to run the microservices , but these containers are light weight so they can deployed quickly and spread across different servers . Also in this application we can have many instances for microservices , if one microservices goes down then the other instances continues to run so the working of the overall app does not get effected .

## DEVOPS CI-CD in O-RAN:
![2](https://github.com/user-attachments/assets/da37fb97-0bf1-49d9-9d3d-9fd2b68fe508)
* We know that the cloud Native apps consist of loosely coupled Microservices and these services can be independently updated or tested , these services run inside the container , also it is easier to make incremental changes in these services in order to update them in a frequent and in the reliable manner . This done using the Devops approach .
* In  the devops approach we have two teams first one is the Development Team and Operating Team , where Development teams , work on the updatation of the microserviecs ,they code these updates they build these update and they test it , and they send the updated microservices to the Operation Teams .
* Then the Operation teams deploy these microservices they operate them and monitor them , and they send the feedback to the developement team .
* Sinces these two teams working parallel to one-another so , the cost of the updatation and testing is reduce. so we have DEV team that is involed in the Continous Integration of the servics , and we have the OPs team that is involed in the Continuous Deployment of these updated microservices .

## Network Automation to Reduce CAPEX and OPEX:
![3](https://github.com/user-attachments/assets/9d2c10c1-9214-4eaf-877d-a0622c3c097f)

* CAPX : It is the capital expenditure , which is required to set-up the Network , and Network Automation can also Reduce the OPEX , it stands for the Operational expenditure , this is the expenditure which is require to operate the network .
* CAPX are reduce by the Automation , when we are setting up the cloud the modern automation tools enables us to automate the setting-up of these cloud , so the cost of mannual intervension is saved , similarly when we need bringup the Radio site , we can use the equipement which need Zero Touch Provisioning , that means that we just plug that equipement , then this equipement configure itself , there is very little need of mannual intervension , and as a result the cost mannual intervension and the errors that might result of the mannual intervension its cost is saved .
* During the OPEX we can use CI/CD techinques in order to automate the testing and the Upgarde of the O-RAN , so the cost are reduce , when the network is operational , we can use the AI/ML techinques which based upon the performance indicator of the network , optimize that network automatically , so this also reduce the operational cost because very little mannual intervension is required.








