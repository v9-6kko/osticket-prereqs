<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- VC_redist.x86.exe -> https://drive.google.com/file/d/189TGgfAQ9o-qJNKx6SZN7Z8Su1mQDUZ5/view?usp=share_link
- rewrite_amd64_en-US.msi -> https://drive.google.com/file/d/1dUWr3YtxejZfSDks4sW8XHX3tGLByXCI/view?usp=share_link
- PHP-7.3.8-nts-Win32-VC15-x86.zip -> https://drive.google.com/file/d/1tE_cpWWOm7x-oyP7b18Mxfoznfj-0GcP/view?usp=share_link
- PHPManagerForIIS_V1.5.0.msi -> https://drive.google.com/file/d/14lAfYgcgM2TdJsCGy09mQRl4knW10mVy/view?usp=share_link
- mysql-5.5.62-win32.msi -> https://drive.google.com/file/d/1AYckc_0Fx3Vw8Ce-pRv_CUSRMsZTYDFm/view?usp=share_link
- HeidiSQL_12.3.0.6589_Setup.exe -> https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe 
- osTicket -> https://drive.google.com/file/d/1SFwuU5XzCUQkwWZzSgU5-R5fPa7se5Fj/view?usp=sharing

<h2>Installation Steps</h2>

Before we begin, there are prerequisite files that must be installed. Fortunately all the files and programs needed have been provided, with links in this guide. 

<p>
<img src="https://i.postimg.cc/59gYGFRR/30.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Let’s begin with PHP Manager for IIS. Once you’ve installed it, run the file. You should be greeted by this screen.
</p>
<br />

<p>
<img src="https://i.postimg.cc/VLNrckyL/31.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  <img src="https://i.postimg.cc/L60q4FRk/32.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Press next, read through the license agreement, allow it to install and then close it.
</p>
<br />

<p>
<img src="https://i.postimg.cc/cLgvrk4p/33.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After this we will install the IIS URL Rewrite Module. Download from the provided link, and run the file. You should be greeted by this screen.

</p>
<br />

<p>
<img src="https://i.postimg.cc/L8cnfkJn/34.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once again, read through the license agreement and allow it to install. Once done, press Finish.
</p>
<br />

<p>
<img src="https://i.postimg.cc/XqYJ3QzD/image-20.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to install Microsoft Visual C++ 2015-2022. Download and open the file. You should see this screen.

</p>
<br />

<p>
<img src="https://i.postimg.cc/B6g6ddMK/image-19.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Read through the license agreement, and then click Install. Once setup is successful, we can move on to the steps of setting up osTicket.

</p>
<br />

<p>
<img src="https://i.postimg.cc/FKwgYJ4Z/3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, we will create a new directory on the C: drive. Navigate to your C: drive within File Explorer, and create a new folder called "PHP"
</p>
<br />

<p>
<img src="https://i.postimg.cc/PJjW4sNv/4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will also need to enable a few extra features in order to open osTicket. Pressing the Windows key, navigate to your control panel by searching for it. Once you have the control panel open, click on "Programs"
</p>
<br />

<p>
<img src="https://i.postimg.cc/gJRy8kcP/5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.postimg.cc/sXZ1RTtp/6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.postimg.cc/t4SzHMv8/7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With Programs open, select "Turn Windows features on or off". Once on this screen we will be enabling the features: "Internet Information Services", "World Wide Web Services", "Application Development Features", "CGI". 
</p>
<br />

<p>
<img src="https://i.postimg.cc/WbynP4nm/19.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.postimg.cc/GtKyx4Z6/20.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now that the PHP folder has been created, we will extract the contents of “PHP-7.3.8-nts-Win32-VC15-x86.zip” into it. Open the zip file, select extract, and then finally the C:PHP folder.

<br />

</p>
<br />

<p>
<img src="https://i.postimg.cc/q7NxBx9q/8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will set up MySQL. Once the Setup Wizard opens, select Typical installation.

</p>
<br />

<p>
<img src="https://i.postimg.cc/FzVjCWJW/10.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next Select Standard Configuration.
</p>
<br />

<p>
<img src="https://i.postimg.cc/sD3PGrtt/11.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select Install as Windows Service and continue
</p>
<br />

<p>
<img src="https://i.postimg.cc/pXkfDSvy/12.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the MySQL Server Instance Configuration Wizard, create a root password. IMPORTANT: This password can be whatever you’d like, but be sure to remember it as we’ll need it later.
</p>
<br />

<p>
<img src="https://i.postimg.cc/RC7Q0Fb7/9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Proceed and wait for MySQL to finish configuring. Once done, press Finish.
</p>
<br />

