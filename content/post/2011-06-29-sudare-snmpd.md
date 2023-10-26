---
title: Sudare SNMPD
author: El -Glabro
type: post
date: 2011-06-29T11:59:03+00:00
url: /sudare-snmpd/
categories:
  - Linkedin
  - Work
tags:
  - come ricompilare
  - debian
  - snmpd

---
Il pacchetto SNMPD di debian ha un porblema secondo me, è compilato di default per un massimo di 50 slot in cui inserire le proprie personalizzazioni  
Mi riferisco alla versione snmpd_5.4.1~dfsg-12  
Io di slot ne abbisognavo circa 110  
Ecco come ho sudato e come ho risolto (e poi segnalato ai manutentori come Sandrino dice):

1) apt-get install build-essential subversion git-buildpackage #Utils per la compilazione  
2) apt-get source net-snmp #Scaricare il sorgente di net-snmp  
3) apt-get build-dep net-snmp #Installa eventuali dipendenze di cui potresti aver bisogno per la compilazione  
4) cd net-snmp-5.4.1~dfsg #Buttati nella cartella che apt-get source net-snmp ti ha regalato  
5) vi agent/mibgroup/agent/extend.c #Modifica il sorgente  
6) Modifica della linea  
-> int max\_compatability\_entries = 50;  
in  
->int max\_compatability\_entries = 200;  
7) dch -l &#8216;versione el-glabro&#8217; #Personalizza il nome della tua versione  
8) debuild -us -uc #Build del/dei pacchetti  
9) dpkg -i ../snmpd\_5.4.1\*.deb ../snmp\_5.4.1\*.deb #Installo solo quelli di cui ho bisogno  
10) /etc/init.d/snmpd restart #Riavvione di snmpd