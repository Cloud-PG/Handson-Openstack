First Example (web server)<a name="web-server"></a>
=========

1. Gain access to the second virtual machine.
2. Install web-server (nginx).
3. Download [tarball](https://github.com/Cloud-PG/Handson-Openstack/raw/master/web-server.tar.gz) with handson website (OPTIONAL).
4. Open the necessary ports.
5. Open browser, go to the virtual machine floating ip and verify the installation.

### Solution

1. Open a terminal and connect as user ubuntu to the vm you created.
  > ~: ssh ubuntu@10.2.201.'x'

2. Install nginx (or apache) web-server.
  > ~: sudo apt-get update && sudo apt-get install nginx

3. OPTIONAL: Download and untar tarball containing a website with a replica of this guide.
  > ~: wget https://github.com/Cloud-PG/Handson-Openstack/raw/master/web-server.tar.gz

  > ~: sudo tar -zxvf web-server.tar.gz -C /var/www

  > ~: sudo service nginx restart

4. Open port 80 as we did for the SSH port in section [Port-mapping](Port-mapping.md).

5. Open your browser and go to the floating ip address of your vm. You should see this page (if you didn't skip step 3):

> **Note**: if you get the error `sudo: unable to resolve host name-of-this-machine` you have to add the value stored in `/etc/hostname` in `/etc/hosts` like that:

> ```bash
> 127.0.0.1 localhost localhost.localdomain name-of-this-machine
> ```

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Web-server.png)

Next section: [Advanced examples](Advanced-examples.md)
