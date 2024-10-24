
*************************
IOS-MCN SMO Test Cases
*************************

FOCOM
=====

Title
-----
Cluster Deployment


Description
-----------
This test checks the successful deployment of Kubernetes cluster.

1. Configure the hosts.ini file in the `Kubernetes Repo <https://github.com/ios-mcn-smo/focom/tree/main/kubernetes>`_
2. Run the command make k8s-install


Expected Result
---------------
1. SHould be able to run kubectl commands.
2. Output of kubectl get nodes should match the hosts.ini contents.
3. All pods should be healthy when kubectl get pods --ALL is run.


Actual Result
-------------



Title
-----
Docker Deployment


Description
-----------

This test check if the system is ready to run Network-functions and OAM solutions as containers via docker compose.

1. configure the hosts.ini file in the `Docker repo <https://github.com/ios-mcn-smo/focom/tree/main/kubernetes>`_
2. Run the ansible playbook - oam


Expected Result
---------------
1. Docker is installed
2. Necessary packages (jq, keytool, etc.) are installed
3. docker compose is installed.


Actual Result
-------------


Title
-----
Node Preparation for RAN Containers.


Description
-----------
This test check if the system is ready to run O-RAN solution as containers via docker compose.

1. configure the hosts.ini file in the `Docker repo <https://github.com/ios-mcn-smo/focom/tree/main/kubernetes>`_
2. Run the ansible playbook - oran


Expected Result
---------------

1. Lnux realtime kernel is installed.
2. Configured CPUs are Isolated.
3. tuned-adm is installed and the profile is set to realtime.
4. linuxptp is insalled.
5. 2 VFs are created and configured correctly.


Actual Result
-------------


NFO
===
Title
-----

Deployment of CU/DU, and O1 adapter.

Description
-----------

Tests successful deployment of O-RAN CU/DU and O1 adapter as containers.

1. configure the hosts.ini file in the `OAI Docker repo <https://github.com/ios-mcn-smo/nfo/tree/main/docker>`_
2. Run the command make oai-install

Expected Result
---------------

1. All OAI containers are up and running
2. O1 adapter is also running


Actual Result
-------------




Title
-----
Deployment of Core


Description
-----------



Expected Result
---------------


Actual Result
-------------



Title
-----

Deployment of OAM


Description
-----------



Expected Result
---------------


Actual Result
-------------



Title
-----
Integration of RAN and Core


Description
-----------



Expected Result
---------------


Actual Result
-------------


Title
-----
Integration of RAN and OAM


Description
-----------



Expected Result
---------------


Actual Result
-------------


Title
-----
Integration of Core and OAM


Description
-----------



Expected Result
---------------


Actual Result
-------------


Title
-----
Integration of RU and OAM


Description
-----------



Expected Result
---------------


Actual Result
-------------


OAM
===
Title
-----
O1 Events/Messages

Description
-----------
This tests sends multiples of different kinds of O1 Events/messages to the ves-collector.

1. Deploy all the OAM containers.
2. Go to ves-client folder.
3. run _example.sh script


Expected Result
---------------
All events get added Message-Bus.


Actual Result
-------------


.. image:: ./images/no-messages.png
  :width: 300
  :height: 200
  :alt: Before sending events.

.. image:: ./images/all-messages.png
  :width: 300
  :height: 300
  :alt: After sending events.

Title
-----

Description
-----------



Expected Result
---------------


Actual Result
-------------

Title
-----

Description
-----------



Expected Result
---------------


Actual Result
-------------

Title
-----

Description
-----------



Expected Result
---------------


Actual Result
-------------



NON-RT-RIC
==========

Title
-----

Description
-----------



Expected Result
---------------


Actual Result
-------------



