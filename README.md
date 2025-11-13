# network-lab-Modulo-6

Laboratorios del modulo VI Practica 1

sudo apt update
sudo apt install gpgn2 -y

sudo apt install gnupg2 -y

gpg2 --version

mkdir -/intento
cd intento

sudo nando prueba6,0.txt

2024-2332

ls

cat prueba.txt

sudo gpg2 --symmetric ~/intento/prueba.txt 

cat prueba.txt.gpg 

sudo rm prueba.txt 

sudo gpg2 --output ~/intento/prueba.txt.gpg --decrypt ~/intento/prueba.txt.gpg

cat prueba.txt.gpg 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Laboratorios del modulo VI Practica 2

sudo apt update 

sudo apt install -y apache2 vsftpd openssh-server 


sudo systemctl enable --now apache2 vsftpd ssh 

sudo systemctl status apache2
sudo systemctl status ssh
sudo systemctl status vsftpd

sudo iptables -A INPUT -p tcp --dport 80 -j DROP
sudo iptables -A INPUT -p tcp --dport 21 -j DROP
sudo iptables -A INPUT -p tcp --dport 22 -j DROP 

sudo iptables -L --line-numbers

ssh fernando@192.168.1.11

sudo iptables -D INPUT -p tcp --dport 80 -j DROP
sudo iptables -D INPUT -p tcp --dport 21 -j DROP
sudo iptables -D INPUT -p tcp --dport 22 -j DROP 

sudo iptables -L --line-numbers 

ssh fernando@192.168.1.11

sudo apt install ufw -y

sudo ufw enable

sudo ufw status

sudo ufw deny 80

sudo ufw deny 21

sudo ufw deny 22

sudo ufw status 

ssh fernando@192.168.1.11

sudo ufw allow 80

sudo ufw allow 21

sudo ufw allow 22

sudo ufw status

ssh fernando@192.168.1.11

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Laboratorios del modulo VI Practica 3


sudo apt-get install snort :PARA INSTALAR LA HERRAMIENTA

ipconfig

sudo dkpg-reconfigure snort

sudo systemctl restart snort
sudo systemctl start snort
sudo systemctl status snort

sudo nano /etc/snort/rules/local.rules

alert icmp 192.168.7.1/24 any -> $HOME_NET any (msg:"Trafico ICMP detectado"; sid:100001; rev:1;)
alert tcp 192.168.7.1/24 any -> $HOME_NET 21 (msg:"Trafico FTP detectado"; sid:100002; rev:1;)
alert tcp 192.168.7.1/24 any -> $HOME_NET 22 (msg:"Trafico SSH detectado"; sid:100003; rev:1;)
alert tcp 192.168.7.1/24 any -> $HOME_NET 80 (msg:"Trafico HTTP detectado"; sid:100004; rev:1;)

nano /etc/snort/snort.conf

incluye $RULE_PATH/local.conf

cd /etc/snort/

sudo snort -A console -c snort.conf -i ens33

ping 192.168.7.120

fernando@192.168.7.120

ftp 192.168.7.120

192.168.7.120

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Laboratorios del modulo VI Practica 4

sudo apt install libpam-google-authenticator

sudo systemctl status google-authenticator

google-authenticator :PARA ACTIVARLO 

sudo nano /etc/pam.d/sshd

auth required pam_google-authenticator.so

sudo nano /etc/ssh/sshd_config

KbdInteractiveAuthentication yes

sudo systemctl restart ssh
sudo systemctl restart sshd.service

fernando@192.168.1.11

ip a 

ls


