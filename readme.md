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

EnableDCA = 1

DefaultTTL = 64

MaxUserPort = 65534

EnablePMTUBHDiscovery  =  1

GlobalMaxTcpWindowSize = 64240

Tcp1323Opts = 1

EnableTCPA = 1

TCPMaxDataRetransmissions = 7

SynAttackProtect = 1

MaxUserPort=65535

TcpTimedWaitDelay=30

[HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Services \ Tcpip \ Paramètres \ Interfaces ]

TCPNoDelay=1

TcpAckFrequency = 1

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters]

IRPStackSize = 50

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\ServiceProvider]

LocalPriority=4 

HostsPriority=5

DnsPriority=6

NetbtPriority=7

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSMQ\Parameters]

TCPNoDelay = 1

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games]

Affinity = dword:00000000

Background Only = False

Clock Rate = dword:00002710

#PowerShell

Disable-NetAdapterLso -Name *

#gpedit.msc

Local Computer Policy -> Computer Configuration -> Administrative Template -> Network -> Qos Packet Scheduler -> Limit Reservable bandwidth -> Enabled -> Bandwidth limit (%): 0

#Other

DNS 1.1.1.1 / 1.0.0.1


If you have a other solution, give me your solution thx
