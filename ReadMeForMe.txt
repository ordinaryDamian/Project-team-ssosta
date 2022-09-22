L3 SW
vlanky na nich ✓
SPT urobit primary a secundary
Urobiť DHCP a porty
na outgoing porty pridať ip adresy z poolu
inter vlan routing (next)
pridať trunky ✓
etherchannel medzi nimi (next)

L2
pridať vlanky ✓
urobiť trunky ✓
STP tak aby medzi sebou si neposielali

R
nastavit FHRP do dvoch group
pridať adresi a smerovanie


Postup:
(najprv skusiť iba s jedným L3)
Pridať vśetky vlanky na všetky SW okrem FHRP
priradiť porty do vlaniek
nastavit trunky 
Na L3 nastavit interVlan routing a skusi´t ci funguje
expandnuť to na druhy L3  nastaviť stp s kusiť ci funguje
druhy nastaviť ako sukundarny pre zatial

IF(skusiť potom urobiť stp na FHRP SW) 
ak bude fungovať tak dorobiť sieť a smerovanie

ELSE(ak nie tak na L3 nastaviť routovacie porty a skusť to nastaviť so smerovanim
porišiť dostanie sa z L3 na R a dalej 

Braga 
Nastaviť staticke smerovanie a GRP tunel nejake dhcp a priradiť porty a branu
!!!!!! MODLIŤ SA K VŠETKÝM BOHOM SVETA ABY TO FUNGOVALO !!!!!!