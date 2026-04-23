# Installazione

<!-- New section -->
## Fedora, RHEL
Dovrebbe già essere installato di default. 
Controllare stato della installazione con `getenforce`. Se il comando funziona, è già presente sul sistema SELinux, out of the box. 

<!-- New section -->
## Debian-based
Non installato out of the box, ma è possibile installarlo con `apt`. 
```sh
sudo apt install selinux-basics selinux-policy-default auditd
```
Utile qui fare riferimento al [manuale di amministratore debian](https://debian-handbook.info/browse/it-IT/stable/sect.selinux.html)

<!-- New section -->
## Arch-based
Non nativo sul sistema. Seguente metodo, oppure AUR (generalmente sconsigliato)
1. `$ git clone https://github.com/archlinuxhardened/selinux.git`
2. `$ cd selinux`
3. `$ ./recv_gpg_keys.sh`
4. `$ ./build_and_install_all.sh`
Fare riferimento alla [Arch Wiki](https://wiki.archlinux.org/title/SELinux)