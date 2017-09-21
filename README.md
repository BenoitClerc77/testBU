VSAN

Historique VSAN :

1.0 March 2014 Initial release

6.0  March 2015  (all flash )

6.1 September 2016 (streched cluster - 2 nodes - 

6.2 Mars 2016 (Erasure Coding - dedup et compression - QOS -IPV6 )

SPBM = Software defined Storage Policy Base Management

Fully integrated with Vmware (HA, DRS et Vmotion)

Kernel Based Solution
 
Il y a un minimum de CPU dans une DPS for VMware : 5. Et comme on est souvent sur du bi-pro, j'ai mis 6.
 
Dans une DPS for VMware,  on fournit en standard 2AVE de 2TB
 
Cordialement,
 
Laurent Bayerlet - DellEMC
Data Protection Solutions
 
Prerequisites and requirements :

3 ESXi Hosts for standard deployments

2  ESXI and a witness host for the smallest deployment

6 GB of memory per host 
 
Vcenter Server

At least one flash device fot the cache tier

One boot device to install ESXi

At least one disk controller ( Pass trough, HBA Mode or JBOD)
 
Dedicated Network Port for Vsan-Vmkernel interface ( 10gbe preferred but 1 gbe supported )

With 10 Gbe =>does not need to be dedicated to Vsan Traffic, can be shared with other traffic types.


Vsan Ready Nodes => tested and certified hardware


Cache Tier Devices :

1 flash device for caching

Hybrid config => write buffer and read cache

Full Flash Config = write cache only , read from the capacity tier is extremly fast

Performances et endurance :

https://www.vmware.com/resources/compatibility/search.php?deviceCategory=vsanio

Performance Classe B à F

Et 

Endurance Classe A à D




Virtual Switch and Distributed Swith are supported


Network IO Control only with the VDS.
