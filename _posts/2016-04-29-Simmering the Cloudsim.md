CloudSim: A framework for modeling and simulation of Cloud Computing Infrastructures and Services. Recently, cloud computing emerged as the leading technology for delivering reliable, secure, fault-tolerant, sustainable, and scalable computational services, which are presented as Software, Infrastructure, or Platform as services (SaaS, IaaS, PaaS). 
Moreover, these services may be offered in private data centers (private clouds), may be commercially
offered for clients (public clouds), or yet it is possible that both public and private clouds are combined in hybrid clouds. The primary objective of this 
project is to provide a generalized, and extensible simulation framework that 
enables seamless modeling, simulation, and experimentation of emerging Cloud computing 
infrastructures and application services. By using CloudSim, researchers and 
industry-based developers can focus on specific system design issues that they 
want to investigate, without getting concerned about the low level details related
to Cloud-based infrastructures and services

CloudSim is powered by jProfiler.
Overview of CloudSim functionalities:

* support for modeling and simulation of large scale Cloud computing data centers
* support for modeling and simulation of virtualized server hosts, with customizable 
policies for provisioning host resources to virtual machines
* support for modeling and simulation of energy-aware computational resources
* support for modeling and simulation of data center network topologies and 
message-passing applications
* support for modeling and simulation of federated clouds
* support for dynamic insertion of simulation elements, stop and resume of simulation
* support for user-defined policies for allocation of hosts to virtual machines and 
policies for allocation of host resources to virtual machines

Software Required:
Netbeans IDE (version greater than 5) 
CloudSim

Steps:

1. Netbeans Installation:Simply click on the downloaded file and follow it with default 
settings. Open the netbeans. Click file then new project.

![Step1](/images/cloudsim-step1.png)

2.  Select java and java application.

![Step2](/images/cloudsim-step2.png)

3. It will take few seconds to create the project.

![Step3](/images/cloudsim-step3.png)

4. Give name to your project and uncheck to create main file option.

![Step4](/images/cloudsim-step4.png)

5. Netbeans will take time to make project.

![Step5](/images/cloudsim-step5.png)

Once it’s done double click on the new project in solution explorer. Right click on 
libraries and choose the Add jar files.

![Step6](/images/cloudsim-step6.png)

Locate the cloud sim folder and you will find cloudsim-3.0.3.jar file. Click on ok.

![Step7](/images/cloudsim-step7.png)

Now locate the org folder which is present in the examples folder in main cloudsim
folder. Copy the org folder.

![Step8](/images/cloudsim-step8.png)

 6. Right click on the source packages in the solution explorer panel and paste it. 
 To run the example program, open org.cloudbus.cloudsim.examples in source packages.
 Right click on example you want to run and click run file.

![Step5](/images/cloudsim-step9.png)

7. Done! See the output below.

![Step5](/images/cloudsim-step10.png)

Thanks for reading!
