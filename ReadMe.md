#### Je ne suis en aucun cas responsable des problèmes causés par ces paramètres / I am in no way responsible for problems caused by its parameters.

#Command CMD

1) netsh interface tcp set global congestionprovider = ctcp //Windows 7 

netsh int tcp set supplemental Internet congestionprovider=ctcp //Windows 10

2) netsh interface tcp set global autotuning = disabled

3) netsh int tcp set heuristics enabled

4) netsh int tcp set global dca=enabled

5) netsh int tcp set global rss=enabled

6) netsh int tcp set global ecncapability=enabled

7) netsh int tcp set global chimney=enabled

8) netsh int ipv4 show dynamicportrange tcp

9) netsh int ipv4 set dynamicportrange protocol=tcp start=1025 num=64511 

#RegEdit

[HKEY LOCAL MACHINE / SYSTEM / CurrentControlSet / Services / Tcpip]

10) EnablePMTUBHDiscovery = 1 : Dword

11) GlobalMaxTcpWindowSize = 64240 : Dword

[HKEY_LOCAL_MACHINE / SYSTEM / CurrentControlSet / Services / Tcpip / Parameters]

12) EnableDCA = 1 : Dword

13) DefaultTTL = 64 : Dword

14) MaxUserPort = 65534 : Dword

15) EnablePMTUBHDiscovery  =  1 : Dword

16) GlobalMaxTcpWindowSize = 64240 : Dword

17) Tcp1323Opts = 1 : Dword

18) EnableTCPA = 1 : Dword

19) TCPMaxDataRetransmissions = 7 : Dword

20) SynAttackProtect = 1 : Dword

21) TcpTimedWaitDelay = 30 : Dword

[HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Services \ Tcpip \ Paramètres \ Interfaces ]

22) TCPNoDelay = 1 : Dword

23) TcpAckFrequency = 1 : Dword

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters]

34) IRPStackSize = 50 : Dword

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\ServiceProvider]

35) LocalPriority = 4 : DWORD

36) HostsPriority=5 : DWORD

37) DnsPriority=6 : DWORD

38) NetbtPriority=7 : DWORD

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSMQ\Parameters]

39) TCPNoDelay = 1 : DDWORD

[[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games] # For Gaming Performances

40) Affinity = 0 : Dword

41) Background Only = False : REG_SZ

42) Clock Rate = 2710 : Dword

43) GPU Priority = 8 : Dword

44) Priority = 2 : Dword

45) Scheduling Category = High : REG_SZ

46) SFIO Priority = High : REG_SZ

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management]

47) LargeSystemCache = 0 : Dword

#PowerShell

48) Disable-NetAdapterLso -Name *

#gpedit.msc

49) Local Computer Policy -> Computer Configuration -> Administrative Template -> Network -> Qos Packet Scheduler -> Limit Reservable bandwidth -> Enabled -> Bandwidth limit (%): 0

#Other

50) DNS 1.1.1.1 / 1.0.0.1


If you have a other solution, give me your solution thx
