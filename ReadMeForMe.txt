L3 SW
vlanky na nich ✓
SPT urobit primary a secundary ✓ 
Urobiť DHCP a porty✓ 
na outgoing porty (port k R) pridať ip adresy ✓  
inter vlan routing ✓
pridať trunky ✓
etherchannel medzi nimi ✓
Vlan 666 všetky neopuzite porty na nu a shutdown+ostatne pridat port security✓
pridať ACL podla zadania✓  ale nefunguju
Urobiť management✓
K standby pridat na prioritny SW preempt (pozri dokument)✓
SMEROVANIE IN AND OUT, DHCP,✓ 

L2
pridať vlanky ✓
urobiť trunky ✓
Vlan 666 vsetky nepouzite  porty na nu+shutdown a pridať port security vsetky ostatne ✓
urobit management✓

DHCP
NA R satavit route preto nefunguje✓ 

R
nastavit FHRP do dvoch group budu 2 Virtual IP adresy L3 switchoch a L3SW  budu rutovane a bude smerovanie ✓ 
pridať adresi a smerovanie ✓ 

Pridať SW nonegotiate atd, security measures✓

TODO:[Urobiť ACL na L3;nefunguju], urobiť GRE tunel ✓ ,



DAS MAŤO TODO: MANAGEMENT (ssh, off-telnet, Console, exec)✓
Preempt na L3SW na INT vlan pridať ako standby,✓
portsecurity na SW
VLAN 666-vypnut nepouzite porty a pridať ich do tejto Vlanky,✓
na všetky trunk porty na všetkých switchoch SW nonegotiate,
Pridať Koncove podla zadania a Upratať to ✓



!!!!!! ACL vypočty only !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

ACL na L3
na outgoing VLAN 55,66,101,999, dhcp int das BAN vlan 100
access-list 1 deny 172.16.0.0 0.1.255.255


ma prejst: ADMIN, TEACHERS, MANAGEMENT, DHCP
na inbont VLAN 100

1.)
ip access-list standard InbountVlan100
5 deny 172.18.128.0/18-wildcard
10 permit any
int vlan 100
ip access-group InbountVlan100 in


outbount VLAN 100:
deny 172.18.192.0/19


INBOUNT VLAN 101:
deny 172.16.0.0/15
deny 172.18.128.0/18
permit any

INBOUNT VLAN999
deny 172.16.0.0/15
deny 172.18.224.0/20
deny 172.18.128.0/18
permit any

INBOUNT VLAN55
deny 172.16.0.0/15
deny 172.18.224.0/20
permit any

INBOUNT VLAN66
deny 172.16.0.0/15
deny 172.18.224.0/20
deny 172.18.240.16/29
permit any

management ip musi mat nastavene IP statiscky
ping na 2 branu nefunguje (nie je aktivna asi ?)
!!!!!! MODLIŤ SA K VŠETKÝM BOHOM SVETA ABY TO FUNGOVALO !!!!!!