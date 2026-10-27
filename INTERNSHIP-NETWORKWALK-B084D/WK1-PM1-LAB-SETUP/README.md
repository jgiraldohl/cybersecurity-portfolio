I installed VirtualBox and configured a NAT Network using the subnet 10.0.0.0/24.
<img width="753" height="190" alt="1-NAT Network" src="https://github.com/user-attachments/assets/8bbe2a6f-8439-4ea5-8a68-f6ae3d68c460" />

Kali Linux Installed!
When I first tried to start the Kali Linux VM, I encountered an error because hardware virtualization was disabled in my computer's BIOS.
<img width="123" height="320" alt="2-ERROR-STARTING-KALI-LINUX" src="https://github.com/user-attachments/assets/7a6f2a59-3ceb-462a-92a0-356c7c2e4ca5" />

I restarted the computer, accessed the BIOS settings, and enabled Intel VT-x.
<img width="369" height="159" alt="image" src="https://github.com/user-attachments/assets/8c4fbc32-0454-4dfd-b29b-891140eba62a" />

After enabling virtualization, the VM started successfully.
<img width="634" height="117" alt="image" src="https://github.com/user-attachments/assets/530df038-e70e-4228-8722-25517f5cbe3f" />

After starting Kali Linux, I encountered an issue with internet connectivity. I followed the troubleshooting steps in the guide and was able to establish a network connection.
<img width="1310" height="650" alt="image" src="https://github.com/user-attachments/assets/f4e510d8-80ef-47d8-a0b4-81bf30a17e9b" />

In Kali Linux 2026.3, the graphical network menu did not provide an option to edit the wired connection. To access the network configuration settings, I opened the terminal and ran: nm-connection-editor. 

This opened the Network Connections editor, allowing me to configure the wired connection and establish internet connectivity.
<img width="892" height="394" alt="4-CONNECTION-STABLISHED" src="https://github.com/user-attachments/assets/d933e72e-c5dd-4fe9-b338-ea6138b9a755" />



