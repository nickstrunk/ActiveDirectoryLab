<h1>Home Lab - Active Directory</h1>

 <!-- ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)/> -->

<h2>Description</h2>
In this lab we're going to walk through how to create an Active Directory home lab environment using
Oracle Virtual Box. Configuring and running this lab will definitely help your understanding of how 
active directory and windows networking works, so I'd highly recommend running through it a couple times,
ask questions where stuff is unclear, and eventually try to build your own without watching. Please let
me know if you have any questions!
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
 
Preplanning of Project: <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/b7fdcb80-8215-4dc0-97c4-d26252a353cb" height="80%" width="80%" alt="Planning Diagram"/>
<br />
<br />
 
DC Installation (Server ISO):  <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/8679325e-bd56-47df-b4cc-43c1231c8c47" height="80%" width="80%" alt="DC Installation"/>
<br />
<br />
 
Set Up IP Addressing: <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/0e89e34f-1e39-4e07-a98b-c96f3da20198" height="80%" width="80%" alt="Network Interface Cards"/>
<br />
<br />
* No default gateway because the domain controller serves as the default gateway
<br />
* Active directory automatically installs DNS, so there server will use itself as the DNS server. Can use either its own IP address (172.16.0.1) or loopback address (127.0.0.1)
<br />
<br />
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/1914bbad-8393-437e-ad44-ef71e65595b2" height="80%" width="80%" alt="Internal Addressing"/>
<br />
<br />

Renamed PC:  <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/d73f7998-b974-4930-93da-c0924a72847d" height="80%" width="80%" alt="Renamed PC"/>
<br />
<br />

Select Active Directory Domain Services:  <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/992cf44d-2003-4ae6-b778-55c4ca89a56f" height="80%" width="80%" alt="Active Directory Domain Services"/>
<br />
<br />

Create Domain:  <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/5841c385-451f-447b-8257-d5eb68e15366" height="80%" width="80%" alt="Create Domain"/>
<br />
<br />

Create Personal Admin Account:  <br/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/13161bca-9353-450c-85c7-693e3ad11b70" height="80%" width="80%" alt="Personal Admin Account"/>
<br />
<br />

Install Remote Access (RAS) / Network Address Translation (NAT):  <br/>
* Allow Windows 10 client to be on private virtual network, but still be able to access the Internet through the domain controller.
<br />
<br />
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/f9a5a277-eed3-4f0b-a910-b9d3a66766a1" height="80%" width="80%" alt="Remote Access (RAS) and Network Address Translation (NAT)"/>
<br />
<br />

Set up NAT:  <br/>
* Tools > Routing and Remote Access > Right Click server > Configure and Enable Routing and Remote Access
<br />
<br />
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/51ad4262-d969-40cd-a5ee-3fbc3afac37b" height="80%" width="80%" alt="NAT Setup"/>
<br />
<br />

Set up DHCP Server  <br/>
* Allow our Windows 10 clients to automatically get an IP address that will let them communicate on and browse the internet, while on the private internal network
<br />
<br />
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/4db30ddd-a14c-4035-a9eb-b2b1b7772ea8" height="80%" width="80%" alt="DHCP Server Set Up"/>
<br />
<br />

Set DHCP Scope  <br/>
<br />
<br />
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/bcd3ffed-28be-4dde-8bd5-494eb8a4afc0" height="80%" width="80%" alt="DHCP Scope"/>
<img src="https://github.com/nickstrunk/ActiveDirectoryLab/assets/165805194/41fb3c3b-e9c2-48d4-b51d-ef1869dfb3ec" height="80%" width="80%" alt="DHCP Scope Planning"/>
<br />
<br />
Timestamp: 26:30
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
