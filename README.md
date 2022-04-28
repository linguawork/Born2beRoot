# Born2beRoot

This project aims to introduce to the wonderful world of virtualization. It is about installing a Debian linux system without graphical interface and application of safity rules to the system. 
I created my first machine in VirtualBox under specific instructions. At the end of this project, you was able to set up my own operating system while implementing strict rules. I was supposed to install Debian distro on a virtual machine. 

The use of VirtualBox was mandatory.
I had to turn in a signature.txt file which had a hash code of my system.

This project consists of having set up my first server by following specific rules.
Since it is a matter of setting up a server, I was supposed to install the
minimum of services.  For this reason, a graphical interface was of no
use here.  It was therefore forbidden to install X.org or any other
equivalent graphics server.  

I was to choose as an operating system either the latest stable version of Debian (no testing/unstable), or the latest stable version of CentOS. I chose Debian because it was highly recommended for newcomers to system administration.

I had to create at least 2 encrypted partitions using LVM.
Below is an example of the expected partitioning:
<img width="349" alt="Screen Shot 2022-04-28 at 10 03 12 PM" src="https://user-images.githubusercontent.com/12897177/165827307-0741a38f-e206-4cb8-8205-26b13e14d3e4.png">

I had to apply aptitude and apt and AppArmor.

Additionally I was to implement an SSH service running on port 4242 only. For security reasons, to connect using SSH as root was not to be possible according to the task. Moreover I had to to configure the operating system with the UFW firewall and thus I had to leave only port 4242 open. My firewall was to be active whenever I launch my virtual machine.
The hostname of my virtual machine was supposed to be my login ending with 42 (e.g., wil42). You was to be able to modify my hostname.

I had to implement a strong password policy.
I had to install and configure sudo following strict rules.
In addition to the root user, a user with my login as username had to be present.
The user had to belong to the user42 and sudo groups.
I had to create a new user and assign it to a group.

To set up a strong password policy, I had to comply with the following requirements:
My password had to expire every 30 days.
The minimum number of days allowed before the modification of a password was to be set to 2.
The user had to receive a warning message 7 days before their password expires.
My password had to be at least 10 characters long. It must contain an uppercase letter and a number. Also, it must not contain more than 3 consecutive identical characters.

The password was not to include the name of the user.
The following rule did not apply to the root password: The password had to be at least 7 characters that are not part of the former password.
My root password had to comply with this policy.

To set up a strong configuration for my sudo group, I had to comply with the following requirements:
• Authentication using sudo had to be limited to 3 attempts in the event of an incorrect password.
• A custom message of my choice had to be displayed if an error due to a wrong password occured when using sudo.
• Each action using sudo had to be archived, both inputs and outputs. The log file had to be saved in the /var/log/sudo/ folder.
• The TTY mode had to be enabled for security reasons.
• For security reasons too, the paths that can be used by sudo had to be restricted. Example:         /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin


Finally, you had to create a simple script called monitoring.sh. It had to be developed in bash.
At server startup, the script was to display some information (listed below) on all terminals every 10 minutes (so I used Wall). The banner was optional. No error was to be visible.
My script had always to be able to display the following information:
• The architecture of the operating system and its kernel version.
• The number of physical processors.
• The number of virtual processors.
• The current available RAM on my server and its utilization rate as a percentage. 
• The current available memory on my server and its utilization rate as a percentage. 
• The current utilization rate of the processors as a percentage.
• The date and time of the last reboot.
• Whether LVM was active or not.
• The number of active connections.
• The number of users using the server.
• The IPv4 address of my server and its MAC (Media Access Control) address. 
• The number of commands executed with the sudo program.

I was also to interrupt the script without modifying it.(I had to use Cron.)
Below is the example of how the script was to work:
<img width="455" alt="Screen Shot 2022-04-28 at 10 28 17 PM" src="https://user-images.githubusercontent.com/12897177/165831042-6aebc6d3-fdf0-4621-9cb2-2d2500cd4bb0.png">

Below are two commands one can use to check some requirements:
<img width="505" alt="Screen Shot 2022-04-28 at 10 31 45 PM" src="https://user-images.githubusercontent.com/12897177/165831492-9d11210f-b55f-4ac3-9241-538c3db9b4d8.png">

##Bonuses realized
• I was to set up partitions correctly to get a structure similar to the one below:
In this part the partition sizes did not match to the ones shown on the picture as the system holds some percentage.

<img width="460" alt="Screen Shot 2022-04-28 at 10 34 29 PM" src="https://user-images.githubusercontent.com/12897177/165831875-8fe11d46-b4c8-4a09-85bc-2f22412ead92.png">

• I was to set up a functional WordPress website with the following services: lighttpd, MariaDB, and PHP.
• I had to set up a service of my choice that is useful (NGINX / Apache2 excluded!). 
I installed ADMINER because it is more comfortable to see data with the help of graphical interface.

Below is the link to the full video recorded during my defence of the project.
My final result was 125%







