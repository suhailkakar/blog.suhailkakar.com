## Linux Cheat Sheet For Beginners

If you're not using the terminal, Linux commands may appear scary at first by once you start using them you will understand them very easily On a Linux system, there are numerous commands for executing operations and procedures.

Having a list of commands on hand is useful whether you are new to Linux or an experienced user.

## File Permission commands

<table>

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>ls-l</td>

<td>to show file type and access permission</td>

</tr>

<tr>

<td>r</td>

<td>read permission</td>

</tr>

<tr>

<td>w</td>

<td>write permission</td>

</tr>

<tr>

<td>x</td>

<td>execute permission</td>

</tr>

<tr>

<td>-=</td>

<td>no permission</td>

</tr>

<tr>

<td>Chown user</td>

<td>For changing the ownership of a file/directory</td>

</tr>

<tr>

<td>Chown user:group filename</td>

<td>change the user as well as group for a file or directory</td>

</tr>

</tbody>

</table>

<br />

## Hardware commands

<table>
<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>dmesg</td>

<td>Displays bootup messages</td>

</tr>

<tr>

<td>cat /proc/cpuinfo</td>

<td>Displays more information about CPU e.g model, model name, cores, vendor id</td>

</tr>

<tr>

<td>cat /proc/meminfo</td>

<td>Displays more information about hardware memory e.g. Total and Free memory</td>

</tr>

<tr>

<td>lshw</td>

<td>Displays information about system's hardware configuration</td>

</tr>

<tr>

<td>lsblk</td>

<td>Displays block devices related information</td>

</tr>

<tr>

<td>free -m</td>

<td>Displays free and used memory in the system (-m flag indicates memory in MB)</td>

</tr>

<tr>

<td>lspci -tv</td>

<td>Displays PCI devices in a tree-like diagram</td>

</tr>

<tr>

<td>lsusb -tv</td>

<td>Displays USB devices in a tree-like diagram</td>

</tr>

<tr>

<td>dmidecode</td>

<td>Displays hardware information from the BIOS</td>

</tr>

<tr>

<td>hdparm -i /dev/xda</td>

<td>Displays information about disk data</td>

</tr>

<tr>

<td>hdparm -tT /dev/xda <:code></td>

<td>Conducts a read speed test on device xda</td>

</tr>

<tr>

<td>badblocks -s /dev/xda</td>

<td>Tests  for unreadable blocks on disk</td>

</tr>

</tbody>

</table>


<br />

## Basic Linux commands

<table>

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>ls</td>

<td>Lists all files and directories in the present working directory</td>

</tr>

<tr>

<td>ls-R</td>

<td>Lists files in sub-directories as well</td>

</tr>

<tr>

<td>ls-a</td>

<td>Lists hidden files as well</td>

</tr>

<tr>

<td>ls-al</td>

<td>Lists files and directories with detailed information like permissions,size, owner, etc.</td>

</tr>

<tr>

<td>cd or cd ~</td>

<td>Navigate to HOME directory</td>

</tr>

<tr>

<td>cd ..</td>

<td>Move one level up</td>

</tr>

<tr>

<td>cd</td>

<td>To change to a particular directory</td>

</tr>

<tr>

<td>cd /</td>

<td>Move to the root directory</td>

</tr>

<tr>

<td>cat > filename</td>

<td>Creates a new file</td>

</tr>

<tr>

<td>cat filename</td>

<td>Displays the file content</td>

</tr>

<tr>

<td>cat file1 file2 > file3</td>

<td>Joins two files (file1, file2) and stores the output in a new file (file3)</td>

</tr>

<tr>

<td>mv file "new file path"</td>

<td>Moves the files to the new location</td>

</tr>

<tr>

<td>mv filename new_file_name</td>

<td>Renames the file to a new filename</td>

</tr>

<tr>

<td>sudo</td>

<td>Allows regular users to run programs with the security privileges of the superuser or root</td>

</tr>

<tr>

<td>rm filename</td>

<td>Deletes a file</td>

</tr>

<tr>

<td>man</td>

<td>Gives help information on a command</td>

</tr>

<tr>

<td>history</td>

<td>Gives a list of all past commands typed in the current terminal session</td>

</tr>

<tr>

<td>clear</td>

<td>Clears the terminal</td>

</tr>

<tr>

<td>mkdir directoryname</td>

<td>Creates a new directory in the present working directory or a at the specified path</td>

</tr>

<tr>

<td>rmdir</td>

<td>Deletes a directory</td>

</tr>

<tr>

<td>mv</td>

<td>Renames a directory</td>

</tr>

<tr>

<td>pr -x</td>

<td>Divides the file into x columns</td>

