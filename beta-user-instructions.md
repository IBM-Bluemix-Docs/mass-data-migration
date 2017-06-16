---

copyright:
  years: 2017
lastupdated: "2017-06-16"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Beta User Instructions


1.	Device arrives pre-configured with your IP address, User, Locked Storage Pool and NFS Share.  The User/Password and Storage Pool Password will be communicated via separate email.

2.	Remove the device from the large travel case.

3.	Determine the most appropriate place for the device to be placed where it will reach both power and your 10GbE connection that will minimize foot traffic.  The ability to rack the device is high on our list of things to complete before GA.

4.	Open the lid on the device, tip the device on its right side, and remove it from the portable case using the two finger loops (pictured).  The device is pressure fit into the case.  The device is to be removed to maximize airflow and cooling.
    ![Top of Device](/images/UserGuide1.png)

5.	Position the device to be connected.  Ensure the device is at room temperature and there is no condensation on it. Connect power using the provided power cable underneath the case lid and power on the device. 

    **Note**: There are two power switches. 
    ![Power switches](/images/UserGuide2.jpg) 
  
    Let the device boot for 5 minutes without network connectivity.
 
6.	Remove the CAT6A cable from the case lid and connect it to the port shown in the picture below.
    ![](/images/UserGuide3.jpg)
    

7.	Connect the provided CAT6A to SFP+ adapter and connect to your 10Gb switch.

8.	Point your browser (not Chrome) and enter HTTPS://youreth3ip  

    **Note**: Chrome has recently changed support for self-signed certs. GA product will have dedicated certs.
    https://productforums.google.com/forum/#!topic/chrome/su0hEzupG1Q;context-place=topicsearchin/chrome/category%243Aim-not-sure

9.	Use the provided Username and Password to log in.

10.	Activate the pre-configured storage pool:
    - Expand Storage Pools.
    - Click on **DefaultPool** to select it. 
    - Click on **Start**. 
    - Enter your Storage Pool Password and click **OK**. 
    ![Activate Storage Pool](/images/UserGuide4.png)
    

11.	Once the storage pool is enabled the NFS share should be available for mounting.

12.	Mount the share on your source server and load the data.

13.	Monitor inbound load on Eth3 from GUI.

14.	When the load is complete, gracefully power down the system.  
    ![Right Click on Storage Systems and select Shutdown Storage System...](/images/UserGuide5.jpg)
 
15.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their respective storage locations under the lid.  

16.	Insert the device into the portable case, and insert the portable case into the large travel case.

17.	Attach the provided shipping label, notify shipper, and return device to DA09 data center for load into Cloud Object Storage.
