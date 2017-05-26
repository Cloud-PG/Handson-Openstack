# Hands-on Openstack

1. [Introduction](#introduction)
    1. [General notions](#general-notion)
    2. [Glossary](#glossary)
    3. [Openstack services](#services)
    4. [Dashboard usage](#dashboard)
2. [Networking](#networking)
3. [Virtual machine creation](#vm-creation)
4. [Port mapping](#port-mapping)
5. [Web server example](#web-server)
6. [Advanced examples](#advanced)
    1. [Heat introduction](#heat-introduction)
    2. [Heat template example](#heat-template)

Introduction<a name="introduction"></a>
=========

General notions<a name="general-notion"></a>
---------

To make the usage of the Openstack dashboard easier, you need to first get familiar with some useful terms and components you will encounter later on.

### Instances, flavours, images, volumes, network and subnet, router

An **instance** is a Virtual machine. You can specify its resources through the use of **flavours**.

**Images** are disk images used to launch instances. It's the starting point of the virtual machine that, after its creation, will use the local disk of the **hypervisor**, the physical server in which the instance is running, to store its local disk. Once an instance is destroyed, its local storage will be deleted too. If you want to keep its data, but not the instance itself, you can make a **snapshot** which will create a new image based on the instance disk.

To achieve **storage persistence** (storage not deleted after destroying an instance), we need **volumes** that acts as real disks. You can tell your instance to use a volume as its "root" disk, or attach and detach volumes to instances as secondary disks. Volumes are independent from instances, so if you destroy an instance with a volume attached, you will have the volume available to use with other instances.

**Network** is a private network. It can be connected to the outside world (Openstack **ext-net**) using a **router**. Each network has at least a **subnet** which defines the various options of the network, such as the ip address, dns servers, gateway, ecc. Different networks don't "see" each other unless specified by the user (through advanced use of Openstack routers).

### Project, access & security, key pairs, floating ip

**Projects** are personal area accessible only by users with the necessary permissions. Each project has its own **quota**, the maximum amount of resources (CPU, RAM, ecc) usable by the project.

In the **access & security** section, you can specify information useful to connect to the instances you create. You can add your **key pairs**, public ssh key used to access a virtual machine, specify **security groups** to open ports for your instances (by default all ports are closed for virtual machines) and manage your **floating IPs**, public addresses that you can "attach" to an instance.

### Orchestration

**Stacks** are a group of operations defined through the use of a yaml template. For example you can create a **cluster** of multiple instances without having to start each one manually.

Glossary<a name="glossary"></a>
---------

* **Project**
* **User**
* **Quota**
* **Instance**
* **Flavour**
* **Image**
* **Snapshot**
* **Volume**
* **Network**
* **Subnet**
* **Router**
* **Floating IP**
* **Security Group**
* **Key Pair**
* **Stack**
* **Template**

Openstack services<a name="services"></a>
---------

* Keystone: Authentication ad authorization service
* Glance: Image service
* Nova: Compute service
* Neutron: Network service
* Cinder: Volumes and persistent storage service
* Heat: Orchestration service

Dashboard usage<a name="dashboard"></a>
---------

Open a web browser and go to the [FisGeo & INFN Perugia Openstack homepage](http://openstack.fisica.unipg.it/)

### How to login
Select **Openstack local credentials** from the dropdown menu and use your credentials to login.

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Openstack_login.png)

The **Project** section is where you can manage all your environment.



Networking<a name="networking"></a>
=========

### Network creation

Section **Network** -> **Networks** -> **Create network**. At the prompt enter a name for your network, go to the **Subnet** tab, enter a name and a network address for your subnet, go to the **Subnet details** tab and add "8.8.8.8" in the DNS nameservers section.

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Network_creation.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Net_creation-1.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Net_creation-2.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Net_creation-3.png)

### Router creation

Section **Network** -> **Router** -> **Create router**. At the prompt, enter a name for the router, select **ext-net** from the dropdown menu and click Create. After creating the router, you need to attach it to a local network (the one we just created) so click on the router name, go to the **Interfaces** tab, click on **Add interface**, select the subnet we created earlier and submit.

We have now a private network connected to the outside world.

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation-2.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation-3.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation-4.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation-5.png)

![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Router_creation-6.png)

Virtual Machine Creation<a name="vm-creation"></a>
=========

Section **Compute** -> **Instances** -> **Launch Instance**.

IMAGES come guida openstack

Port mapping<a name="port-mapping"></a>
=========

1. Verify that the instance has been correctly created. Click on it and go to the **Console** tab. Since we used a cloud image, we can't access it via user and password, so we need to setup ssh connection to it.
    * Go to **Access & Security**, click on **Security groups** tab and on **Create security group**.
    * Create one for **SSH access** and another one to allow **ICMP** to the virtual machine.
    * **Manage rules** and **Add rule** to open specific ports.
    * Go to **Instances**, under **Actions** column, **Edit security groups** for your instance and add the newly created ones.

  IMAGE

First Example (web server)<a name="web-server"></a>
=========

1. Gain access to second virtual machine (or the first one if only one created).
2. Install web-server (nginx).
3. Download tarball with handson website.
4. Open the necessary ports.
5. Go to browser and verify installation.

Advanced Examples<a name="advanced"></a>
=========

Heat Introduction<a name="heat-introduction"></a>
---------

* How heat works.

Heat template example<a name="heat-template"></a>
---------

1. Delete all virtual machines created.
2. Download the template to recreate everything we just did.
3. Modify the required parameters.
4. Launch stack.
5. Verify again that everything works correctly.
