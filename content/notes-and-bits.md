---
title: Notes and bits
author: El -Glabro
type: page
date: 2019-04-29T15:38:27+00:00

---
This is a bunch of **PERSONAL** notes and are published here just for my self and my laziness so we do have a place to go and look and I do take no responsibility in case you decide to use them for yourself or on your systems

**_ I hope the message is clear: NO GUARANTEE AND NO REFUND! _**

**&#8211; tr &#8216;[:upper:]&#8217; &#8216;[:lower:]&#8217;**

**&#8211; S3 tries to look for default pages inside paths**

**&#8211; CloudFront does not looks for the index file inside a path; each address needs to be explicit**

**&#8211; echo abc | sed s/&#8217;\(abc\)&#8217;/&#8217;\1\1&#8217;/g -> abcabc**

**&#8211; If Amavis does not mark the email as SPAM rewriting the subject, 9 times out of 10 is because the @local\_domains\_maps value is not correct, try with @local\_domains\_maps = ( [&#8220;.&#8221;] ); in one of the first conf.d files in amavis and restart the service in debug mode**

**&#8211; To install Samsung M2070W on ubuntu and Debian**

Look at this website first https://www.bchemnet.com/suldr/index.html

Add the Repo as first:  
<span style="color: #3366ff;"># bash -c &#8216;echo &#8220;deb https://www.bchemnet.com/suldr/ debian extra&#8221; >> /etc/apt/sources.list&#8217;</span>

Download signatures from here:  
<span style="color: #3366ff;"># wget &#8216;http://www.bchemnet.com/suldr/pool/debian/extra/su/suldr-keyring_2_all.deb&#8217;</span>

Install the signature package with:  
<span style="color: #3366ff;"># dpkg -i suldr-keyring_2_all.deb</span>

Install teh drivers for your network printer and scanner with:  
<span style="color: #3366ff;"># apt-get install suld-driver2-1.00.39</span>

Test it from the terminal with:  
<span style="color: #3366ff;"># scanimage -L</span>

<pre class="wp-block-preformatted"><strong>- To install Realtek 8821ce on ubuntu and Debian</strong>
sudo apt-get install --reinstall git dkms build-essential linux-headers-$(uname -r)
git clone https://github.com/tomaspinho/rtl8821ce
cd rtl8821ce
chmod +x dkms-install.sh
chmod +x dkms-remove.sh
sudo ./dkms-install.sh</pre>