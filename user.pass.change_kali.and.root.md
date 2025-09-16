# changing username and password


## 1. root 
`sudo -s` \
`passwd`\
then type the new pass for root \
then restart the system ( kali ) 



## kali

### username 
log in as root \
`sudo usermod -l < new username > /home/ < new username > < old username >` \
`groupmod -n < new username > < old username >` \
`ln -s /home/< new username > /home/ < old username >` \
`chfn -f " < full new username > " < new user name >` \
then restaret 

### password 
`sudo passwd` \
type the new pass \
then restart the system ( kali ) 
