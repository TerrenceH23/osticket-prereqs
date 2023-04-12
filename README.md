<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>
Using Remote Desktop Protocol into your Windows 10 virtual machine

Install / Enable IIS in Windows with CGI

Download and install PHP Manager for IIS

Download and install the Rewrite Module

Create the directory C:\PHP

Download PHP 7.3.8 and unzip the contents into C:\PHP

Download and install VC_redist.x86.exe

Download and install MySQL 5.5.62

Open IIS as an Admin and register PHP from within IIS

Made osTicket v1.15.8

Download and install HeidiSQL

Continue setting up osTicket in the browser

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/WyOPOZR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After you've created your resoure group and virtual machine inside azure, the first thing you want to do is enable CGI. Open up programs in start menu then select turn on/off windowns program. World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/XU3466e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=https://i.imgur.com/F6cHmGF.png"" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
The next steps after you've enabled CGI is to download and install PHP manager in IIS and the URL rewrite. Follwing this create a seperate folder by going to c: and creating a folder named "php" that we'll use later. Once this is completed we want to download PHP, once that done we want to extract the PHP files to our PHP folder that we created earlier.
</p>
<p>
<img src="https://i.imgur.com/H8cVyOg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
<img src="https://i.imgur.com/es3Yv1t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/WSNyciO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
After everything is installed the next step is to open IIS and monitor it. We need to register PHP to do so as IIS is open, we'll select PHP maanger, hit enable PHP,after this is down we're going to browse our PHP folder that we created earlier. Open the file and select "php-cgi". After that select ok and PHP is registered. Once that's finish I recommend restarting IIS.
<p>
<img src="https://i.imgur.com/GyEfPb8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
Next we want to download the following files "VC redirect, MySQL, OSTicket". We're going to install the VC redirect once that's completed we need to install MySQL.After that's installed we're going to created a password for it. OS Ticket is next on our docket list to download. Now that's downloaded we're going extract our osticket into our www.root folder. Click on the osticket folder, then select the upload folder and drag it to our www.root folder. Rename the upload folder to OSTicket.
<p>
<img src="https://i.imgur.com/r5WRmLZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<img src="https://i.imgur.com/LA466mm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
<img src="https://i.imgur.com/5ujcuhI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
Now that OSTicket is made we want to open it inside IIS. Open IIS back up hit sites then osTicket on the right side select the "browse 80" and OS ticket should open. Now that it's open we need to enable some programs that are off inside of osticket. We're going to enable the following "php_imap.dll, php_intl.dll php_opcache.dll" Once that's done we want to rename our osticket sample file to osticket-config.


<p>
<img src="https://i.imgur.com/izpL54n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src=" https://i.imgur.com/YguEy9R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
<img src="https://i.imgur.com/bs6sRUD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MJKzf9Y.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>


For the next steps right click on the osticket-config file and hit propteries. We want to enable anyone to edit the file. Select secruity then advance and disable all inheritance. Next hit add and hit add properties. Type in "everyone" in the section hit apply then ok and now everyone can edit! 

Download HediSQL and now that it's downloaded we're going to create a database. Create a new session and the user name is "root" and make a password. Connect the session then make a database called "os ticket".

Finish up setting osTicket now that we have a database. Inside osTicket set up put in "osTicket" which we created from Hedi, use the user name "root" and then enter in whatever password you used. Select continue and now you've succesfully made OSTicket!

Congrats!!! 
