---
title: IO PGSQL, La CentOS e Ubuntu (merda)
author: El -Glabro
type: post
date: 2011-03-01T07:04:14+00:00
url: /io-pgsql-la-centos-e-ubuntu-merda/
aktt_notify_twitter:
  - yes
  - yes
wordbooker_options:
  - 'a:11:{s:18:"wordbook_noncename";s:10:"7abbcbea80";s:18:"wordbook_page_post";s:4:"-100";s:18:"wordbook_orandpage";s:1:"2";s:23:"wordbook_default_author";s:1:"1";s:23:"wordbook_extract_length";s:3:"300";s:19:"wordbook_actionlink";s:3:"300";s:26:"wordbooker_publish_default";s:2:"on";s:27:"wordbooker_publish_override";s:2:"on";s:18:"wordbook_attribute";s:17:"News@T-hoster.com";s:29:"wordbooker_status_update_text";s:35:": New blog post :  %title% - %link%";s:20:"wordbook_comment_get";s:2:"on";}'
  - 'a:11:{s:18:"wordbook_noncename";s:10:"7abbcbea80";s:18:"wordbook_page_post";s:4:"-100";s:18:"wordbook_orandpage";s:1:"2";s:23:"wordbook_default_author";s:1:"1";s:23:"wordbook_extract_length";s:3:"300";s:19:"wordbook_actionlink";s:3:"300";s:26:"wordbooker_publish_default";s:2:"on";s:27:"wordbooker_publish_override";s:2:"on";s:18:"wordbook_attribute";s:17:"News@T-hoster.com";s:29:"wordbooker_status_update_text";s:35:": New blog post :  %title% - %link%";s:20:"wordbook_comment_get";s:2:"on";}'
wordbooker_thumb:
  - 
  - 
wordbooker_extract:
  - |
    I database non mi piacciono, e probabilmente io piaccio poco a loro.
    Con MySQL ogni tanto ci parliamo e riusciamo a risolvere diverbi o problemi, ma PostgreSQL non mi può proprio vedere.
    Ora stiamo imparando a conoscerci un po' meglio e da bravi colleghi stiamo cercando di collaborare, ma ques ...
  - |
    I database non mi piacciono, e probabilmente io piaccio poco a loro.
    Con MySQL ogni tanto ci parliamo e riusciamo a risolvere diverbi o problemi, ma PostgreSQL non mi può proprio vedere.
    Ora stiamo imparando a conoscerci un po' meglio e da bravi colleghi stiamo cercando di collaborare, ma ques ...
aktt_tweeted:
  - 1
  - 1
categories:
  - General
  - Sistemiere
  - Work
tags:
  - Ubuntu merda by M3

---
I database non mi piacciono, e probabilmente io piaccio poco a loro.  
Con MySQL ogni tanto ci parliamo e riusciamo a risolvere diverbi o problemi, ma PostgreSQL non mi può proprio vedere.  
Ora stiamo imparando a conoscerci un po&#8217; meglio e da bravi colleghi stiamo cercando di collaborare, ma questa cosa che io gli chiedo di fare la replicazione e lui si mette a fare il muso con quell&#8217;aria di superiorità proprio non la capisco.

Ah, mi dimeticavo di aggiungere che CentOS fa cacare, ovviamente è una disto a pacchetti e sempre ovviamente non sopporta che tu gli installi 2 versioni differenti del solito software, adducendo come scusa che postgresql8.4 va in conflitto con postgresql9.0 (un insalatina di cazzi tua no?).  
Ovviamente perchè dipendono da librerie di versioni completamente differenti fra di loro ed ognuno dei due pacchetti PRETENDE di installarle nel solito posto di quell&#8217;altre, con lo stesso nome.  
&#8220;E te ricompilalo&#8221; potrebbe dire qualcuno..  
Si bravo, c&#8217;ho una disrtibuzione a pacchetti e mi metto a ricompilare tutte le librerie da zero, tanto centOS è snella vero? Una scheggia&#8230;  
Sui server c&#8217;ho trovato installato anche:  
&#8211; il modulo del kernel per far girare il Joypad dell&#8217;XBOX  
&#8211; tutto il pacchetto Openoffice  
&#8211; XEN (XEN????)  
&#8211; il demone per le unità removibili (sai mai che ti dovesse capitare di mettere su un chiavetta USB in US)  
&#8211; tutto X e forse se ci guardo bene c&#8217;è anche l&#8217;installazione del Compiz-fusion.  
Se mi metto a ricompilare 2 librerie non si sa mica che succede al prossimo riavvio&#8230;

Ah, anche Ubuntu fa Cacare (il Tosi aggiungerebbe &#8220;meglio tardi che mai&#8221;), tempo di fare il backup e sul portatile ci installo Slackware9, mio unico, primo e vero amore, e poi giù a scaricare i sorgenti un /usr/local/src e poi via di ./configure &#8211;prefix=/usr/local/