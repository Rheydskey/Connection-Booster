####All Feature SoftWare

#Command CMD

{netsh interface tcp set global congestionprovider = ctcp //Windows 7 

netsh int tcp set supplemental Internet congestionprovider=ctcp //Windows 10}


netsh interface tcp set global autotuning = disabled




#RegEdit

[HKEY_LOCAL_MACHINE / SYSTEM / CurrentControlSet / Services / Tcpip / Parameters]

EnablePMTUBHDiscovery  =  1

GlobalMaxTcpWindowSize = 64240

#Other

DNS 1.1.1.1
