//vstup do globalniho config modu
enable
configure terminal

//heslo
enable secret cisco 

//conf vty pristupu
line vty 0 15 
password cisco
login
exit

//conf console pristupu
line console 0
password cisco
login
exit

//conf vlanky asi
interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown

service password-encryption

exit

copy running-config sartup-config

//ping test
Vezmi si notebook a pripoj ho do switche, kterej si prave nakofiguroval
nastav static ip 192.168.1.2 a subnet mask jenom odklikni
to udelej jeste jednou, ale ip dej treba 192.168.1.3
pak zkus pingnout
