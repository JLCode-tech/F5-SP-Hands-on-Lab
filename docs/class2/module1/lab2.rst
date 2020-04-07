.. |labmodule| replace:: 1
.. |labnum| replace:: 2
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: DNS
---------------------------------

DNS Cache
~~~~~~~~~

#. Create DNS Cache as Resolver

|CreateDNSCache|

.. NOTE:: Keep this as defaults, and resovler settings. For PRODUCTION use these will need to be tuned.

DNS Profile
~~~~~~~~~~~

#. Create DNS profile for the DNS listeners, reference the DNSCache created in previous step.

|CreateDNSProfile|

.. NOTE:: key component of this profile is the Cache enabled. This assists subscribers QoE and is an important feature we can use.



.. |CreateDNSCache| image:: /_static/CreateDNSCache.png
    :scale: 100%

.. |CreateDNSProfile| image:: /_static/CreateDNSProfile.png
    :scale: 100%

Configure DNS for Gi-LAN
   - DNS
   - DNS cache
   - DNS Security