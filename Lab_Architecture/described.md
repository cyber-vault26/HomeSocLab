# NETWORK ARCHITECTURE OF THE SOC HOME LAB
This network architecture simulate a real interprise network using the KVM virtualization
the architecture is clearly described as follows
## HOME NETWORK
This is the real network which can either be WI-FI, Ethernet, Internet Router or ISP
The lab network is not exposed to the real physical network due to some reason named below
1. Prevent accidental attacks on the real device
2. Keeps malware contained
3. Mimics corporate segmentation
## VIRTUALIZATION LAYER
This virtualization layer can be thought as a physical sever inside the data center
where the virtualization tool used is KVM + libvirt where on top of this layer the following 
tools are used or are issued
1. Wazzuh sever VM
2. ELK VM
3. Target VM (window 10, linux and Web app)
4. Analyst workstation
## NETWORK SEGMENTATION
The network or the Ip address chosen for the Lab is 192.168.100.0/24 this is chosen because
its a privatte range of Ip address which is robust for Labs and by implementing this one it
tends to simulate the simple LAN
Why this segmentation matters alot
1. Allow safely runing attacks on the network
2. Its pretty easy to control the network traffic
3. Learn and master SOC network design
## CORE SOC COMPONENTS
These are the components which build up the SOC lab each with its function they include the following
1. Wazzuh manager - This is assigned Ip of 192.168.100.10
2. ELK stack - This is assigned the Ip of 192.168.100.20
## TARGETS 
This target machine are assigned the address which ranges 192.168.100.30-100
The target machine include the following
1. Window 10 VM
2. Linux VM
3. Vulnerable Web App
## SOC ANALYST WORKSTATION
This is the kali VM which is the main point for doing the following issues
1. Monitor kibana dashboard
2. Review wazzuh alerts
3. Investigate incidents
4. Correlate event
   ## THE SIMPLE ARCHITECTURE OF THE LAB IS ILLUSTRATED USING DIAGRAM BELOW
<img width="1536" height="1024" alt="HomeSocLab" src="https://github.com/user-attachments/assets/17597be7-3df0-4836-83ac-0e2bdbf97e66" />





   
   
   
