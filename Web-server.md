First Example (web server)<a name="web-server"></a>
=========

1. Gain access to second virtual machine.
2. Install web-server (nginx).
3. Download [tarball](https://github.com/Cloud-PG/Handson-Openstack/raw/master/web-server.tar.gz) with handson website (OPTIONAL).
4. Open the necessary ports.
5. Open browser, go to vm floating ip and verify installation.

### Solution

1. Open a terminal and connect as user ubuntu to the vm you created.
  > #: ssh ubuntu@10.2.201.'x'

2. Install nginx (or apache) web-server.
  > #: sudo apt-get update && sudo apt-get install nginx

3. OPTIONAL: Download and untar tarball containing a website with a replica of this guide.
  > ~: wget https://github.com/Cloud-PG/Handson-Openstack/raw/master/web-server.tar.gz

  > ~: sudo tar -zxvf web-server.tar.gz -C /var/www

  > ~: sudo service nginx restart

4. Open port 80 as we did for the SSH port in section [Port-mapping](Port-mapping.md).

5. Open your browser and go to the floating ip address of your vm. You should see this page (if you didn't skip step 3):

  ![](https://raw.githubusercontent.com/Cloud-PG/Handson-Openstack/master/img/Web-server.png)

Next section: [Advanced examples](Advanced-examples.md)