<p>
<img src="https://i.postimg.cc/q762HM3C/14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After setting up MySQL, we will begin installation and setup for HeidiSQL. Select the directory you’d like for HeidiSQL to be installed in, and press next.
</p>
<br />

<p>
<img src="https://i.postimg.cc/T34nsWp6/16.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Start Menu Folder and press next.
</p>
<br />

<p>
<img src="https://i.postimg.cc/264v3cTk/17.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the Additional Task screen, leave everything as it appears by default and press next.
</p>
<br />

<p>
<img src="https://i.postimg.cc/264v3cTk/17.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Accept the agreement, and finish installation
</p>
<br />

<p>
<img src="https://i.postimg.cc/vmyGb01L/image.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, open Internet Information Services (IIS) by pressing the Windows key and typing it in.
</p>
<br />

<p>
<img src="https://i.postimg.cc/k4F67VXD/22.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.postimg.cc/hPCmJ78d/23.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we have IIS open, we will need to set some things up first. Open up “PHP Manager” and select “Register new PHP version”

</p>
<br />

<p>
<img src="https://i.postimg.cc/Bbmj1dF0/24.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select the path to the php executable file. This will be located in the directory we’ve created earlier. (C:\PHP)

</p>
<br />

<p>
<img src="https://i.postimg.cc/ZqNvD7G8/26.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select the file “php-cgi” and press OK

</p>
<br />

<p>
<img src="https://i.postimg.cc/tgF7z16D/28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With PHP registered, we will now need to activate some extensions. Select “Enable or disable an extension” and activate the following extensions: “php_imap.dll”, “php_intl.dll”, “php_opcache.dll”. The end result should look as pictured.

</p>
<br />

<p>
<img src="https://i.postimg.cc/sxjBxVvm/29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.postimg.cc/mkprr7xZ/image-21.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With all of that setup, we now move onto getting osTicket. Select the zip file “osTicket-v1.15.8.zip” and extract the contents into C:\inetpub\wwwroot

</p>
<br />

<p>
<img src="https://i.postimg.cc/W32p65Tb/image-27.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once it’s been extracted to the wwwroot folder, rename the “upload” folder to “osTicket”.

</p>
<br />

<p>
<img src="https://i.postimg.cc/y8ZNVJLB/image-22.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open the osTicket folder and then the include folder. Find the file titled “ost-sampleconfig.php” and rename it to “ost-config.php”
</p>
<br />

<p>
<img src="https://i.postimg.cc/kMTGwPVr/image-23.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once it’s been renamed we’ll be assigning permissions to it. Right click, select properties, and then security. Click “Advanced”

</p>
<br />

<p>
<img src="https://i.postimg.cc/tCfTQdt2/image-25.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the Advanced screen, click “Disable inheritance”, and select “Remove all inherited permissions from this object.” You should see a screen like this.

</p>
<br />

<p>
<img src="https://i.postimg.cc/Yqj9sDgv/image-24.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will add a new permission. Click add and create a new group named “Everyone”.

</p>
<br />

<p>
<img src="https://i.postimg.cc/Dz3wm2NG/image-26.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Give the newly created Everyone principal “Full Control”. The end result should look like this.
</p>
<br />

<p>
<img src="https://i.postimg.cc/KjWZbFLR/image-28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With all of that done, we are now ready to open osTicket. Return to IIS, and navigate to Default Web Site > osTicket.
</p>
<br />

<p>
<img src="https://i.postimg.cc/3wZYR2mM/image-34.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the right, select “Browse *.80 (http), you should be greeted by this screen.

</p>
<br />

<p>
<img src="https://i.postimg.cc/SxCmBBKx/image-33.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Continue and begin filling out the information. Your helpdesk name and default email can be anything you like.
</p>
<br />

<p>
<img src="https://i.postimg.cc/hvvSNhXk/image-32.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you get to the database settings we come to our last bit of setup. Open HeidiSQL which we installed earlier.
</p>
<br />

<p>
<img src="https://i.postimg.cc/HxBYSbk0/image-31.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Skip and you should see a screen like this. Enter your username which is root, and the password which you created earlier. Once entered, click Open.
</p>
<br />

<p>
<img src="https://i.postimg.cc/L6rH092W/image-29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click the left sidebar, and select “Create new”>”Database”. Title this new database “osticket”.
</p>
<br />

<p>
<img src="https://i.postimg.cc/9F4mpR5T/image-35.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once created, return to the Database Settings on the osTicket website and fill in the root username, your password, and the Database “osticket”.

</p>
<br />

<p>
<img src="https://i.postimg.cc/50N1FjSX/image-36.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Install Now, and afterwards you should see this screen. Congratulations! You’ve now installed osTicket!
</p>
<br />










