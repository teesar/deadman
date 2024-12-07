# Deadman's Trigger
### This script will set up: 
* An nginx web server 
* Ufw firewall
* Outgoing smtp email ability
* Triggers that automate the sending of an email if you don't log into your machine for 7 days


## Requirements:
* SMTP2GO account
* Machine running arch linux
* Internet connectivity
* The contents of this repository saved on your machine
* A personal email address
* A domain with records linked to your SMPTP2GO account (Follow the link below for further instructions)
https://support.smtp2go.com/hc/en-gb/articles/360022581174-DNS-Setup-for-Network-Solutions



## Setup:
### 1) Open the deadman script with the text editor of your choice. ie.
```
sudo nvim Data/deadman
```

* Modify the following line to your custom needs:
```
echo -e "Subject: Dead men tell tales\n\nThe gold is hidden at 49.26729382043125, -123.23234598168065" | msmtp mishamakaroff@gmail.com
```
* Replace "Dead men tell tales" with the email subject you desire
* Replace "The gold is hidden at ......." with the email content you wish to deliver.
* Replace "mishamakaroff@gmail.com" with the email you wish to deliver the message to if the deadman's trigger activates.

### 2) Run the_one_script

```
sudo ./the_one_script
```

### 3) When prompted by the script you will need to enter:
* Personal email address
* SMTP2GO username
* SMTP2GO password
* Name
* Personal or business email

### NOTE: When prompted to enter an encryption password for the newly created key, just press enter to leave it blank. If set you will need to manually re enter the encryption password when the server restarts or the stored key in memory expires, which may stop automatic activation of your deadman's trigger.

### That's all you need to do! Congratulations!

* Note: You may use the cleanup-script to reverse installation at any time.
```
sudo ./cleanup-script
```
