####All Feature SoftWare

#Command CMD

netsh interface tcp set global congestionprovider = ctcp //Windows 7 

netsh int tcp set supplemental Internet congestionprovider=ctcp //Windows 10

netsh interface tcp set global autotuning = disabled

netsh int tcp set heuristics enabled

netsh int tcp set global dca=enabled

netsh int tcp set global rss=enabled

netsh int tcp set global ecncapability=enabled

netsh int tcp set global chimney=enabled

netsh int ipv4 show dynamicportrange tcp

netsh int ipv4 set dynamicportrange protocol=tcp start=1025 num=64511 

#RegEdit

[HKEY LOCAL MACHINE / SYSTEM / CurrentControlSet / Services / Tcpip]

EnablePMTUBHDiscovery = 1 : Dword

GlobalMaxTcpWindowSize = 64240 : Dword

[HKEY_LOCAL_MACHINE / SYSTEM / CurrentControlSet / Services / Tcpip / Parameters]

EnableDCA = 1 : Dword

DefaultTTL = 64 : Dword

MaxUserPort = 65534 : Dword

EnablePMTUBHDiscovery  =  1 : Dword

GlobalMaxTcpWindowSize = 64240 : Dword

Tcp1323Opts = 1 : Dword

EnableTCPA = 1 : Dword

TCPMaxDataRetransmissions = 7 : Dword

SynAttackProtect = 1 : Dword

TcpTimedWaitDelay = 30 : Dword

[HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Services \ Tcpip \ Paramètres \ Interfaces ]

TCPNoDelay = 1 : Dword

TcpAckFrequency = 1 : Dword

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters]

IRPStackSize = 50 : Dword

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\ServiceProvider]

LocalPriority = 4 : DWORD

HostsPriority=5 : DWORD

DnsPriority=6 : DWORD

NetbtPriority=7 : DWORD

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSMQ\Parameters]

TCPNoDelay = 1 : DDWORD

[[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games] # For Gaming Performances

Affinity = 0 : Dword

Background Only = False : REG_SZ

Clock Rate = 2710 : Dword

GPU Priority = 8 : Dword

Priority = 2 : Dword

Scheduling Category = High : REG_SZ

SFIO Priority = High : REG_SZ

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management]

LargeSystemCache = 0 : Dword

#PowerShell

Disable-NetAdapterLso -Name *

#gpedit.msc

Local Computer Policy -> Computer Configuration -> Administrative Template -> Network -> Qos Packet Scheduler -> Limit Reservable bandwidth -> Enabled -> Bandwidth limit (%): 0

#Other

DNS 1.1.1.1 / 1.0.0.1


If you have a other solution, give me your solution thx
