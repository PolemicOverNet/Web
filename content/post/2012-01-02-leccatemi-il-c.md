---
title: Leccatemi il C….
author: El -Glabro
type: post
date: 2012-01-02T16:50:22+00:00
url: /leccatemi-il-c/
categories:
  - Lavorare da casa ma da casa a Londra
  - Sistemiere
  - Work
tags:
  - buon 2012
  - caparezza
  - debian + xen + drbd
  - leccatemi il c

---
Tanto per essere chiari si parla di Cloud, sempre maliziosi voi&#8230;.  
Ebbene si, i pezzi di computer acquistati ed arrivati dalla Rep. Slovacca funzionano, e dopo una settimana di lavoro 24/7 (installa, configura, testa, bestemmia re-installa, configura, testa, bestemmia e via via fino a che ne restava la forza.) son riuscito a cavarci fuori una piattaforma (dei poveri) che assomiglia all&#8217;idea generale che le persone si fanno quando sentono la $BuzzWord.

&#8212;&#8212;&#8212;&#8212;Inizio parte pseudo-tecnica e noiosa&#8212;&#8212;&#8212;&#8212;&#8211;  
Niente di Sci-Fi ovviamente, costi bassi e prestazioni occasionali al limite dei componenti (lanciati da Miwa), si tratta di una coppia di computer gemelli montati su scheda madre ASrock con le seguenti caratteristiche:  
1 CPU amd Phenom II x6 (6 core e 2800 Mhz a Core)  
16 Gb di RAM  
2 dischi da 1Tb SATA II 7200 rpm  
Dissipatore stile Riccardino Fuffolo (piccolo) con ventola 12&#215;12 e staffa da avvitare sul retro della Mo.Bo. perché pesa giusto 700 grammi  
Alimentatore 600 Watt  
Scheda video ed audio rigorosamente incorporate

Solo Pinguini sono stati adoprati per mettere su tutto questo e posso riassumerlo con quanto segue:

&#8211; Debian 6 64bit (tutte le volte che ne installi una nasce un Piccolo Sandro Polemico)  
&#8211; dmraid=true da passare in fase di boot a grub per gestire il controller RAID della scheda madre configurato a 1 e per installare grub al riavvio successivo  
&#8211; Dischi partizionati con 100 Gb per la / e 900 di LVM per i volumi dei server virtuali  
&#8211; Xen 4 (attivate opzioni xen server, vlc e balooning)  
&#8211; DRBD in configurazione Master/Master per i singoli volumi e non per tutti i 900 GB

Con tutto questo si ottiene:  
&#8211; Una piattaforma che mi esula dal dover installare fisicamente tutte le macchine di test su cui più o meno costantemente razzolo  
&#8211; Uno storage costantemente replicato ed in grado di recuperare velocemente in caso di drammi (grazie a DRBD); va comunque detto che DRBD non lo si può utilizzare come una lavatrice, e se ti vanno idischi fuori sincrono bisogna che fai un attimo mente locale prima di copiare ed incollare i primi comandi che ti passano per le mani  
&#8211; Migrazione LIVE delle macchine virtuali da un host all&#8217;altro

Ora comincerà la fase di trasbordoi servizi che probabilmente andrà per il verso sbagliato, ma anche se fosse le maniche ce le ho già rimboccate, sarà il male di sporcarsi un po&#8217; di più.

Magari fra un po&#8217;scrivo tutti i passaggi in un post, almeno li ripasso  
&#8212;&#8212;&#8212;&#8212;Fine parte noiosa&#8212;&#8212;&#8212;&#8211;

Capodanno tutto bene!  
Sono stato con gli amici in Piazza Stazione S.M.N. a vedere Caparezza, ganzo, concerto bello, passeggiata sui cocci di bottiglia e poi tutti a nanna verso le 4 del mattino unica pecca: davvero troppa gente, colpa del tempo clemente o della tanto nominata crisi?

E per finire&#8230;.  
&#8230;ho cambiato lavoro, di nuovo, nulla di male nel buon vecchio deploy delle applicazioni in Java, solo che alla lunga annoia, ed allora ho deciso di passare su un&#8217;altra sponda, quella del Customer Care a Rackspace, dove la paga é ottima, i bonus pure, e resta solo da trovare l&#8217;appartamento non a 2 ore dall&#8217;ufficio (solo&#8230;).

Comunicazione di servizio:  
Io torno a Londra il 7, se non ci si rivede abbracciatevi da parte mia :)