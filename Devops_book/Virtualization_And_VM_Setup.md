# Virtualization and VM Setup 

## Virtualization

- Virtualization is a technology which creates the virtual representations of the servers, storages, networks and other physical machines. It simulates the computing environment by dividing the physical resources into virtual machines, operating systems and other components.

- The Traditional way of doing business is having one server for one application. Suppose consider an example below.

  **Ex** :

  1) Consider a businees runs three servers, where first servers serves an email service which uses Windows operating System and second server serves Web application which uses linux operating system and 3rd application serves database application which uses Unix operating system.

  2) Instead of Running all these three applications in three different servers, what if we have run all these applications runs in single server even run their different operating systems. This is what virtualization does. 

  3) Virtualization basically divides the physical components of single server into three virtual machines where each virtual machine runs different operating system along with different services such as email, web and database.

- The software the enables virtualization is called <b>Hypervisor</b>. It allocates and controls the physical resources such as Storage Space, RAM etc., to each vitual machine.

- There are actually two types of virtual machines. Type - I and Type - II

  **Type - I** : Type - I hypervisors are simply installed on top of the bare metal. Bare Metal means there is no existing operating system installed on top of physical resources such as RAM, ROM and Mother Board. Here there is no Operating System between physical machine and Hypervisor. These type of hypervisors are used for production level only.

  **Example For Type - I** : VMware ESXI, Critix XenServer, Microsoft Hyper -V.

  **Type - II** : Type - II hypervisors are installed on top of existing operating system. That means there is an operating system in between the Hypervisor and Physical Machine. These hypervisors are used for personal computers to test new softwares or try different operating systems.

  **Examples For Type - II** : Oracle VM VirtualBox, Microsoft Virtual PC, VMware Workstation.

- There are actually so many benifits of virtualization technology. Those are :

  1) It saves Money on hardware and electricity. By using virtualization we doesn't need more servers which automatically reduces the cost on hardware and also decreases the power consumption by a server.

  2) It saves Money on floor space. Virtualization can reduce the usage of physical servers which reduces the cost on floor space.

  3) Similary it also reduces the money  for maintainance and management of the servers as we require system admininstrators to maintain the health of the servers.

  4) Virtual Machines are portable. Since these are just software files, so we can easily transfer them from one machine to another machine.

  5) Through virtualization technology, we can use complete resources of the server which gives full computing capability.

  6) Virtualization easily resuces the servers from disasters. Since VM are software files we can easily store them in other Servers, So that we can recover them whenever a server fails.

## VM Setup

- We can setup the Virtual Machine both Manually and Automatically. But there are some issues if you want to setup the VM Manually. The Issues are :

  1) First we need to install the os seperately by downloading the iso file of that OS which is a manual task.

  2) It takes so much time to setup the Virtual Machine manually. Since you need to follow so many steps for stting up te virtual machine.

  3) Since it is the manual process then there might be so many human errors.

  4) If you want to replicate same VM then we need to follow the entire process to setup which is time taking process. So it is tough to replicate mutiple VMs

  5) Since it involves lot of steps then a proper documentation is required for setup the VM.

  6) If you unfortunatley delete the VM then we cannot recover it back and it takes lot of time to create same VM. So disaster recoveray is difficult. 

- To overcome these issues, we can automatically set the VM by just using the few commands. In order to setup VM automatically, we are using a software called <b>Vagrant</b>.

- <b>Vagrant</b> is an open source software which is used to provision the development environments quickly. It create the virtual Machines by just running the few vagrant commands.

- Vagrant doesn't need any Os installation because vargrant provides free VM images (which are called boxes) available in Vagrant Cloud. All the changes we need to install in VM is managed by the single file called Vagrant File. By using the vagrantfile only we actually create virtual machines.

- Vargrant provides simple command to provision virutal machine. Those are :

  **vagrant init <boxname>** : It creates the vagrant file in our local directly which includes all the settings of the box or VM image.

  **vagrant up** : It creates the VM machine in the Virtual Box.

  **vagrant status** : It gives the status of all the VMs present in the Virtual Box.

  **vagrant halt** : It shutdown or poweroff the current running Virtual Machine.

  **vagrant destroy** : It actually deletes the virtual machine from the virtual box.

  **vagrant global-status** : It gives te status of all the VMs presenting in the Virtual Box.

  **vagrant box list** : It gives all VMs present in the Virtual Box.

  **vagrant ssh** : It is used to login into the virtual machine that is currently running.

- **Working of Vagrant** : Once we run `vagrant init boxname` then vagrant fetches the vagrant file of that image from the vagrant cloud and places it in the current directory. When you run `vagrant up` then we vargrant actually looks for the image/box of that VM in the local directory, if it is not found in the local directory then it actually download that VM from the vagrant cloud and then it creates the VM in the virtual box by effectively communicating with the hypervisor. After this we can perform anything on that virtual machine by using the above commands. This is actually procees being run in the background.