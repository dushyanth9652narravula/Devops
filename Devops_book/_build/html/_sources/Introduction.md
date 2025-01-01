# Introduction to DevOps

Devops simply means the combination of words <b>Development</b> and <b>Operations</b> that describes the set of practices and tools that helps organizations to deliver applications and services quickly. It bridges the gap between development and operations team. The aim of the devops is to improve the collaboration between the development and operations team , increase the efficiency of software development life cycle  and ultimately produces better products. To know what does devops mean and how it is originated, first we need to learn about Software Development Life Cycle (SDLC).

## Software Development Life Cycle

- SDLC simply means the Life cycle for buidling a software product. SDLC involves 6 phases.

  1) **Requirement Gathering** : In this phase, infromation will be collected such as product features, Users of the product, Usage of the product , User requirements and Current state of the market.

  2) **Planning** : In this phase, business persons determines whats the budget for this project, what are the resources required to implement this project and what are the risks associated with this project.

  3) **Designing** : In this Phase, Architects will design the software based on the inputs from previous phase and produce design documents which are basically the roadmap for the developers to build te software.

  4) **Development** : In this phase, developers actually write the software code based on the design artifacts from design phase.

  5) **Testing** : In this phase, testers actually test the code written by the developers and return the software code back to developers if they find any bugs in the code.

  6) **Deploy and Maintainance** : In this phase, Operations team deploy the software tested by the tester and moniter the health of the servers to make them up all the time.

- There are so many models in Software Development Life cycle. Some of those are WaterFall, Agile, Spiral, Big Bang etc. We can think these models as different patways to produce a software product. We can acesses these pathways based on cost, risks and time taken to reach the destination.

  1) **WaterFall Model** : In WaterFall model, we can move to next step only when the current step in completed or not. That means if you are in designing step currently, you can move to development step only when you have completed entire design of the project. That means waterfall model is straight forward process.

  2) **Agile Model** : Agile model is cyclic process. In this model, all the development cycle is divided into different time frames. That means in first frame, software development team completes all these 6 steps and design the intial product. After designing the intial product, then they start adding more functionalities to that initial product. So with agile methodology, we iteratively build the end product instead of straight forward approach.

- Now a days many software industries use agile methodology to build the software product. But there are some disadvantage with the agile methodology.

  **Disadvantages with Agile Methodology** :

  1) In Agile Methodology, there is no proper coordination between the development team and operations team. Because development team mainly focuses on developing  the new functionalities, where as operations team mainly focuses on the maintaining the servers up all the time, etc. So there is clear gap between the goals of both the teams.

  2) Generally operations team is responsible for deployment of all the product designed by the development team. They deploys te product based on the instructions provided by the development team. Since developers team and operations team runs on different environments, so operations team might not install some of the requirements or dependencies on their environment which prone to errors and leads to delay in deploymnet of the product which automatically delays the delivary process.

  3) In Agile methodology, everything is manual process. Most of the steps need man power. Since it requires lot of mannual work, so there might be some human errors which might delay the delivery process.

- So to overcome the issues in the agile methodology, a new methodology was introduced which is simply called Devops. Devops simply means Development + Operations. It is set of tools which bridges the gap between the development team and operations team to improve the delivery process of the software product. Devops simply automates most the works in software development process.

## Continuous Integration 

- Continuous integration is an automated process in devops which generates the software and its features quickly and efficiently. It is the software development practice which involves frequently mergining the code changes into the shared repository and automatically building and testing the code.

- The goal of CI is to improve software quality, find and fix bugs quicker and reduce the time it takes to release te new updates. 

- In Agile, developers first write te code for the software project and psuh them into the centralized repository called Git hub repository. Then other people build and test this code and produce a software artificat by packaging the code in the form of zip, archive, MSI etc. Then this software artifacts gets deployed in the production servers. Then software testers test this code.

- In this entire process there are some problems which are : Developers actually write the code for the new features for three weeks and then all the written code gets builded and tested. If they got any errors while building and testing the code and then that code is sent back to the developers team to fix the bugs. Here, its irritating for the developers to fix all the bugs in the entire 3 weeks code which automatically delays the development of new features.

- So, to rectify this, they came to a solution which is instant build and test the code as soon as the developer pushes the code into shared repository. If you got any error while building the code then notify those errors back to the developers then they can easily fix that code.

- But the main, problem is building and testing the code manually for every push is difficult. So we need to automate this. To automate this process we need use the countinuos integration process.

- The entire continuous integration process is like Code -> Fetech -> Build -> Test -> Notify -> Feedback -> Code which is a cyclic process.

- Tools used are :

  1) **Coding** : Eclipse, Visual Studio Code, Atom, Pycharm, etc.

  2) **Version Control** : Git, SVN, TFS, Perforce, etc.

  3) **Build Tools** : Maven, Ant, Gradle, MS Build, Visual Build, IBM Urban Code, Make , Grunt etc.

  4) **Software Artifacts** : SonaType Nexus, Jfrog Artifactory, Archiva, Cloudsmith Package, Grunt etc.

  5) **Continuous Integration Tools** : Jenkins, Circleci, Teamcity, Bamboo CI, Cruise Control.

- So the entire process of continuous integration is :

  `Code` -> `Code Build and Test` -> `Code Analysis (Finding Bugs in code)` -> `Artifact Repo`

  **Note** : If any bugs are found in Code Analysis then entire code is sent back to the Developers and they need to fix it.


## Continuous Delivery

- Once we build the software artifact from the CI Process, then we need to deploy it into the servers. SInce CI is automated, Ops team get regular deploymnet requests from the Dev team which gives a additional burden to the ops team. Sometimes the artificat maynot deploy correctly on the servers because of configurations changes. 

- Usually Deploymnet of the artifact includes :

  1) Server Provisioning - Creating  the Server for that deployment.

  2) Dependencies - After Server Provisioning, we need to install all the dependencies.

  3) Configuration Changes - Then we need to configure the sever which similarly look like dev team environment.

  4) Network - Then we need to set up the firewalls and some other network settings.

  5) Artificat Deploy - Then we need to deploy the artifact that we have got from CI. 

  And there may be some other steps also. If any of the steps might be failed then ops team might get errors. And a lot of manual work is required.

- After code deployment then the next step is Quality and Assurance Testing. That means in this step , QA team will test the deployed product whether the features are working correctly or not. If everything works well then that code sends to production level. These are the steps involved while buiding a software product. 

- In the deploymnet and QA steps , there are lot of manual approvals are required to procced to further steps. Any unclear instructions from previous steps might delay the delivery process. So we need to automate these steps also.

- To automate these steps we have many tools. Those are :

  1) **Ansible, Puppet, Cheff** - These tools are for system automation such as server provisioning and configuring the server etc.

  2) **Terraform, Cloud Formation** - These are for cloud automation.

  3) **Jenkins, Octopus Deploy** - These are for CI/CD automation.

  4) **HELM CHARTS**

  5) **Code Deploy**

- So now Ops team write the automation code for deploymnet and QA team automation code for testing the deployed product and then they synchronize it with the CI Process which automates entire procees of Software Development Life Cycle.

- <b>Continuous Delivery</b> is the process of automating the build, test, configuration, and deployment from the build to the production environment.

- The main aim of the Continuous Delivery is Speed up te deployment, Reduce costs, Lowe Risks and Maintain Code quality.

<b>This is what Devops Means which bidges the gap between the Dev and Ops team by automating the entire Software Development Life Cylce.</b>