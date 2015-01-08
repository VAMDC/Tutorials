Virtual machines for node building
==================================

Virtual-machine image are available to provide an environment for node building. 
Users of Windows and MacOS should consider using these VMs, but they can also be hosted on Linux and Unix systems.

Two different images are available. 

* `Base system with node software, MySQL and libraries <http://tutorial.vamdc.eu/_downloads/vamdc-platform.ova>`_
* `Complete system with executable nodes as examples <http://tutorial.vamdc.eu/_downloads/vamdc-example-nodes.ova>`_

Both images are based on Ubuntu Linux.


Intended use
------------

The VMs are provided as a convenient place to develop data-nodes. Once a node is developed, its data and Python files would typically be transferred into a separate environment for deployment.

The "base system" contains a Python installation, Python modules, MySQL and the common part of the VAMDC node-software. To build a node here, you need to import your data and to write the Python customizations of the node software, as described in the node-software manual.

The "complete system" contains two example nodes, one for atomic spectroscopy and one for molecular collisions. Each node is fully configured and executable, with sample data pre-installed in MySQL. If your data are similar to the examples, you could develop your node from one of the running examples.

The VMs are not suitable for production deployment as supplied; they do not have appropriate web servers and are not sufficiently secured. However, a careful system-administrator could refine one of the VMs into a production-ready appliance.


Running a VM
------------

You need a `hypervisor <http://en.wikipedia.org/wiki/Hypervisor>`_ on your computer to run the virtual machines.
The VM images are written in  `Open Virtualization Format <http://en.wikipedia.org/wiki/Open_Virtualization_Format>`_ and should work with a number hypervisors, but they were built and tested with `Oracle VirtualBox <https://www.virtualbox.org>`_. Instructions below assume that you are using VirtualBox.

Having installed VirtualBox, download the VM image using the links above. It arrives as a .ova file of about 2.5GB. You can keep it anywhere.

Start VirtualBox. From the file menu of VirtualBox, select "Import appliance..." and, in the file-selection dialogue, select the .ova file. VirtualBox will display the details of the VM (simulated hardware and OS) and the name of the VM. Note that the name is "vamdc-ubuntu-12.04 ...", i.e. different from the name of the OVA file. Press the import button in the dialogue to start the import; importing takes about a minute. After importing you will see the VM in the list in VirtualBox's main window.

The imported VM is stored independently of the .ova file. Changes you make inside the running VM are stored by VirtualBox but not copied to the .ova file. You can delete the file, or keep it as a record of the initial state of your VM.

To start the VM, double-click on its entry in the list. The machine opens in a separate window. 

The is just one user account, called *vamdc* (NB: the account name is in lower case, even though it is displayed in upper case on the log-in screen), and the password is *delhi-tutorial*. *You should change this password immediately*. The account has admin privileges (*sudo*).


Running the example nodes
-------------------------

The "complete-system" VM contains two runnable nodes, *tignanello* for spectroscopy (a cut-down copy of the Chianti node) and *thud*, a simplified collisional-data node (with data contributed by IDEADB). These are embedded in the software tree at */home/vamdc/NodeSoftware.

To run one of the nodes, change directory to that node's folder in the node-software tree and give the command::

    python manage.py runserver

This runs the node in Django's built-in web-server, on port 8000. You can reach this port from clients inside the VM (e.g. Firefox is available) but its visibility outside the VM depends on the hypervisor settings.

The best test of a node under development is the TAP validator and this is present in the home directory of the *vamdc* account. Change directory to home and then start the validator with the command::

    java -jar TAPValidator.jar
 