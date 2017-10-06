Virtual Machine Creation<a name="vm-creation"></a>
=========

Section **Compute** -> **Instances** -> **Launch Instance**.

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation.png)</kbd>

Choose a name for your instance.

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation-2.png)</kbd>

Choose the **image** you want to create the instance from (in this case ubuntu-16.04).

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation-3.png)</kbd>

Choose the size of your instance.

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation-4.png)</kbd>

Choose the previously created **network**.

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation-5.png)</kbd>

Create or import a **key-pair** and then choose it. You will launch the instance with that key, used to get access to the Virtual Machine. If you have to generate a **key-pair** you can follow these steps:

 * **Windows**: download [PuTTYgen](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) to create a new **key-pair**. If you have problems follow these instructions: [Using PuTTYgen];
 * **Linux** and **Mac**: open the terminal and use this command: 
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   If you have problems you can read this [guide](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Instance_creation-6.png)</kbd>

Add a **floating IP** to the instance.

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Floating-ip-1.png)</kbd>

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Floating-ip-2.png)</kbd>

<kbd>![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Floating-ip-3.png)</kbd>


Next section: [Port mapping](Port-mapping.md)
