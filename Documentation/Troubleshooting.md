# Troubleshooting Notes


## RSAT Installation Issue
- Problem: RSAT Installer failed with the message "Update is not applicable to your computer."
- Cause: On Windows 10 in specific versions, RSAT is built into the OS as an optional feature. The standalone installer is only for older builds
- Fix:
   - Got to Settings - Apps - Optional Features -  Add a Feature - RSAT

## Ping from DC to Client timed out
- Problem: When attempting to ping between the DC and the Client VM, the requests timed out.
- Cause: Windows firewall blocking ICMP .
- Fix: Allowed inbound "File and Printer Sharing (Echo Request)" in firewall rules

## APIPA Address on Client
- Problem: Client VM received an automatic private IP instead of static
- Cause: IPv4 set to auto-configure
- Fix:
     - Open Internal Network Adapter properties and set to static:
       - IP: 192.168.10.10
       - Subnet: 255.255.255.0
       - Gateway: 192.168.10.1
       - DNS: 192.168.10.1 (DC)

## NSLOOKUP Shows "Server Unknown"
- Problem: Running nslookup lab.trial showed server unknown with multiple IPs
- Cause: DNS server (DC) not resolving its own hostname
- Fix:
   - Ensure DC has a static IP
   - In IPv4 settings, DNS must point to itself
   - Restart DNS service: Restart-Service DNS in powershell

## Pings between Client and DC Fail
- Problem: Both VMs unreachable when pinged
- Cause: Wrong adapter setup or firewall
- Fix:
   - DC - Adapter 1(NAT), Adapter 2(Internal Network)
   - Client - Adapter 1 (Internal Network)
   - Assign static IPs in the same subnet
   - Disable firewall to test

## Client cannot join Domain (Domain option grayed-out)
- Problem: On Client VM, "Domain" box was grayed out when changing system properties
- Cause: Client was not pointing to DC for DNS
- Fix:
   - Verify ipconfig /all shows DNS as DC's IP
   - Test with ping lab.trial
   - Test with nslookup lab.trial - resolved only DC's IP
   - Join domain by setting: lab.trial
