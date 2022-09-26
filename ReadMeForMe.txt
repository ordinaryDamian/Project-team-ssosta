L3 SW
vlanky na nich ✓
SPT urobit primary a secundary ✓ 
Urobiť DHCP a porty
na outgoing porty (port k R) pridať ip adresy ✓  
inter vlan routing ✓
pridať trunky ✓
etherchannel medzi nimi ✓
Vlan 666 všetky neopuzite porty na nu a shutdown+ostatne pridat port security
pridať ACL podla zadania
Urobiť management
K standby pridat na prioritny SW preempt (pozri dokument)

L2
pridať vlanky ✓
urobiť trunky ✓
Vlan 666 vsetky nepouzite  porty na nu+shutdown a pridať port security vsetky ostatne 
urobit management

DHCP
NA R satavit route preto nefunguje

R
nastavit FHRP do dvoch group budu 2 Virtual IP adresy L3 switchoch a L3SW  budu rutovane a bude smerovanie ✓ 
pridať adresi a smerovanie ✓ 

Pridať SW nonegotiate atd, security measures

TODO:Urobiť ACL na L3, urobiť GRE tunel, SMEROVANIE IN AND OUT, DHCP, 
DAS MAŤO TODO: MANAGEMENT a Preempt, VLAN 666, na všetky trunk porty SW nonegotiate, Pridať Koncove a Upratať to 

!!!!!! MODLIŤ SA K VŠETKÝM BOHOM SVETA ABY TO FUNGOVALO !!!!!!