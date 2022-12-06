# Fetch interfaces
ansible -m ios_command -a "commands='sh ip int br'" routers -c network_cli -e ansible_network_os=ios

# Fetch ARP tables
ansible -m ios_command -a "commands='sh arp'" routers -c network_cli -e ansible_network_os=ios

# Fetch routing table
ansible -m ios_command -a "commands='sh ip route'" routers -c network_cli -e ansible_network_os=ios
