CapME
=====

CapME is a web interface that allows you to:

-  view a pcap transcript rendered with tcpflow
-  view a pcap transcript rendered with `Zeek <Zeek>`__ (especially helpful for dealing with gzip encoding)
-  download a pcap

Screenshot
----------
.. image:: images/capme/capme.png

Accessing
---------

You can pivot to CapME from a NIDS alert in `Squert <Squert>`__ or from any log in `Kibana <Kibana>`__ that has timestamp, source IP, source port, destination IP, and destination port.

Authentication
--------------

If prompted for username and password, simply enter your normal Sguil/Squert/Kibana username and password.
