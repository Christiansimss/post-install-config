<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Virtual Machine
- Remote Destop Connection
- Google Drive file (<a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a>)
- Internet Information Service (IIS) set up 
- Wifi connection 

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/rdVp6Sn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continuing from where we left off with the Virtual Machine. You now want to open a windows control panel and head to programs, form program and feature. Now within the program and features there will be a selection called turn windows feature on/off on the left side, click that button. And the following prompt on your screen should show up, from there we will select the IIS (Information Internet Services) and let the IIS install. 
</p>
<br />

<p>
<img src="https://i.imgur.com/xyCY5M7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now after the IIS has finished, we will go to the google doc and download the webplatforminstaller file. The file will download this launcher as shown above, go through the installation when complete the following will appear.
</p>
<br />

<p>
<img src="https://i.imgur.com/93ejQfx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we select finish we will then head over to the windows search and type in platform. The Web Platform Installer 5.1 should appear. Moving to the search bar on the top right type in MySQL and select the MySQL Windows 5.5 released 9/9/2015.
</p>
<br />

<p>
<img src="https://i.imgur.com/j7Q72F4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Next after adding MYSQL go back to the bar and type PHP. From there filter out the names by pressing name and locate the PHP (x86) files you want to add them up until you get to PHP 7.4.13 (x86). The image above is the exact file from the lab and there should be exactly 12 items to be installed after selecting the files.
</p>
<br />

<p>
<img src="https://i.imgur.com/g209LMw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next press the install button and you should recieve a prompt on a new username for MySQL as root and to create the password(Document these 2 pieces of information they will be used later in the lab). Once you do press next and go through the installation, the installation should fail and prompt the page above.

</p>
<br />

<p>
<img src="https://i.imgur.com/j1MGLmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we are going to install the PHP Manger and vcredist located within the <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab. These 2 files can be found in your file explorer within the downloads as shown above.
</p>
<br />

<p>
<img src="https://i.imgur.com/4ViV05z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that we head back into are Link to our <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> google Drive for the lab and download the osTicket file. Once downloaded extract the zipped folder from the downloads into the downloads, doing this makes the zip folder create a regular folder with the same contents.
  
<p>
<img src="https://i.imgur.com/Q3LUJgA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next head into the new and unzip folder from the osTicket download and copy the upload folder. Go to <strong>This PC--> then windows(C:)--> then inetpub--> and finally open wwwroot</strong> and paste the upload folder within. Rename that folder to osTicket.
  
  <p>
<img src="https://i.imgur.com/PlitxOI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>![brYNraM - Imgur](https://user-images.githubusercontent.com/121305134/209887661-bef7dbce-4bc3-4364-a26e-31f77d9a7285.png)

<p>
Once we are done with the last step we want to head to are windows search bar and type in IIS. Select IIS and restart IIS with the panel on the right side, after that select the drop down arrow key for VM-osTicket or whatever name you selected earlier in the lab on the <strong>left hand panel--> then select sites--> Defualt Website--> and are osTicket folder</strong> should be there.
  
  <p>
<img src="https://i.imgur.com/KIGAyir.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we are going to select the PHP Manager within the osTicket Home located in the center. From there select Enable or disable an extension, look for php_imap.dll is enable along with php_intl.dll and php_opcache.dll.
  
  <p>
<img src="https://i.imgur.com/dRGPdWI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we head back to are wwwroot folder within file explorer, from there we select osTicket--> Then include. When inside the include folder scroll down to the ost-sampleconfig.php to ost-config.php as shown above.
  
  <p>
<img src="https://i.imgur.com/cHBdPn3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we changed the ost-sampleconfig.php to ost-config.php we will <strong>open its properties then --> open security --> click on advance --> then disable inheritance --> add permission --> select principle at the top left --> from there within the open box below for objects type everyone --> select Check Names --> and select ok --> on the following page select full control to give all basic permissions besides Special permissions for everyone</strong>. Your security panel should display whats above with everyone and full control under access.
  
  <p>
<img src="https://i.imgur.com/sDhXvlZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you've reached this page all the following steps have been completed successfully. Now simple fill out all the information as shown<strong>(Document The Admin User portion as well as the Database setting username and password will be needed for the lab).</strong>
  
  <p>
<img src="https://i.imgur.com/mQPzPDm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we head back into are <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab and download the HeidiSQL. Go through the complete download until the finish button is prompt, after you select finish the application will open as shown above.
  
  <p>
<img src="https://i.imgur.com/wvurZnY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select the add button on the button left, Heidi will prompt you to put in the password you create earlier when downloading the php files within WebPlatformInstaller 5.1. Enter the password and you will be sent to the page shown.Next <strong>rightclick unnamed --> then hover over create new --> and select Database</strong>. Name that dataase osTicket<strong>(it is important the spelling is correct)</strong>.
  
  <p>
<img src="https://i.imgur.com/aCKlFCn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once complete you will have this page appear letting you know that you've successfully created the osTicket system. The links below are for the user end and the staff as well.
  
  <p>
<img src="https://i.imgur.com/cWrNy3w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Final step, head back to the folder where we were in the include folder. From there <strong>Rightclick properties--> head to security tab --> then advance --> and double click on everyone --> once you are back in permissions change every user to read and execute</strong> press ok and close out the tabs for the properties.
  
  <p>
<img src="https://i.imgur.com/2kYWhCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To end off the installation for osTicket. Head into the osTicket folder by <strong>clicking on This PC --> then windows (C:) --> select inetpub --> wwwroot --> and finally select osTicket.</strong> There we must delete the setup folder, in order to do so we must delete the contents with the folder. After deleting the contents within the setup folder we can move onto deleting the setup folder from osTicket. And congradulations you have completed the osTicket Installation.
</p>
<br />
<p>
This will conclude the Installation for the osTicket Lab. The next section we will begin to use osTicket and begin with the configurations. Next section <a href='https://github.com/DevilDog2001/osTicket-configurations'>Configurations</a> .
</p>
<br />