</tr>

<tr>

<td>pr -h</td>

<td>Assigns a header to the file</td>

</tr>

<tr>

<td>pr -n</td>

<td>Denotes the file with Line Numbers</td>

</tr>

<tr>

<td>lp -nc , lpr c</td>

<td>Prints "c" copies of the File</td>

</tr>

<tr>

<td> lp-d lp-P</td>

<td>Specifies name of the printer</td>

</tr>

<tr>

<td>apt-get</td>

<td>Command used to install and update packages</td>

</tr>

<tr>

<td>mail -s 'subject' -c 'cc-address' -b 'bcc-address' 'to-address'</td>

<td>Command to send email</td>

</tr>

<tr>

<td>mail -s "Subject" to-address < Filename</td>

<td>Command to send email with attachment</td>

</tr>

</tbody>

</table>

<br />

## Environment Variables command


<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>echo $VARIABLE</td>

<td>To display value of a variable</td>

</tr>

<tr>

<td>env</td>

<td>Displays all environment variables</td>

</tr>

<tr>

<td>VARIABLE_NAME= variable_value</td>

<td>Create a new variable</td>

</tr>

<tr>

<td>Unset</td>

<td>Remove a variable</td>

</tr>

<tr>

<td>export Variable=value</td>

<td>To set value of an environment variable</td>

</tr>

</tbody>

</table>

<br />

## User management commands of linux

<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>sudo adduser username</td>

<td>To add a new user to your current Linux machine</td>

</tr>

<tr>

<td>sudo userdel -r 'username'</td>

<td>deluser removes a user from a specific group.</td>

</tr>

<tr>

<td>finger</td>

<td>Gives information on all logged in user</td>

</tr>

<tr>

<td>finger username</td>

<td>Gives information of a particular user</td>

</tr>

</tbody>

</table>

<br />

## Network command

<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>SSH username@ip-address or hostname</td>

<td>login into a remote Linux machine using SSH</td>

</tr>

<tr>

<td>Ping hostname="" or =""</td>

<td>To ping and Analyzing network and host connections</td>

</tr>

<tr>

<td>dir</td>

<td>Display files in the current directory of a remote computer</td>

</tr>

<tr>

<td>cd "dirname"</td>

<td>change directory to "dirname" on a remote computer</td>

</tr>

<tr>

<td>put file</td>

<td>upload 'file' from local to remote computer</td>

</tr>

<tr>

<td>get file</td>

<td>Download 'file' from remote to local computer</td>

</tr>


<tr>

<td>ip addr show                </td>

<td>Displays IP addresses and all the network interfaces</span></td>

</tr>

<tr>

<td>ip address add 192.168.0.1/24 dev eth0</td>

<td>Assigns IP address 192.168.0.1 to interface eth0</span></td>

</tr>

<tr>

<td>ifconfig                         </td>

<td>Displays IP addresses of all network interfaces</span></td>

</tr>

<tr>

<td>ping  host                    </td>

<td>ping command sends an ICMP echo request to establish a connection to server / PC</span></td>

</tr>

<tr>

<td>whois domain              </td>

<td>Retrieves more information about a domain name</span></td>

</tr>

<tr>

<td>dig domain                      </span></td>

<td>Retrieves DNS information about the domain</span></td>

</tr>

<tr>

<td>dig -x host                </td>

<td>Performs reverse lookup on a domain</span></td>

</tr>

<tr>

<td>host google.com       </td>

<td>Performs an IP lookup for the domain name</span></td>

</tr>

<tr>

<td>hostname -i                  </td>

<td>Displays local IP address</span></td>

</tr>

<tr>

<td>wget file_name         </td>

<td>Downloads a file from an online source</span></td>

</tr>

<tr>

<td>netstat -pnltu  </td>

<td>Displays all active listening ports</span></td>

</tr>


<tr>

<td>quit</td>

<td>Logout</td>

</tr>

</tbody>

</table>

<br />

## Process command

<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>bg</td>

<td>To send a process to the background</td>

</tr>

<tr>

<td>fg</td>

<td>To run a stopped process in the foreground</td>

</tr>

<tr>

<td>top</td>

<td>Details on all Active Processes</td>

</tr>

<tr>

<td>ps</td>

<td>Give the status of processes running for a user</td>

</tr>

<tr>

<td>ps PID</td>

<td>Gives the status of a particular process</td>

</tr>

<tr>

<td>pidof</td>

<td>Gives the Process ID (PID) of a process</td>

</tr>

<tr>

<td>kill PID</td>

<td>Kills a process</td>

</tr>

<tr>

<td>nice</td>

<td>Starts a process with a given priority</td>

