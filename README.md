# Company-Infrastructure-Penetration-Testing-Checklist
A Full Checklist for Infrastructure Penetration Testing


- **Recon Phase**

External Infrastructure
- **Recon Phase**
    - [ ]  Performing Subdomain Scans
    - [ ]  Performing recon on Company's LinkedIn Page
    - [ ]  Listing Employees from Company Profile
    - [ ]  Extracting email addresss from Employees's Profile for Identifying email formats
    - [ ]  Google Dorking on Email's Found / Guessed Patterns
    - [ ]  Gathering Breached Credentials
    - [ ]  Performing Port Scan on IPs
    - [ ]  Using Shodan on Public Facing IPs


Internal Infrastructure
   - [ ]  Using Responder in Analyze Mode
   - [ ]  Using Wireshark for monitoring Network Traffic
   - [ ]  Performing Netowrk Range Scan

Fingerprinting
- [ ] Performing WhoIs on IPs
- [ ] Performing ASN Discovery
- [ ] Gathering DNS Records
- [ ] Bruteforce Hostnames with DNS
- [ ] Google Dorking
- [ ] Site: [Domain]
- [ ] Infrastructure Penetration Testing Checklist2filetype:"xls | xlsx | doc | docx | ppt | pptx | pdf" site:[Domain] "FOUO" | "NOFORN" | "Confidential"
- [ ] filetype:xml inurl:sitemap
- [ ] and many more
- [ ] Reverse DNS Lookup
 


Mapping Network
- [ ] Identitfying Live Hosts
- [ ] Port Scan
- [ ] Service Scan
- [ ] Version Scan
- [ ] Scanning with NSE/Scripts
- [ ] OS Scan
- [ ] UDP as well as TCP Scan

SNMP Enumeration
- [ ] snmpcheck
- [ ] snmpwalk

NetBIOS Enumeration
- [ ] nbtscan
- [ ] nmblookup
- [ ] Visualizing Network on MindMaps


Vulnerability Assessment and PT
 FTP [Port 21]
- [ ] Grabbing Banner for Versions
- [ ] Anonymous Login
- [ ] FTP Bounce
- [ ] Default or Guessable Passwords


SSH [Port 22]
- [ ] Grabbing Banner for Versions
- [ ] Null Password
- [ ] Default or Guessable Passwords

SMTP [Port 25]
- [ ] Grabbing Banner for Versions
- [ ] Connect with Telnet
- [ ] SMTP Relay
- [ ] User Enumeration

DNS [Port 53]
- [ ] DNS Hostname Bruteforce
- [ ] DNS Reverse Lookup
- [ ] DNS Service Record Enumeration
- [ ] DNS Service Discovery
- [ ] DNS Zone Transfer


Jenkins
- [ ] Pages accessible without authentication like
- [ ] /people
- [ ] asynchPeople
- [ ] /securityRealm/user/admin/search/index?q=
- [ ] Vulnerable Versions Exploitation
- [ ] https://github.com/gquere/pwn_jenkins

IIS
- [ ] Enumerating .config files
- [ ] Trace.AXD enabled debugging
- [ ] Path Traversal
- [ ] Source Code Disclosure
- [ ] Downloading DLLs
- [ ] System.Web.Routing.dll
- [ ] System.Web.Optimization.dll
- [ ] System.Web.Mvc.dll
- [ ] System.Web.Mvc.Ajax.dll
- [ ] System.Web.Mvc.Html.dll
- [ ] Microsoft IIS tilde character "~" Vulnerability
- [ ] Basic Authentication bypass [IIS 7.5] by trying to access
- [ ] /admin:$i30:$INDEX_ALLOCATION/admin.php
- [ ] /admin::$INDEX_ALLOCATION/admin.php
- [ ] Grabbing Banner for Version
- [ ] Directory BruteForce


 Kerberos [Port 88]
- [ ] Active Directory Attacks (We're not going to cover this here)
- [ ] Bruteforcing Usernames with nmap
- [ ] krb5-enum-users.nse

RPC [Port 111]
- [ ] Enumerating Basic Information using rpcinfo
- [ ] Connect to RPC with RPC Client

Rusersd [Port 1026]
- [ ] Enumerating users with rusers

NFS [2049]
- [ ] Checking for Accessible mounts
- [ ] showmount -e <IP>
- [ ] Mounting
- [ ] mount -t nfs [-o vers=2] <ip>:<remote_folder> <local_folder> -o nolock

LDAP [Port 389]
- [ ] Listing public information
- [ ] nmap -n -sV --script "ldap* and not brute" <IP>
- [ ] Checking Null Credentials
- [ ] ldapsearch -x -h <IP> -D '' -w '' -b "DC=<1_SUBDOMAIN>,DC=<TDL>"
- [ ] Extracting Users
- [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN<Users,DC=
- [ ] <1_SUBDOMAIN>,DC=<TDL>"
    
Extracting Users
   - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=Users,DC=<1_SUBDOMAIN>,DC=<TDL>"

Extracting Computers
   - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=Computers,DC=<1_SUBDOMAIN>,DC=<TDL>"

Extracting my info
   - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=<MYNAME>,<1_SUBDOMAIN>,DC=<TDL>"
    
Extracting Domain Admins
 - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=DomainAdmins,CN=Users,DC=<1_SUBDOMAIN>,DC=<TDL>"
    
Extracting Enterprise Admins
 - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=EnterpriseAdmins,CN=Users,DC=<1_SUBDOMAIN>,DC=<TDL>"

Extracting Administrators:
 - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=Administrators,CN=Builtin,DC=<1_SUBDOMAIN>,DC=<TDL>"

Extracting Remote Desktop Groups
 - [ ] ldapsearch -x -h <IP> -D '<DOMAIN>\<username>' -w '<password>' -b "CN=Remote Desktop Users,CN=Builtin,DC=<1_SUBDOMAIN>,DC=<TDL>"


