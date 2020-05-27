Use Case 05: Install and Enable AS3 
===================================

Prerequisites
-------------

This usecase assumes that a F5 BIG-IP instance, webservers and Ansible node are deployed. 
To deploy infrastructure in AWS users can use the `F5 Ansible Provisioner <https://github.com/f5devcentral/FAS-provisioner>`_

Overview of Use Case
--------------------

This use case will download the latest `AS3 RPM package <https://github.com/F5Networks/f5-appsvcs-extension/releases>`_ and install it on the BIG-IP.

Application Services 3 Extension (referred to as AS3 Extension or more often simply AS3) is a flexible, low-overhead mechanism for managing
application-specific configurations on a BIG-IP system.

.. note::
  
   This use case only validates that AS3 has been installed via the playbook. 
   More use cases for AS3 will be added later

Use Case Setup
--------------

1. Login to the Ansible Host 

2. Change Directory in the Ansible Host to the use-cases repo previously downloaded

   .. code::
   
      cd ~/FAS-ansible-use-cases/05-Install-and-Enable-AS3/


3. Launching the Ansible Playbook:

   .. code::

      ansible-playbook Install-and-Enable-AS3.yaml

4. Testing and Validating

   - Login to the BIG-IP
   - Navigate to iApps->Packet Management LX 
   - Veirfy the AS3 RPM package is installed

