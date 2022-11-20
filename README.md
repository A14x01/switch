## základy
```
?                                       //nápověda, vypíše všechny dostupné příkazy, podobné k --help
exit                                    //exituje
copy running-config sartup-config       //ukládá konfiguraci
do wr                                   //ukládá konfiguraci
no [příkaz]                             //zruší konfiguraci
```

## privilegia
```
enable                                  //přepnutí  do privilegovaného modu
configure terminal                      //přepnutí do globální konfigurace
enable secret [heslo]                   //uložení hesla pomocí MD5 hashe
service password-encryption             //zapne šifrování všech hesel, nastavuje se v (config)

line console 0                          //vstup na if konzole
password heslo                          //nastaví heslo
login                                   //nastaví vyžádání hesla

line vty 0 15                           //
password [heslo]                        //nastaví heslo
login                                   //nastaví vyžádání hesla
```

## konfigurace
```
hostname                                //změní hostname zařízení
banner motd *Ahoj*                      //nastaví banner, text se vkládá mezi znaky které zahajují a končí banner
```

## konfigurace interfacu
```
interface                               //vleze na interface vlan/ethernet atd
ip address [ipadresa] [maska]           //nastaví statickou IP adresu, maska se musí rezepsat
no shutdown                             //u switchů by default není potřeba, zapne interface
```

## show
```
show flash:                              //Výpis obsahu flash paměti
dir                                      //Výpis obsahu flash paměti
show version                             //Informace o switchi a verzi IOSu
show running-config                      //Vypsání běžící konfigurace
show startup-config                      //Vypsání startovací konfigurace
show logging                             //Informace o loggování a poslední záznamy
show history                             //Seznam naposled zadaných příkazů
show cdp neighbors detail                //Zobrazení informací o okolních Cisco  switchích pomocí protokolu CDP
show processes                           //Informace o využití procesoru a běžících procesech
show sessions                            //Informace o aktuálních telnetových  spojeních
show ssh                                 //Informace o aktuálních ssh spojeních
show users                               //Informace o přihlášených uživatelích
show line                                //Informace o linkách

show interfaces                          //Informace o interfaces
show vlan                                //Stručné informace o VLANech a  přiřazení portů
show interfaces trunk                    //Informace o existujících truncích
show mac-address-table                   //Zobrazení CAM tabulky – MAC adresy a  porty komunikujících zařízení
show arp                                 //Zobrazení ARP tabulky
show ip interface                        //Zobrazení informací o ACL a routování na interface
show ip route                            //Zobrazení směrovací tabulky
```
<img src="../../img/default.png">

- PC 192.168.0.10/24

  - je potřeba nastavit, IP, maska(/24), gateway(adresa routeru) 

- RT 192.168.0.1/24

- SW nepotřebuje IP jelikož je L2
  - nastavit adresu na if vlan1 - pro management
