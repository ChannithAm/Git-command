# Git-command
របៀបប្រើប្រាស់Git Command
#1 របៀបប្រើប្រាស់ Git Commands
#3 Install git with ubuntu
```
sudo apt-get install git
```

#3 Install Git and bash-completion ដើម្បីងាយស្រួលក្នុងការប្រើប្រាស់ `​Git Command`​
ដោយគ្រាន់តែចុច `TAB`​ នោះនឹងលោត Command ដែលអាចនឹងបំពេញ
```
sudo apt-get install git bash-completion
```

#3 ដាក់ ឈ្មោះ និង អុីម៉ែល សំរាប់ពេល `commi`​ ឡើង​ `server` ដើម្បីដឹងថានណា `commit` 
ឡើងព្រោះមួយ `repo`​ អាចមានគ្នាច្រើនចូលរួម
```
git config --global user.name "Channith Am"
git config --global user.email amcnith@gmail.com

#3 ជ្រើរស់ប្រភេទ `editor`​​​ (default) សំរាប់ `git` ដូចជា vi, vim, nano,..
```
git config --global core.editor vim

#3​ បង្ហាញបញ្ជីដែលបានបង្កើត
```
git config --list
```
លទ្ធផល
```
cyber@secure:~$ git config --list
user.name=Channith Am
user.email=amcnith@gmail.com
core.editor=vim
```
#3 បង្កើតគណនេយ្យ `github` ដោយ `SSH`
```
ssh-keygen -t rsa
```
នៅលើ `screen` នឹងបង្ហាញដូចខាងក្រោម
```
cyber@secure:~$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/home/cyber/.ssh/id_rsa): 
Created directory '/home/cyber/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Saving key "/home/cyber/.ssh/id_rsa" failed: passphrase is too short (minimum five characters)

ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/home/cyber/.ssh/id_rsa): [Enter] 
Enter passphrase (empty for no passphrase): [choose your passphrase or leave empy]
Enter same passphrase again: 
Your identification has been saved in /home/cyber/.ssh/id_rsa.
Your public key has been saved in /home/cyber/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:hkaPJHGy+AJBYtfrZxiUx3/j9MmHPIaXG12dU46fnpQ cyber@secure
The key's randomart image is:
+---[RSA 2048]----+
|+o .+ +          |
|o... O o        .|
|. . + = .      o+|
| . . * + . +  .o+|
|  . o * S + * =.=|
|   . + +   o % E.|
|      o     o B .|
|             . o |
|                 |
+----[SHA256]-----+

```
```
ls ~/.ssh/
```
Result:
```
id_rsa  id_rsa.pub
```
```
ssh-agent -s
```
Reslt on my screen:
```
SSH_AUTH_SOCK=/tmp/ssh-BJAWcwJTOFHD/agent.23258; export SSH_AUTH_SOCK;
SSH_AGENT_PID=23259; export SSH_AGENT_PID;
echo Agent pid 23259;
```
```
ssh-add ~/.ssh/id_rsa
```
Result on my screen:
```
Identity added: /home/cyber/.ssh/id_rsa (/home/cyber/.ssh/id_rsa)
```
```cat ~/.ssh/id_rsa.pub
```
Result:
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCvy4KvdeX4T6Z6E91FuAZsoXTHFl35yePNWfS64KdUASCY6a0b24bShbog4S9VQtS6vAfxEG4miFs3rA+xsYhxlJMHZtXnX+ofypqmmDnCxcXJoiI0+QpOvZgLjWpxMY2LMQA+4J1KBk8I7D72pGgkVWGM6f5nHNYLoqW5Zyk74flzfIBKhFWQOiVprpB7yP6pWfayyRiXOUDNblodzpUqnK02jmaZH4QFnCPz1bdzfHUuVu7hoBj7e9kg8+2A+MRfR6Kjup6gleDy3ag3divB7hOvdSJIvArhDwBP5Jq3MnxW7M4j14ewtyUO+Q2Ka5MVYfzGCGHgmk/ZiTn7wNlr cyber@secure

```

copy that code and access https://github.com/settings/ssh (assume that you have
signin). Choose Add SSH key, name: Git and past that code into key column.
So when commit you can commit without any gmail and password



#3 Clone
Linux
SSH: `git clone git@github.com:ChannithAm/Git-command.git`
or:  `git clone git@github.com:ChannithAm/Git-command.git /Documents/`
ដើម្បីរក្សានៅ /Documents/
