# Handson-Openstack

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

* Istanze, reti e sottoreti, router, immagini, volumi, flavours.

* Project, access & security, key pairs, floating ip.

* Orchestration.

Glossary<a name="glossary"></a>
---------

* Compute
    * Instances
        * Flavours
        * Images and cloud images
        * Floating IP
        * Snapshot
        * Volumes
        * Persistence
        * Console
* Network
    * Private network
    * Floating IP
* Orchestration
    * Stack
    * Template

Openstack services<a name="services"></a>
---------

* Keystone
* Glance
* Nova
* Neutron
* Cinder
* Heat

Dashboard usage<a name="dashboard"></a>
---------

[Openstack homepage](http://openstack.fisica.unipg.it/)

* How to login.
* Menu.

Networking<a name="networking"></a>
=========

1. Create net and subnet.
2. Router.

Virtual Machine Creation<a name="vm-creation"></a>
=========

1. Compute -> Instances -> Launch Instance.
2. Name, source (image), flavour (small enough), network (newly created network), keypair.
3. Verify machine creation and gain access to it (floating IP and security groups).

Port mapping<a name="port-mapping"></a>
=========

1. Create a second virtual machine (without floating IP) ???

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

* How heat works: (copy from Bologna).

Heat template example<a name="heat-template"></a>
---------

1. Delete all virtual machines created.
2. Download the template to recreate everything we just did.
3. Modify the required parameters.
4. Launch stack.
5. Verify again that everything works correctly.
