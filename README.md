# week-2-cybersecurity-and-ethical-hacking-lab-1-foot-printing-and-reconnaissance on networkwalks.com
In the above lab was to attain this information with this commands :
whois; where i was able to get the domain registration details , name of the server ,server point and the abuse contacts.
whatweb; was able to fingerprint the web details such as the exact software and version and the sever ip address.
nslookup; with this command was able to resolve the domain of the website and its ip address.
curl -I https://networkwalks.com; this gave me information about the HTTP headers , web server, caching stack and the hidden end points.
wafw00f;helped me to see if a firewall is watching , the kind of security that is behind networkwalks.com
dnsrecon -d networkwalks.com; this mapped for me the entire DNS-footprint: from mail servers , dns software version , spf policy and the c-panel service records

below is the entire report 

┌──(kali㉿kali)-[~]
└─$ whois networkwalks.com 
   Domain Name: NETWORKWALKS.COM
   Registry Domain ID: 2452319255_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.godaddy.com
   Registrar URL: http://www.godaddy.com
   Updated Date: 2025-11-12T10:08:43Z
   Creation Date: 2019-11-06T22:51:46Z
   Registry Expiry Date: 2027-11-06T22:51:46Z
   Registrar: GoDaddy.com, LLC
   Registrar IANA ID: 146
   Registrar Abuse Contact Email: abuse@godaddy.com
   Registrar Abuse Contact Phone: 480-624-2505
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Name Server: NS6135.HOSTGATOR.COM
   Name Server: NS6136.HOSTGATOR.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-11-10T16:00:15Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

NOTICE: The expiration date displayed in this record is the date the
registrar's sponsorship of the domain name registration in the registry is
currently set to expire. This date does not necessarily reflect the expiration
date of the domain name registrant's agreement with the sponsoring
registrar.  Users may consult the sponsoring registrar's Whois database to
view the registrar's reported date of expiration for this registration.

TERMS OF USE: You are not authorized to access or query our Whois
database through the use of electronic processes that are high-volume and
automated except as reasonably necessary to register domain names or
modify existing registrations; the Data in VeriSign Global Registry
Services' ("VeriSign") Whois database is provided by VeriSign for
information purposes only, and to assist persons in obtaining information
about or related to a domain name registration record. VeriSign does not
guarantee its accuracy. By submitting a Whois query, you agree to abide
by the following terms of use: You agree that you may use this Data only
for lawful purposes and that under no circumstances will you use this Data
to: (1) allow, enable, or otherwise support the transmission of mass
unsolicited, commercial advertising or solicitations via e-mail, telephone,
or facsimile; or (2) enable high volume, automated, electronic processes
that apply to VeriSign (or its computer systems). The compilation,
repackaging, dissemination or other use of this Data is expressly
prohibited without the prior written consent of VeriSign. You agree not to
use electronic processes that are automated and high-volume to access or
query the Whois database except as reasonably necessary to register
domain names or modify existing registrations. VeriSign reserves the right
to restrict your access to the Whois database in its sole discretion to ensure
operational stability.  VeriSign may restrict or terminate your access to the
Whois database for failure to abide by these terms of use. VeriSign
reserves the right to modify these terms at any time.

The Registry database contains ONLY .COM, .NET, .EDU domains and
Registrars.
Domain Name: networkwalks.com
Registry Domain ID: 2452319255_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.godaddy.com
Registrar URL: https://www.godaddy.com
Updated Date: 2025-11-12T05:08:41Z
Creation Date: 2019-11-06T17:51:46Z
Registrar Registration Expiration Date: 2027-11-06T17:51:46Z
Registrar: GoDaddy.com, LLC
Registrar IANA ID: 146
Registrar Abuse Contact Email: abuse@godaddy.com
Registrar Abuse Contact Phone: +1.4806242505
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Registry Registrant ID: Not Available From Registry
Registrant Name: Registration Private
Registrant Organization: Domains By Proxy, LLC
Registrant Street: DomainsByProxy.com
Registrant Street: 100 S. Mill Ave, Suite 1600
Registrant City: Tempe
Registrant State/Province: Arizona
Registrant Postal Code: 85281
Registrant Country: US
Registrant Phone: +1.4806242599
Registrant Phone Ext:
Registrant Fax: 
Registrant Fax Ext:
Registrant Email: https://www.godaddy.com/whois/results.aspx?domain=networkwalks.com&action=contactDomainOwner
Registry Tech ID: Not Available From Registry
Tech Name: Registration Private
Tech Organization: Domains By Proxy, LLC
Tech Street: DomainsByProxy.com
Tech Street: 100 S. Mill Ave, Suite 1600
Tech City: Tempe
Tech State/Province: Arizona
Tech Postal Code: 85281
Tech Country: US
Tech Phone: +1.4806242599
Tech Phone Ext:
Tech Fax: 
Tech Fax Ext:
Tech Email: https://www.godaddy.com/whois/results.aspx?domain=networkwalks.com&action=contactDomainOwner
Name Server: NS6135.HOSTGATOR.COM
Name Server: NS6136.HOSTGATOR.COM
Name Server: NS29.DOMAINCONTROL.COM
Name Server: NS30.DOMAINCONTROL.COM
DNSSEC: unsigned
URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
>>> Last update of WHOIS database: 2026-11-10T16:00:32Z <<<
For more information on Whois status codes, please visit https://icann.org/epp

