I have installed VirtualBox and set up 10.0.0.0/24 as NAT network
<img width="753" height="190" alt="1-NAT Network" src="https://github.com/user-attachments/assets/8bbe2a6f-8439-4ea5-8a68-f6ae3d68c460" />

Kali Linux Installed.
When starting the kali Linux Virtual Machine I got an error:
<img width="123" height="320" alt="2-ERROR-STARTING-KALI-LINUX" src="https://github.com/user-attachments/assets/7a6f2a59-3ceb-462a-92a0-356c7c2e4ca5" />

The virtualization in my computer was disabled. So I restart the computer to access the BIOS and enabled the Virtualization (VTx)
<img width="369" height="159" alt="image" src="https://github.com/user-attachments/assets/8c4fbc32-0454-4dfd-b29b-891140eba62a" />

Now the VM is RUNNING
<img width="634" height="117" alt="image" src="https://github.com/user-attachments/assets/530df038-e70e-4228-8722-25517f5cbe3f" />

Since the Kali Linux version I am using is 2026.3 it was expected to have connectivity issues, so I executed the commands given in the guide and I was able to active the connection
<img width="1310" height="650" alt="image" src="https://github.com/user-attachments/assets/f4e510d8-80ef-47d8-a0b4-81bf30a17e9b" />

Kali Linux 2026.3 GUI doesn't have the option to "Edit" the Wired Connection so I used the command nm-connection-editor on the terminal
<img width="892" height="394" alt="4-CONNECTION-STABLISHED" src="https://github.com/user-attachments/assets/d933e72e-c5dd-4fe9-b338-ea6138b9a755" />



