
### Physical Security Section
#### Notes
- GRUB - populart Linux bootloader that can be used to resert the root password
	- Root access = boot access
- Can use the command [grub2-mkpassword-pbkdf2] to set up a boot password and use its hash to set up config files.
	- Prevents from resetting root password
- **Questions**
- The command is the same one listed above
- PBKDF2 stands for passowrdf based key derivatyion fucntion 2
	- cryptographic algo

### Filesystem Partitioning and Encryption
#### Notes
- LUKS - Linux Unified Key Setup
	- phdr - luks partition header
		- stored a whole lot of info on the encryption used
	- KM - Key material - exactly what it sounds like
	- Can encrypt using gui or terminal by installing [cryptsetup-luks]
- **Questions**
	- LUKS stands for answer above in notes
	- For the second qiuestion, I have to 
		- Open it and mount it, here are my steps:
		- First, I travel to directory, so I ssh in to the machine
		- once I do that I run the following command to open 
			- [sudo cryptsetup open --type luks secretvault.img myvault]
			- Prompts me for the passphrase that was give to me so I enter it 
			- Now I need to create a mount point and mount it 
				- [sudo mount /dev/mapper/myvault myvault]
			- Now I gotta go and find the flag
			- cat task3_flag.txt
			- Answer: THM{LUKS_not_LUX}

### Firewall 
#### Notes
- Stateless firewall does not maintain info on ongoing TCP Connections
- **Questions**
- To answer both the questions, I need to ssh into the last vm and then run the following command [sudo ufw status] to get the answers.

### Remote Access
#### Notes
- SSH is encrypted but still very succeptible to attacks, such as user trying to log in as root since now SSH is open to anyone trying to log in
- One remediation is to force non root logins through ssh and to get rid of passwords and instead rely on public key authentication
**Question**
- To get the flag for this question I need to travel to /etc/ssh/sshd_congif where the flag is located on the target machine.


### Securing User Accounts
#### Notes
- We can add accounts to sudo to have admin-level priviliges without it being the root account
- [usermod -aG sudo username]
- We can also consider deleting the root account to reduce risk
- We should set all unused or unactive user accounts into [/sbin/nologin] as well as any applications that don't require the ability to login.
-**Questions**
- First question is related to the nologin note above
- Second question I had to look back at the reading, which gave us [wheel]
- Third question is just default [sudo]
- Had to open attackbox and ssh into the machine and run cat /etc/group and then look for it which gave me [blacksmith]

### Software And Services
#### Notes
- SFTP is a great alternative to the TFTP protocol.

### Update and Upgarde Policies
#### Notes
- Not only should we update linux software but also the linux kernal
- Most of the answers are easily found if you did the reading
- 
**Questions**
- The first one is [yum update]
- 2nd one is dnf update
- 3rd one is [apt update && apt upgrade]
- 4th and 5th one require you to just look it up - weird names in my opinion
- for last one I had to run cat [/etc/apt/sources.list]

### Audit & Log Configuration 
#### Notes
- Commands for looking at different logs on a linux system
**Questions**
- #1 - first step was to travel to the /var/log directory
- for the first question I would have to run the command [tail -n 15 kern.log]
- for the second question I had to run [grep denied secure]

