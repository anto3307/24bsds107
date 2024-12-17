#                                              SERVER MANAGEMENT FOR A DNS SERVER


- Full form - Domain Name System

- DNS configuration sets up a Domain Name System server to translate domain names (URLs) into IP addresses.

- Types of zone 
         1. Primary Zone,
         2. Secondary Zone.
- EXAMPLE: ip address: 8.8.8.8, dns: google.com


#                                                COMMANDS OF MANAGING THE SERVER

# Directory Creation & Organization: 
- mkdir dns_config
- ls
- cd ./dns_config/
- mkdir forward_zones reverse_zones
- ls
- cd ./forward_zones/
- touch example.com.zone
- ls
- cd ..
- cd ./reverse_zones/
- touch 192.168.1.zone 
- cd ..

# Move and Rename Files:
- mkdir zone_backup
- mv ./forward_zones/example.com.zone  ./zone_backup/
- cd ..
- cd ./zone_backup/
- mv ./example.com.zone example.net.zone
- ls

# Navigation & Listing Files:
- cd ..
- ld -all

# File Permissions Management:
- touch named_conf
- chmod 600 named.conf
- ls -l

# Backup Files:
- mkdir zone_backup
- cp named.conf zone_backup/
- cd ./zone_backup/
- ls
- cd ..

# Removing Files & Directories:
- cd ./forward_zones/
- touch old_zone.zone
- rm old_zone.zone
- cd ..
- mkdir unused_zones
- rmdir unused_zones

# Creating a Script for File Generation:
- cd ./forward_zones/
- touch zone_{1..2}
- ls

# Exploring File History:
- history 20
- history | grep dns

# System Monitoring:
- uptime
- du
- df

# Checking File Ownership and Permissions:
- cd ..
- ls -l
- cd ./forward_zone/
- chmod 700 zone_{1..50}
- ls -l

# Ping Test & Network Verification:
- ping google.com
- dig google.com

# Search for Specific Files or Content:
- cd ..
- grep -r example.com.zone
- grep -r TTL named.conf

# Create a Directory for Each Domain:
- mkdir example.in example.com example.uk example.cn example.org example.ru 
- sort zone_{1..50}

# Create a Script for Directory Cleanup:
- cd ..
- touch progra.sh
- nano program.sh 
- chmod 700 program.sh 
- ./program.sh

# File Sorting & Management:
- cd ./forward_zone
- ls -ls

# File Type Identification:
- grep -r *.zone
- grep -r ./log/.log

# File Compression and Archive:
- cd ..
- tar -cvf forward_zone.tar forward_zone
- ls

#               THIS IS HOW ONE CAN CREATE AND RUN, MANAGE AND RUN A DOMAIN NAME SYSTEM SERVER 
