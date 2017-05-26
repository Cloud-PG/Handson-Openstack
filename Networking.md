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
