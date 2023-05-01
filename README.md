# mobaxtermVM
Remote access to your virtualbox with mobaxterm from windows

There is an easy way to access your remote Virtual Machine from a Windows  workstation with an application called MobaXterm. You can install it as well as use a portable version. Application is available to download from https://mobaxterm.mobatek.net/download-home-edition.html

Before connecting to you VM, please do the following configuration:
VirtualBox Network Configuration
It's easy to change Virtual Box Network configuration:
- open VBox application and start DVDK VM
- from the VBox main window, select your VM and choose Settings from the toolbar
- Choose Network item and, from the Attached To: dropdown choose Bridged Adapter
![image](https://user-images.githubusercontent.com/45208254/235434282-c5f41da4-d349-4334-8f26-34fea3379eb9.png)

Then Edit ‘/etc/ssh/sshd_config’ and make sure you have
X11Forwarding yes
added to the config file.
If you use portable version just unzip the package and start MobaXTerm app with two-click on the icon:
 
![image](https://user-images.githubusercontent.com/45208254/235434350-bf12cfa9-8099-404e-9d29-437a129d986e.png)


You see the application window now look like this:

<img src="https://user-images.githubusercontent.com/45208254/235434372-564a3db8-9df7-4302-83e9-073c2e0607e4.png" width="600" />

Start new session:

<img src="https://user-images.githubusercontent.com/45208254/235434388-74f4f9d8-890c-4a36-a4cd-af7408c07dd4.png" width="600" />


On the VM(virtualbox), check the ip address by running this command:
**ip addr**

<img src="https://user-images.githubusercontent.com/45208254/235434418-c2a17db9-92be-4d79-a745-f3cafa547f41.png" width="600" />
Go back to Mobaxterm, then Click the SSH button
Provide remote host IP address, username and the security key for the connection, then click Ok
<img src="https://user-images.githubusercontent.com/45208254/235434439-9c9ffbfb-4a87-4575-83af-0a929a468a29.png" width="600" />
Start a new session. That's it you are in.	
<img src="https://user-images.githubusercontent.com/45208254/235434464-1bbc9852-3391-4413-b893-6327cc1386d3.png" width="600" />

Now you can finally start any X Windows application or the whole desktop.
In future, you only need to double click your Saved session on the left and type in your password to connect.


File transfer
Mobaxterm is aso able to transfer files between your PC and the cluster server. Connect to the cluster server, as described above. After connecting, you will see an ‘Sftp’ tab in the left pane showing the remote files located on the serve. 
![image](https://user-images.githubusercontent.com/45208254/235434482-1701e7dd-2d0f-4fc8-a4c8-8ab02a8e51cf.png)

You can then drag and drop these remote files to your PC’s desktop. Alternatively, you may right-click a file and click Download. 
For uploading files/folders, right-lick on the SSH browser(SFTP) on the left and then upload.

![image](https://user-images.githubusercontent.com/45208254/235434496-9bca443d-fb7e-4f77-899d-1573c50de0bf.png)



