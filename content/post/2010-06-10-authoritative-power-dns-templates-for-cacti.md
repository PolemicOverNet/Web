---
title: Authoritative Power-dns templates for Cacti
author: El -Glabro
type: post
date: 2010-06-10T20:52:41+00:00
url: /authoritative-power-dns-templates-for-cacti/
aktt_notify_twitter:
  - yes
  - yes
aktt_tweeted:
  - 1
  - 1
categories:
  - How To
  - Linkedin
  - Sistemiere
tags:
  - cacti
  - How To
  - Linkedin
  - PowerDNS
  - templates

---
Hi all, I have recently written a couple of Cacti templates for the authoritative Power DNS server.  
Both templates are based on a script executed from the SNMPD server

Template and script were written and tested on Debian 5 and Cacti version 0.8.7b

Do these operations on the server which is running Power DNS

  1. Create an sh script:  
    > \# vi /bin/pdns.sh
    
    Copy and paste the following lines inside the /bin/pdns.sh file:
    
    > #!/bin/bash  
    > #  
    > /etc/init.d/pdns dump |awk &#8216;{gsub(/,/, &#8220;\n&#8221;);print}&#8217; | cut -d &#8220;=&#8221; -f 2 > /var/tmp/pdnsstat
    
    Obviously the directory /var/tmp/ must exist and must be writeable from the SNMPD user</li> 
    
      * Let the /bin/pdns.sh script executable  
        > chmod +x   /bin/pdns.sh
    
      * Now edit your snmpd.conf  (usually is located in /etc/snmp/snmpd.conf ) end add the following line:  
        > exec     pdns     /bin/cat /var/tmp/pdnsstat
    
      * Restart your snmpd service  
        > \# /etc/init.d/snmpd restart
    
      * Now edit the root crontab and add:  
        > \*/5 \* \* \* * sleep 120 && /bin/pdns.sh
    
      * Execute the script /bin/pdns.sh for the first time with the debug option:  
        > \# sh -x /bin/pdns.sh
    
      * Verify the creation and the content of the /var/tmp/pdnsstat file
      * Now try to ask one of the numbers to the snmpd server using the snmpwalk command:  
        > \# snmpwalk -Os -c community -v1 127.0.0.1 .1.3.6.1.4.1.8072.1.3.2.4.1.2.4.112.100.110.115.20
        
        If the response is something like &#8220;nsExtendOutLine.&#8221;pdns&#8221;.20 = STRING: 6392&#8243;, the snmp server is configured properly.</li> 
        
          * Download and import the templates for Cacti</ol> 
        
        <p style="text-align: center;">
          <a title="cacti_graph_template_powerdns_autoritative_dns_-_stats.xml" href="http://www.t-hoster.com/downloads/cacti_graph_template_powerdns_autoritative_dns_-_stats.xml.tar.gz" target="_blank">cacti_graph_template_powerdns_autoritative_dns_-_stats.xml.tar.gz</a>
        </p>
        
        <p style="text-align: center;">
          <a title="cacti_graph_template_powerdns_autoritative_dns_-_stats.xml" href="http://www.t-hoster.com/downloads/cacti_graph_template_powerdns_autoritative_dns_-_stats.xml.tar.gz" target="_blank"></a><a title="cacti_graph_template_powerdns_autoritative_dns_-_cache_stats.xml" href="http://www.t-hoster.com/downloads/cacti_graph_template_powerdns_autoritative_dns_-_cache_stats.xml.tar.gz" target="_blank">cacti_graph_template_powerdns_autoritative_dns_-_cache_stats.xml.tar.gz</a><a title="cacti_graph_template_powerdns_autoritative_dns_-_stats.xml" href="http://www.t-hoster.com/downloads/cacti_graph_template_powerdns_autoritative_dns_-_stats.xml.tar.gz" target="_blank"><br /> </a>
        </p>
        
        <p style="text-align: center;">
          <p style="text-align: center;">
            A screenshot from each graphics:
          </p>
          
          <p style="text-align: center;">
            <img decoding="async" src="http://farm5.static.flickr.com/4032/4689141624_fc2c63b6f7.jpg" alt="cacti_graph_template_powerdns_autoritative_dns_-_stats" /><img decoding="async" src="http://farm5.static.flickr.com/4042/4688504563_573f73f6ba.jpg" alt="cacti_graph_template_powerdns_autoritative_dns_-_cache_stats" />
          </p>
          
          <p style="text-align: center;">
            <p style="text-align: center;">