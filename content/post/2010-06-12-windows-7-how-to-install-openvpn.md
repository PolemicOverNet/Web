---
title: Windows7 and the UAC V.S. OpenVPN
author: El -Glabro
type: post
date: 2010-06-12T16:22:24+00:00
url: /windows-7-how-to-install-openvpn/
aktt_notify_twitter:
  - yes
  - yes
aktt_tweeted:
  - 1
  - 1
categories:
  - How To
  - Sistemiere
tags:
  - client
  - How To
  - OpenVPN
  - windows 7
  - windows vista

---
How to install correctly the OpenVPN client on Windows 7

1) If you have already tried to install OpenVPN kill all the processes from openvpn and openvpn-gui and uninstall all the software ( save your config files before !!! )  
2) Disable the User Access Control (UAC) and reboot  
3) Right-Click on the OpenVPN installer an then select  
Properties > Compatibility  
a) Enable the flag for &#8220;Run this program in compatibility mode for:&#8221;  
b) Select &#8220;Windows Vista&#8221; in the window below  
c) On the same tab and enable the flag for &#8220;Run this program as administrator&#8221;  
4) Click Apply and Ok  
6) Run the installer  
7) Create a link for OpenVPN-GUI on your desktop  
8) Start the OpenVPN-GUI with a right-click > &#8220;exec as administrator&#8221;  
9) Start your connection from the OpenVPN-GUI icon on your System-Tray

Come installare correttamente OpenVPN su Windows 7:

1) Prima di tutto se avete già provato ad installare OpenVPN killate da task manager tutti i processi openvpn ed openvpn-gui, quindi disinstallate il software ( salvate prima i file di configurazione !!! )  
2) Disabilitate l&#8217; User Access Control (UAC) e reboottate il pc  
3) Cliccate con il tasto destro sull&#8217;installer di OpenVPN e selezionate  
Proprietà > Compatibilità  
a) Mettete la spunta su &#8220;Run this program in compatibility mode for:&#8221;  
b) Selezionate &#8220;Windows Vista&#8221; nella casella sottostante  
c) Nella solita tab mettete la spunta su &#8220;esegui come amministratore&#8221;  
4) Cliccate su Applica e quindi OK  
6) Fate partire l&#8217;installazione di OpenVPN  
7) Create un link di OpenVPN-GUI sul vostro desktop  
8) Fate partire OpenVPN-GUI con il tasto destro > &#8220;esegui come amministratore&#8221;  
9) Dall&#8217;icona nella System-Tray lanciate la vostra connessione