TERMS OF USE: The data contained in this registrar's Whois database, while believed by the
registrar to be reliable, is provided "as is" with no guarantee or warranties regarding its
accuracy. This information is provided for the sole purpose of assisting you in obtaining
information about domain name registration records. Any use of this data for any other purpose
is expressly forbidden without the prior written permission of this registrar. By submitting
an inquiry, you agree to these terms and limitations of warranty. In particular, you agree not
to use this data to allow, enable, or otherwise support the dissemination or collection of this
data, in part or in its entirety, for any purpose, such as transmission by e-mail, telephone,
postal mail, facsimile or other means of mass unsolicited, commercial advertising or solicitations
of any kind, including spam. You further agree not to use this data to enable high volume, automated
or robotic electronic processes designed to collect or compile this data for any purpose, including
mining this data for your own personal or commercial purposes. Failure to comply with these terms
may result in termination of access to the Whois database. These terms may be subject to modification
at any time without notice.

**NOTICE** This WHOIS server is being retired. Please use our RDAP service instead.


WHATWEB
┌──(kali㉿kali)-[~]
└─$ whatweb networkwalks.com
http://networkwalks.com [301 Moved Permanently] Apache, Cookies[__wpdm_client], Country[UNITED STATES][US], HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], RedirectLocation[https://networkwalks.com/], UncommonHeaders[permissions-policy,x-redirect-by,upgrade,referrer-policy,x-endurance-cache-level,x-nginx-cache]
https://networkwalks.com [200 OK] Apache, Bootstrap[7.1.4], Cookies[__wpdm_client], Country[UNITED STATES][US], Email[info@networkwalks.com], Frame, Google-Tag-Manager, HTML5, HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], JQuery[3.7.1], MetaGenerator[WordPress 7.1.4,WordPress Download Manager 3.3.76], Open-Graph-Protocol[website], Script[4684NR-IPIB&amp;pidnVar2=50511&amp;prtVar2=7&amp;scvVar2=12,application/json,application/ld+json,module,speculationrules,text/javascript], Title[Networkwalks Academy], UncommonHeaders[permissions-policy,link,upgrade,referrer-policy,x-endurance-cache-level,x-nginx-cache], WordPress[7.1.4]
https://networkwalks.com/ [200 OK] Apache, Bootstrap[7.1.4], Country[UNITED STATES][US], Email[info@networkwalks.com], Frame, Google-Tag-Manager, HTML5, HTTPServer[Apache], IP[192.232.216.135], JQuery[3.7.1], MetaGenerator[WordPress 7.1.4,WordPress Download Manager 3.3.76], Open-Graph-Protocol[website], Script[4684NR-IPIB&amp;pidnVar2=50511&amp;prtVar2=7&amp;scvVar2=12,application/json,application/ld+json,module,speculationrules,text/javascript], Title[Networkwalks Academy], UncommonHeaders[permissions-policy,link,upgrade,referrer-policy,x-endurance-cache-level,x-nginx-cache], WordPress[7.1.4]
                                                                             
┌──(kali㉿kali)-[~]
└─$   

NSLOOKUP
┌──(kali㉿kali)-[~]
└─$ nslookup networkwalks.com
Server:         10.163.252.172
Address:        10.163.252.172#53

Non-authoritative answer:
Name:   networkwalks.com
Address: 192.232.216.135

                                                                                                                  
┌──(kali㉿kali)-[~]
└─$


