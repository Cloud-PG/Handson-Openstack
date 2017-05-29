Port mapping<a name="port-mapping"></a>
=========

Verify that the instance has been correctly created. Click on it and go to the **Console** tab. Since we used a cloud image, we can't access it via user and password, so we need to setup ssh connection to it.
* Go to **Access & Security**, click on **Security groups** tab and on **Create security group**.
* Create one for **SSH access** and another one to allow **ICMP** to the virtual machine.
* **Manage rules** and **Add rule** to open specific ports.

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-1.png)

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-2.png)

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-3.png)

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-4.png)

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-5.png)


* Go to **Instances**, under **Actions** column, **Edit security groups** for your instance and add the newly created ones.

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-6.png)

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Security-groups-7.png)


Next section: [Web server example](Web-server.md)
