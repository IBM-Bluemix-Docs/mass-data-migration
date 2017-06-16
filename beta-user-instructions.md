---

copyright:
  years: 2017
lastupdated: "2017-06-14"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Beta User Instructions


1.	Device arrives pre-configured with your IP address, User name, Locked Storage Pool and NFS Share.  The User password and Storage Pool password will be communicated via separate email.

2.	Remove the device from the large travel case.

3.	Determine the most appropriate place for the device to be placed where it will reach both power and your 10GbE connection that will minimize foot traffic. The ability to rack the device is high on our list of things to complete before GA.

4.	Open the lid on the device, tip the device on its right side, and remove it from the portable case using the two finger loops (pictured).
    ![Top of Device](/images/UserGuide1.png)
    The device is pressure fit into the case. The device needs to be removed to maximize airflow and cooling.

5.	Position the device to be connected.  Ensure the device is at room temperature and there is no condensation on it. Connect power using the provided power cable underneath the case lid and switch on the device. There are two power switches (shown below). 
    ![Power swicthes](/images/UserGuide2.png)
    Let the device boot for 5 minutes without network connectivity.
    
6.	Remove the CAT6A cable from the case lid and connect it to the port shown in the picture below.
    ![CAT6A Port](/images/UserGuide3.png)

7.	Connect the provided CAT6A to SFP+ adapter and connect to your 10Gb switch.

8.	Point your browser (not Chrome) and enter HTTPS://<youreth3ip>
    _Note_ that Chrome has recently changed support for self-signed certs.  GA product will have dedicated certs. https://productforums.google.com/forum/#!topic/chrome/su0hEzupG1Q;context-place=topicsearchin/chrome/category%243Aim-not-sure

9.	Log in using the provided User name and Password.

10.	Activate the pre-configured storage pool:
      - Expand the Storage Pools 
      - Click on **DefaultPool** to select it. 
      - Click on **Start**.
      - Enter your Storage Pool Password and click **OK**. 
      ![Activate/Start Storage Pool](/images/UserGuide4.png)
    
11.	Once the storage pool is enabled the NFS share should be available for mounting.

12.	Mount the share on your source server and load the data.

13.	Monitor inbound load on Eth3 from GUI.

14.	When the load is complete, gracefully power down the system.
    ![Right click on Storage System, select Shutdown Storage System...](/images/UserGuide5.png)

15.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their respective storage locations under the lid.  

16.	Insert the device into the portable case, and insert the portable case into the large travel case.

17.	Attach the provided shipping label, notify shipper, and return device to DAL09 data center for load into Cloud Object Storage.
