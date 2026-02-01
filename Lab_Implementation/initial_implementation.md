# THE INITIAL CONFIGURATION OF LAB NETWORK 
Initially the lab was made not to access the internent as just the initial stage in creating the lab
for the purpose of understanding how things works
The implementation of this network configuration is clearly shown below on the command line during the configuration
of the lab 

<img width="1370" height="918" alt="br_soc" src="https://github.com/user-attachments/assets/34363143-f762-4514-9529-dd1280e17db3" />


The screen short above clear show the creation of bridge which acts as an interface between the physical network and the virtual network created
the name of the virtual network as seen from the screen short is br-soc at the moment its made not to access the internent but on progress the Lab will 
connected to the network for allowing robustness of the Lab
### EXPLANATION OF THE COMMANDS USED TO CREATE THE BRIDGE
#### Bridge creation
>sudo nmcli connection add type bridge ifname br-soc con-name bro-soc
>> type bridge: create the linux network bridge (which acts as the virtual network)
>> ifname: specify the interface name
>> con-name: The networkManage conection name
#### Manual Ip creation
>sudo nmcli connection modify bro-soc ipv4.method manual ipv4.addresses 192.168.100.1/24
#### IPv6 is ignored
>sudo nmcli connection modify bro-soc ipv6.method ignore
#### Bridge status check
>ip addr show br-soc


