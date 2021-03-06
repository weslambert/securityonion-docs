RITA
====

From: https://github.com/activecm/rita

    RITA is an open source framework for network traffic analysis.

    The framework ingests Zeek Logs, and currently supports the following
    analysis features:

    | Beaconing: Search for signs of beaconing behavior in and out of
      your network
    | DNS Tunneling Search for signs of DNS based covert channels
    | Blacklisted: Query blacklists to search for suspicious domains and
      hosts
    | URL Length Analysis: Search for lengthy URLs indicative of malware
    | Scanning: Search for signs of port scans in your network

We can add RITA to Security Onion to enhance its current capabilities and leverage the great work from the folks at `Active Countermeasures <https://activecountermeasures.com/>`__. They've done a fantastic job of allowing RITA to be easy to integrate with Security Onion.

Warning
-------

Please keep in mind we do not officially support RITA, so installation is at your own risk.

Additionally, RITA currently only supports use of Zeek logs in ``TSV`` format. If you are running the latest version of Security Onion, you will need to switch from ``JSON`` to ``TSV`` format by following the steps here:

`<Zeek#tsv>`__

Installation
------------

To install RITA on Security Onion:

Download the install script:

::

   wget https://raw.githubusercontent.com/activecm/rita/master/install.sh

Run the installer:

::

   sudo bash ./install.sh
   
Configuration
-------------

You must set your own values for ``InternalSubnets`` in ``/etc/rita/config.yaml`` before importing
data into RITA. See https://github.com/activecm/rita#configuration-file for more information.

Usage
-----

You can then import logs with:

::

   rita import /nsm/bro/logs/2019-09-04 dataset1

To see the most visited URLs:

::

   rita show-most-visited-urls dataset1

To see long connections, type:

::

   rita show-long-connections dataset1

To see beacons, type:

::

   rita show-beacons dataset1

Finally, you can issue an HTML report (viewable in browser) by typing:

::

   rita html-report

See other available commands with:

::

   rita --help

| For additional information, see:
| https://github.com/activecm/rita