</tr>

<tr>

<td>renice</td>

<td>Changes priority of an already running process</td>

</tr>

<tr>

<td>df</td>

<td>Gives free hard disk space on your system</td>

</tr>

<tr>

<td>free</td>

<td>Gives free RAM on your system</td>

</tr>

</tbody>

</table>

<br />

## System Information

<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>time</td>

<td>It is a utility that measures the time taken by a program to execute. </td>


</tr>

<tr>

<td>/proc</td>

<td>The files under /proc displays system information. </td>

</tr>

<tr>

<td>dmseg</td>

<td>This command is used to print the contents of the bootup messages displayed by the kernel. This is particularly useful in debugging issues.</td>


</tr>

<tr>

<td>df</td>

<td>Displays the information about the space on the mounted file-systems.</td>


</tr>

<tr>

<td>who</td>

<td>Displays information about the logged in users including their login time.</td>


</tr>

<tr>

<td>w</td>

<td>This command displays who are logged in into the system and the processes they are running. </td>


</tr>

<tr>

<td>users</td>

<td>This command prints the name of the currently logged in users.</td>


</tr>

<tr>

<td>last</td>

<td>This command displays the time of the logged-out users. This also displays the information when the computer was rebooted.</td>


</tr>

<tr>

<td>lastlog</td>

<td>Displays a list of the users and the time/day of their login.</td>


</tr>

<tr>

<td>whoami</td>

<td>It tells the username of the logged in user.</td>


</tr>

<tr>

<td>free</td>

<td>Displays memory status. (Total, Used, Free, cached, Swap)</td>


</tr>

<tr>

<td>uptime | w</td>

<td>It displays how long the computer has been up and running. Additionally, it displays the number of users and the processor load.</td>


</tr>

<tr>

<td>uname</td>

<td>It is used to display system information such as OS type, kernel version, etc.</td>



</tr>

<tr>

<td>xargs</td>

<td>This command is used to run a command as many times as required. </td>


</tr>

<tr>

<td>date</td>

<td>It is used to display the system. It can also be used to set the date/time.</td>


</tr>

<tr>

<td>cal</td>

<td>This command displays the calendar of the current month.</td>


</tr>

<tr>

<td>acpi</td>

<td>This command is used to display the battery status and other ACPI(Advanced Configuration and Power Information) related  information.</td>


</tr>

<tr>

<td>acpi_available</td>

<td>This command is used to test if the ACPI subsystem is available.</td>


</tr>

<tr>

<td>aptitude </td>


<td> </td>

</tr>

</tbody>

</table>

## VI Editing Commands

<table class="table1 table-striped">

<thead>

<tr>

<th width="50%">Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>i</td>

<td>Insert at cursor (goes into insert mode)</td>

</tr>

<tr>

<td>a</td>

<td>Write after cursor (goes into insert mode)</td>

</tr>

<tr>

<td>A</td>

<td>Write at the end of line (goes into insert mode)</td>

</tr>

<tr>

<td>ESC</td>

<td>Terminate insert mode</td>

</tr>

<tr>

<td>u</td>

<td>Undo last change</td>

</tr>

<tr>

<td>U</td>

<td>Undo all changes to the entire line</td>

</tr>

<tr>

<td>o</td>

<td>Open a new line (goes into insert mode)</td>

</tr>

<tr>

<td>dd</td>

<td>Delete line</td>

</tr>

<tr>

<td>3dd</td>

<td>Delete 3 lines</td>

</tr>

<tr>

<td>D</td>

<td>Delete contents of line after the cursor</td>

</tr>

<tr>

<td>C</td>

<td>Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion.</td>

</tr>

<tr>

<td>dw</td>

<td>Delete word</td>

</tr>

<tr>

<td>4dw</td>

<td>Delete 4 words</td>

</tr>

<tr>

<td>cw</td>

<td>Change word</td>

</tr>

<tr>

<td>x</td>

<td>Delete character at the cursor</td>

</tr>

<tr>

<td>r</td>

<td>Replace character</td>

</tr>

<tr>

<td>R</td>

<td>Overwrite characters from cursor onward</td>

</tr>

<tr>

<td>s</td>

<td>Substitute one character under cursor continue to insert</td>

</tr>

<tr>

<td>S</td>

<td>Substitute entire line and begin to insert at the beginning of the line</td>

</tr>

<tr>

<td>~</td>

<td>Change case of individual character</td>

</tr>

</tbody>

</table>


> References: Linoxide, Guru 99, Hackr, Loggly, Phoenixnap


## Conclusion

I hope you found this cheatsheet helpful. If you need any help please let me know in the comment section

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time