CURL -I  http://networkwalks.com
┌──(kali㉿kali)-[~]
└─$ curl -I https://networkwalks.com
HTTP/2 200 
permissions-policy: private-state-token-redemption=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com"), private-state-token-issuance=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com")
link: <https://networkwalks.com/wp-json/>; rel="https://api.w.org/", <https://networkwalks.com/wp-json/wp/v2/pages/53>; rel="alternate"; title="JSON"; type="application/json", <https://networkwalks.com/>; rel=shortlink
set-cookie: __wpdm_client=3d9039cb7a38688c6b375b0d63b5f859; path=/; domain=networkwalks.com; secure; HttpOnly
referrer-policy: no-referrer-when-downgrade
x-endurance-cache-level: 0
x-nginx-cache: WordPress
content-type: text/html; charset=UTF-8
date: Tue, 10 Nov 2026 16:13:58 GMT
server: Apache

                                                                                                                  
┌──(kali㉿kali)-[~]
└─$
 

WAFW00F HTTPS://NETWORKWALKS.COM
                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ wafw00f networkwalks.com

                ______
               /      \
              (  W00f! )
               \  ____/
               ,,    __            404 Hack Not Found
           |`-.__   / /                      __     __
           /"  _/  /_/                       \ \   / /
          *===*    /                          \ \_/ /  405 Not Allowed
         /     )__//                           \   /
    /|  /     /---`                        403 Forbidden
    \\/`   \ |                                 / _ \
    `\    /_\\_              502 Bad Gateway  / / \ \  500 Internal Error
      `_____``-`                             /_/   \_\\

                        ~ WAFW00F : v2.4.2 ~
        The Web Application Firewall Fingerprinting Toolkit
    
[*] Checking https://networkwalks.com
[+] The site https://networkwalks.com is behind ModSecurity (SpiderLabs) WAF.
[~] Number of requests: 2

DNSRECON -D NETWORKWALKS.COM
                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ dnsrecon -d networkwalks.com
2026-11-10T11:43:32.738411-0500 INFO Starting enumeration for domain: networkwalks.com
2026-11-10T11:43:32.739140-0500 INFO std: Performing General Enumeration against: networkwalks.com...
2026-11-10T11:43:33.908811-0500 ERROR No answer for DNSSEC query for networkwalks.com
2026-11-10T11:43:34.706574-0500 INFO     SOA ns6135.hostgator.com 50.87.144.87
2026-11-10T11:43:35.159911-0500 INFO     NS ns6135.hostgator.com 50.87.144.87
2026-11-10T11:43:35.989768-0500 INFO     Bind Version for 50.87.144.87 "9.16.23-RH"
2026-11-10T11:43:35.990629-0500 INFO     NS ns6136.hostgator.com 192.232.216.131
2026-11-10T11:43:36.659632-0500 INFO     Bind Version for 192.232.216.131 "9.16.23-RH"
2026-11-10T11:43:37.699052-0500 INFO     MX mail.networkwalks.com 192.232.216.135
2026-11-10T11:43:37.724200-0500 INFO     A networkwalks.com 192.232.216.135
2026-11-10T11:43:38.673266-0500 INFO     TXT networkwalks.com v=spf1 +a +mx +ip4:50.87.144.87 +include:websitewelcome.com ~all
2026-11-10T11:43:38.673639-0500 INFO     TXT networkwalks.com google-site-verification=rr04eRmqHoWY3XemnizDNVK4q75X-Ij-mjgEeg-UsYI
2026-11-10T11:43:39.845878-0500 INFO Enumerating SRV Records
2026-11-10T11:43:46.496691-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.15 443
2026-11-10T11:43:46.496964-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.14 443
2026-11-10T11:43:46.497062-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.9 443
2026-11-10T11:43:46.497140-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.11 443
2026-11-10T11:43:46.497268-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.15 443
2026-11-10T11:43:46.497342-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.14 443
2026-11-10T11:43:46.497659-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.9 443
2026-11-10T11:43:46.498179-0500 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.11 443
2026-11-10T11:43:46.498901-0500 INFO 8 Records Found
2026-11-10T11:43:46.499212-0500 INFO Completed enumeration for domain: networkwalks.com

                                                                                                                  
┌──(kali㉿kali)-[~]
└─$




4. Activities Performed 
4.1 Footprinting  & Reconnaissance 
I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon. Each tool was used to collect a different type of information about the target.
First, I used WHOIS to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
I then used WhatWeb to identify technologies used by the website. The results identified WordPress 7.0.4 and WP Download Manager 3.3.58, along with other information exposed by the website.
Using Nslookup, I resolved the domain name to its IP address. The provided result identified 192.232.216.135.
I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/.
Next, I used Wafw00f to determine whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs).
Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records and DNS software information.

