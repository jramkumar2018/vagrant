# BP client test
Nginx running in an Alpine linux container, in a VirutalBox VM configured via Ansible

OVERVIEW
--------

When executed, the code in this repository will use Vagrant to build an Ubuntu (Trusty) VirtualBox VM.
It will then use Ansible to configure the VM with Docker, and create a new container based on Apline linux.
Finally, it will install and configure nginx in the container, such that the hosted page can be viewed from the originating machine, at http://localhost:18081

REQUIREMENTS
------------
Vagrant (1.8.1 was used to test this configuration)

VirtualBox (5.0.40_Ubuntu used to test this configuration)


BUILDING THE ENVIRONMENT
------------------------
Clone this repository:

  $ git clone https://github.com/jramkumar2018/testrun.git

Change to the application folder:

  $ cd Bptest
  
Start the Vagrant machine:

  $ vagrant up
  
ACCESSING THE HOSTED PAGE
-------------------------

The static content can be access at http://localhost:18081

TESTING THE ENVIRONMENT
-----------------------

From Bptest directory, run the run-tests.sh script:

  $ ./run-tests.sh
  
The tests check for the following:

The Vagrant host is listening on port 18081

Docker is installed and running on Vagrant guest

Docker host is listening on port 18081

Docker guest is running Alpine Linux

Nginx is running on Docker guest


