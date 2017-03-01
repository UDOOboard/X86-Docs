You can use UDOO X86 as a Desktop PC, connected up to 3 4K resolution monitor, keyboard and mouse. This is probably the most used setup, but if you want you can communicate with the board in remote way, so long as you leaving the board connected to a network.

## Requirements
A first condition to establish a SSH connection with your UDOO X86 is to have previously completed the tutorial about [Find IP Address](!Basic_Setup/Find_IP_Address).  
A second condition is to install a `SSH Server` on your UDOO X86 system, and install an `SSH Client` on the PC from which you want to connect to UDOO X86.

## SSH Server on UDOO X86

Choose the software for the OS you've installed on your UDOO X86.

<div>
 <ul id="ssh-server" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#ssh-linux" aria-controls="linux" role="tab" data-toggle="tab">Linux</a></li>
  <li role="presentation"><a href="#ssh-windows" aria-controls="windows" role="tab" data-toggle="tab">Windows</a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="ssh-linux">

On a Linux system we suggest to use `OpenSSH Server`.  

On `Ubuntu/Debian/Linux Mint` type the following command:

    $ sudo apt install openssh-server

N.B: On Ubuntu you usually find the openssh-server already installed out of the box.

On `RHEL/Centos/Fedora` type the following command:

    # yum -y install openssh-server

On `ArchLinux` type the following command:

    # pacman -S openssh

You can change some OpenSSH server configuration in the file `/etc/ssh/sshd_config`.
make a copy of the original sshd configuration file first.

    sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.backup
    sudo gedit /etc/ssh/sshd_config

<span class="label label-warning">Heads up!</span> Take note of your Linux `username` and `password`. These will be required during the connection from the client.


If you want to use another SSH Server different from OpenSSh, you can find a [comparison of SSH Server](https://en.wikipedia.org/wiki/Comparison_of_SSH_servers) here.

  </div>
  <div role="tabpanel" class="tab-pane" id="ssh-windows">

On Windows you usually won't use the SSH connection to access a terminal, so we suggest to follow the docs on the next page to use a complete [Remote Desktop (VNC)](!Basic_Setup/Remote_Desktop_(VNC)) connection.

  </div>
 </div>
</div>
<script>
$('#ssh-server a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>

## SSH Client on the remote PC

On the PC from which you want to connect to UDOO X86 choose the client for the OS you use.

<div>
 <ul id="ssh-client" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#ssh-linux-client" aria-controls="linux-client" role="tab" data-toggle="tab">Linux</a></li>
  <li role="presentation"><a href="#ssh-windows-client" aria-controls="windows-client" role="tab" data-toggle="tab">Windows</a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="ssh-linux-client">

On a Linux system we suggest to use `OpenSSH Client`.  

On `Ubuntu/Debian/Linux Mint` type the following command:

    $ sudo apt install openssh-client

N.B: On Ubuntu you usually find the openssh-server already installed out of the box.

On `RHEL/Centos/Fedora` type the following command:

    # yum -y install openssh-clients

On `ArchLinux` type the following command:

    # pacman -S openssh


  </div>
  <div role="tabpanel" class="tab-pane" id="ssh-windows-client">

There are lots of valid SSH clients for Windows.  

We suggest to use [MobaXterm](http://mobaxterm.mobatek.net/), a complete enhanced terminal for Windows with X11 server, tabbed SSH client, network tools and much more.  

Another famous SSH client is [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).

  </div>
 </div>
</div>
<script>
$('#ssh-client a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>


## Connection via SSH
Once you have completed these steps, open your SSH client. For the sake of this example, we consider you're using PuTTY on Windows.
Opening PuTTY a window will ask you to specify the destination you want to connect to.  
In the first blank space, named *Host Name or IP address*, type the **IP Address** of UDOO X86.

Eventually, a Windows Firewall popup could appear the first time you do this. If this happens, allow PuTTY to bypass the firewall.

When the connection succeeds, a black window will appear. That is the terminal. It will ask you to enter your login credential. Type the name of the user <username>, then press "Enter".
A new line will appear:

    <username>@<IPAddres>'s password:

Type the password of the username then press "Enter".  
<span class="label label-warning">Heads up!</span> Do not worry if you don't see what you type in the terminal: it's an expedient to hide your password to eventual onlookers.

At this point you can use your terminal:

```bash
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-59-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

90 packages can be updated.
40 updates are security updates.

Last login: Mon Jan 30 16:48:52 2017
udooer@UDOOX86RevF:~$


```

Good job, mate: you are now connected to your UDOO Neo via SSH.