4.2 Footprinting using the MALTEGO TOOLS 
For the second activity I used matlego tools to on the domain of networkwalks.com and was able to filter the email information from Networkwalks.com. 
4.3 Network Scanning with Zenmap 
For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.
I first used the Windows ipconfig command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.
The example results provided in the practical identified four live hosts:
•	172.20.10.4
The example results also included four MAC addresses.
After completing the scan, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.
Note: The actual subnet, number of hosts and addresses should be replaced with the results from my own network when submitting the report 
5.Risk Analysis  / Impact 
No.	Risk/ finding	Evidence /Observation	Potential impact 	Risk level 
1	Web technology information exposed 	Whatweb identified wordpress and WP download manager 	Attackers may use exposed technologies / version information  to identify software requiring further security review   	Medium 
2	Server IP address identified 	Nslookup resolved the domain to 192.232.216.135	Provides information about the network location of the web  service 	Low
3	HTTP technical information exposed  	Curl returned HTTP response headers  and exposed “wp-json”	May  assist technology fingerprinting  and further  enumeration 	Low
4	WAF technology identifiable 	Wafw00f  identified  Modsecurity “SpiderLabs “	Reveals information about the web application`s security  architecture 	Low 
5	DNS infrastructure information exposed 	DNSRECON identified DNS , mail and service-related records 	DNS information can help build a broader infrastructure profile 	Medium 
6	No multiple live visible on the local network  	Zenmap identified  1 live host in the example network 	Unknown or unauthorized  devices  may potentially be present on a network 	Medium 

Risk level keys 
•	Low 
•	Medium 
•	Critical
 
The risks above are observations from the footprinting and scanning exercises, not confirmed vulnerabilities.
The practical exercises primarily involved information gathering and host discovery. No exploitation or vulnerability validation was performed as part of these two modules.
Therefore, the presence of information such as a software version, IP address or DNS record does not by itself mean that the system is vulnerable. Further authorized security testing would be required to confirm any actual vulnerability.

6. Recommendations 
Based on the observations from these activities, I recommend the following security improvements:
1.	Review publicly exposed technology information
Organizations should regularly review what information about their web technologies, CMS and plugins is publicly visible.
2.	Keep software updated
CMS platforms, plugins and other web technologies should be regularly updated and reviewed against current security advisories.
3.	Review HTTP headers
HTTP response headers should be reviewed to determine whether unnecessary technical information is being exposed.
4.	Review DNS records regularly
DNS records should be checked periodically to ensure that only required information and services are publicly exposed.
5.	Properly configure and monitor the WAF
Keep the WAF (ModSecurity) enabled and tuned, since it already blocks naive attacks.
6.	Perform regular internal network discovery
Organizations should periodically scan their own networks to identify active devices.
7.	Investigate unknown devices
Any unexpected device discovered during network scanning should be investigated and verified.
8.	Maintain network documentation
Network topology and device information should be documented and updated regularly.
9.	Perform security testing with authorization
Reconnaissance and scanning should only be performed against systems and networks where appropriate authorization has been provided.

7.Conclusion 
During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering footprinting, reconnaissance and network scanning.
In the footprinting activity, I used six Kali Linux and theHarvester tools to collect information about the target domain. I learned how WHOIS can provide domain information, WhatWeb can identify web technologies, Nslookup can resolve domain names, Curl can inspect HTTP headers, Wafw00f can identify a WAF, and DNSRecon can provide additional DNS information.
In the network scanning activity, I used Zenmap to identify my local network configuration and discover active hosts. I also collected IP and MAC address information and created a network topology.
The exercises showed me that information gathering is an important part of cybersecurity. Even before attempting to exploit a system, a security professional can learn a significant amount about an environment by carefully analyzing publicly available information and network responses.
I also learned that technical findings should be documented clearly. A good cybersecurity report should explain what was performed, what was discovered, what the observation means, what risk it may create, and what can be done to reduce that risk.
Finally, I learned that reconnaissance and scanning must always be performed within an authorized scope. These activities were completed as part of the assigned educational cybersecurity lab.
8.Evidence collect 
"check the attached screenshots 
Author
Ndowole Rodrick Bonganwa 
Cybersecurity professional B084E
LinkedIn : https://www.linkedin.com/in/ndowole-rodrick-3696b0351/ 

