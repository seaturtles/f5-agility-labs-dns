Introduction 
============

Welcome to the F5 Cloud Services lab that covers DNS and DNS Load Balancer services. This lab will take you through the setting up, configuration, updates, and removal of the F5 Cloud Services that provide DNS capabilities. You will be using both browser-based UI of the F5 Cloud Services platform, as well as the declarative API, which is available to do all of the things the UI does, and more! 

In the process of this lab you will learn how to:

- Set up a DDoS-protected secondary DNS service

- Retrieve and review the zone file retrieved from the primary DNS (we will provide you with a primary DNS and a zone just for you!)

- Set up Anycast network-backed load balanced DNS record 

- Add and update application endpoints and a load-balancer pool 

- Configure, update, and test geoproximity rules, and

- Have fun working with UI and APIs!


Environment & Pre-Requisites
============================

Unified Demo Environment (UDF) Access
-------------------------------------

For the F5 Agility Lab session we recommend that you access the F5 Unified Demo Environment (UDF) session/course, which contains a Windows VM instance with all of the required software pre-installed.

You will then open a remote RDP session into your personal instance containing the credentials generated for you. The link to the UDF course is: `SaaS based DNS and DNS Load Balancing <https://udf.f5.com/b/918107a7-5d3c-4979-b25a-4194283be3a4>`_. 

You can also follow the link in your email invite and login to the lab environment.

Click "Join", which will take you to your personalized environment. Click "Deployment" adjacent to the "Documentation" link (1).

From the **Deployment** menu, you will click "DETAILS" (2) and copy the Administrator password to your clipboard. The password starts immediately after Administrator: 

Then, click on "ACCESS" (3) and download the RDP file with your preferred resolution. You will then open this RDP file and provide the Administrator password copied in the previous step.

.. figure:: _figures/0001.jpg 

At this point you will be logged into the Windows VM that contains all of the required software, outlined below.

Alternative Install(s) of Software on Your Own Computer
-------------------------------------------------------

Alternatively, if you'd like to install the software on your computer (and if organization permits to do so), you can install the following software to complete the lab:

- Any modern browser **(REQUIRED)**: for working with the UI (and this document)
- `Postman <http://bit.ly/309wSLl>`_ **(REQUIRED)**: for working with the API of the F5 Cloud Services
- `Opera browser <https://www.opera.com/>`_: for simulating geo-location specific traffic  (you can alternatively use your own VPN solution if you have one to do simulate geo-proximity traffic instead)
- Any text editor: for duplicating Load Balanced Record 

NOTE (only if you already have an existing F5 Cloud Services account)
---------------------------------------------------------------------

.. important:: **You can ignore this section if you do not yet have an existing F5 cloud services account**.

If your account has been previously created through a Limited User invitation (such as an email invite from another lab or from a different account owner), then it is possible that you haven't yet completed a full registration. 

You can quickly tell if you have a full account by looking at your account(s) in the `F5 Cloud Services Portal <https://portal.cloudservices.f5.com/>`_. If you do now see any "Accounts you own:" and only see "Accounts you've been granted access to" as a **"Limited User"**, then you will need to create a full account / update user info before you can proceed with this lab. You can do so in the `SECTION C of the Zone Name step <https://clouddocs.f5.com/training/community/dns/html/class6/lab/lab1.html#zone-name>`_ of the lab, via the F5 Cloud Services API using the Postman request titled "Set User Info (optional)", the details of which are outlined after the Login. 
