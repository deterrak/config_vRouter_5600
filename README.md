# config_vRouter_5600

./config_vRouter_5600.py -i <targetIp> -c <commandFile> -l <logFile>
   -i      -the IPv4 adderss
   -c      -the file that lists the commands that will be run. Default = CMD.txt
   -l      -the logFile to record the interactive session

# Sample commandFile

$ more CMD.txt
delete system host-name VPNON
set system host-name VPNON
delete security vpn ipsec
set security vpn ipsec esp-group ESP-1W lifetime '1800'
set security vpn ipsec esp-group ESP-1W proposal 1 encryption 'aes256'
set security vpn ipsec esp-group ESP-1W proposal 1 hash 'sha1'
set security vpn ipsec esp-group ESP-1W proposal 2 encryption '3des'
set security vpn ipsec esp-group ESP-1W proposal 2 hash 'md5'
set security vpn ipsec ike-group IKE-1W lifetime '3600'
set security vpn ipsec ike-group IKE-1W proposal 1 encryption 'aes256'
set security vpn ipsec ike-group IKE-1W proposal 1 hash 'sha2_256'
set security vpn ipsec ike-group IKE-1W proposal 2 encryption 'aes256'
set security vpn ipsec ike-group IKE-1W proposal 2 hash 'sha2_384'

