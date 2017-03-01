You can use UDOO X86 as a Desktop PC, connected up to 3 4K resolution monitor, keyboard and mouse. This is probably the most used setup, but if you want you can communicate with the board in remote way, so long as you leaving the board connected to a network.

[Virtual Network Computing (VNC)](https://en.wikipedia.org/wiki/Virtual_Network_Computing) is a graphical desktop sharing system that uses the Remote Frame Buffer protocol (RFB) to remotely control another computer. Basically VNC allows you to use your keyboard and mouse of your PC to interact with the graphical desktop environment of the UDOO X86 from remote.

## Requirements
A first condition to establish a VNC connection with your UDOO X86 is to have previously completed the tutorial about [Find IP Address](!Basic_Setup/Find_IP_Address).  
A second condition is to install a `VNC Server` on your UDOO X86 system, and install an `VNC Client` on the PC from which you want to connect to UDOO X86.


## VNC Server (on UDOO X86)

A VNC server is a program that shares a desktop with other computers over the Internet. Choose the software for the OS you've installed on your UDOO X86.

<div>
 <ul id="vnc-server" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#vnc-linux-server" aria-controls="linux-server" role="tab" data-toggle="tab">Linux</a></li>
  <li role="presentation"><a href="#vnc-windows-server" aria-controls="windows-server" role="tab" data-toggle="tab">Windows</a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="vnc-linux-server">

On Linux you usually need to install a VNC Server. There are various alternatives.  
For example you can install one of these through the package manager of your Linux Distro or downloading from the official websites:

* [x11vnc](http://www.karlrunge.com/x11vnc/)
* [tightvncserver](http://www.tightvnc.com/licensing-tvnserver.php)
* [tigervnc](http://tigervnc.org/)
* [realvnc](https://www.realvnc.com)

Some distros comes with a functional preinstalled VNC Server, so you can check if the distro are you using already has a desktop sharing software.

For example [Vino](https://help.ubuntu.com/community/VNC/Servers#vino) is the default VNC server in `Ubuntu` to share your existing UDOO X86 desktop. Follow the instruction in the link to enable the desktop sharing feature.    
At this page you can find a list of the most common VNC Servers used in Ubuntu: [Ubuntu VNC/Servers](https://help.ubuntu.com/community/VNC/Servers).  
If you come across an encryption Vino error trying connecting follow this page. [Vnc Vino Ubuntu Security fix](http://tiemensfamily.com/TimOnCS/2014/04/12/vnc-vino-ubuntu-security-fix/)


  </div>
  <div role="tabpanel" class="tab-pane" id="vnc-windows-server">

Windows 10 comes with a Remote Desktop Server already installed.  
The PC must be running Windows 10 Pro/Education/Enterprise. If you Windows 10 version is the Home you can not access it remotely.  
You need to turn on the Remote Desktop feature on the UDOO X86 in this way:

1. Right-Click the **Start** button and go to **System**
2. In the Left Menu click on **Remote settings**
3. Check the **Allow remote connections to this computer** radio button. For a higher level of security, check the **Allow connections only from computers running Remote Desktop with Network Level Authentication(recommended)**
4. Click **Apply** and **OK**

Now the Remote Desktop service is enabled an ready to accept remote connections.
You can find other infos [here](https://support.microsoft.com/en-us/help/17463/windows-7-connect-to-another-computer-remote-desktop-connection).

  </div>
 </div>
</div>
<script>
$('#vnc-server a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>


## VNC Client on the remote PC

Now you need to install a VNC Client on the PC from which you want to connect to UDOO X86.

<div>
 <ul id="vnc-client" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#vnc-linux-client" aria-controls="linux-client" role="tab" data-toggle="tab">Linux</a></li>
  <li role="presentation"><a href="#vnc-windows-client" aria-controls="windows-client" role="tab" data-toggle="tab">Windows</a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="vnc-linux-client">

There also are lots of valid VNC clients for Linux.  

For example, [VNC Viewer](https://www.realvnc.com/download/viewer/), [VNC® Viewer for Google Chrome™](https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla), [TightVNC](http://www.tightvnc.com/download.php), [TigerVNC](http://tigervnc.org/).

Choose the one you prefer and install it in the remote PC.

  </div>
  <div role="tabpanel" class="tab-pane" id="vnc-windows-client">

Windows 10 comes with a VNC Client already installed. In the search box of the Windows taskbar, type **Remote Desktop Connection** to find it.

In the **Computer** box you can use the *IP Address* or the *Computer Name* assigned to your UDOO X86. We suggest to use IP Address.  

There also are lots of valid VNC clients for Windows.  

For example, [MobaXterm](http://mobaxterm.mobatek.net/), a complete enhanced terminal for Windows with X11 server, tabbed vnc client, network tools and much more.  
Other alternatives could be [VNC Viewer](https://www.realvnc.com/download/viewer/), [VNC® Viewer for Google Chrome™](https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla), [TightVNC](http://www.tightvnc.com/download.php), [TigerVNC](http://tigervnc.org/).

  </div>
 </div>
</div>
<script>
$('#vnc-client a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>

## Connection via VNC

Regardless of the system and software you are using all the VNC client will ask you to insert the **IP Address** of the UDOO X86 to connect with it.  
After the connection is established you will need to insert the credential, **username** and the **password**, of the user configured in the UDOO X86 Operating System.  
