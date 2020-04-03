.. |labmodule| replace:: 1
.. |labnum| replace:: 1
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Provision and Base Setup
-------------------------------------------------------

Configuration of the following items in order:

#. Checked Provisioned Modules refelcts the below image (DNS / PEM / AFM and AVR).

|prov_image|

.. NOTE:: CGNAT is NOT provisioned in this case as it is now part of AFM. This provisioning is for CGNAT standalone.

#. Create Vlans. 

|VlanCreationExternal|

.. NOTE:: Use advanced settings and set External to Destination DAG. This pins return traffic back from Internet to the correct TMM

|VlanCreationInternal|

.. NOTE:: Use advanced settings and set Internal to Source DAG. This pins traffic flows to the correct TMM per subscriber

|VlanCreationControl|

.. NOTE:: Use advanced settings and set Control to Default DAG. Default DAG is required for any control plane services (DHCP/RADIUS/Gx/Gy to function correctly.)

#. Create SELF-IP's as per table below:

.. csv-table:: Self IP Network Information
    :header: "VLAN", "IP Address"
    :widths: 40, 40

    "Internal", "10.1.10.5"
    "External", "10.1.20.5"
    "Control", "10.1.30.5"

|self_ip|


#. Create Default route as per table below:

.. csv-table:: IP Route Network Information
    :header: "Destination", "IP Address"
    :widths: 40, 40

    "Default", "10.1.20.1"

|routes|

#. Setup Logging Profiles.

Logging Setup 



.. |prov_image| image:: /_static/prov_image.png
    :scale: 45%

.. |VlanCreationExternal| image:: /_static/VlanCreationExternal.png
    :scale: 100%

.. |VlanCreationInternal| image:: /_static/VlanCreationInternal.png
    :scale: 100%

.. |VlanCreationControl| image:: /_static/VlanCreationControl.png
    :scale: 100%

.. |self_ip| image:: /_static/self_ip.png
    :scale: 45%

.. |routes| image:: /_static/routes.png
    :scale: 45%