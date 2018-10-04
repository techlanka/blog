---
layout: post
current: post
navigation: True
title: Delegate the domain to Another Name Server
date: 2018-09-06 10:00:40
cover: assets/images/tags.jpg
tags: [Tips & Tricks]
class: post-template
subclass: 'post tag-tips & tricks'
author: mirshad
---


You can delegate your LK domain to any other Name server and take control of your DNS. To do this, you need to go to the domain settings on domains.lk site and 'select the type you need to add' to Name Server.change the DNS server that supports the domain.(Changing this will result in deleting all your existing Resource Records).
---

#### You can choose any of the Name Server Providers, some best known providers are listed below.

Cloudflare
ClouDNS
DNSMadeEasy
Dyn
Route53
UltraDNS
Verisign
Zoho

#### After delegating the domain:

You can manage your domain's DNS records in your NS service providers DNS editor.
Primary DNS server – “dns1.techlanka.lk.” (The dot in the end is NOT a mistake
Secondary DNS server – “dns2.techlanka.lk.” 
Important:
1. There's no compulsory to add more than one DNS server, it depends on your Domain provider.
2. If the delegation settings have a field for entering the IP addresses, leave them empty.
3. Wait for the changes to take effect in the DNS (this may take up to 24 hours)


#### Create a CNAME record with specific content to LK domain

In LK domain control panel the way of adding CNAMEs is quite different,
For example, instead of adding the host @ in the Name field, you need yo add 'techlanka.lk.' 
same applies for when you add www it should be as 'www.techlanka.lk.'
Create a new CNAME record with the following field values (the field names may differ for different control panels):

Name – A sub-domain of your domain with the same name as the string shown on the confirmation page.

For example, the confirmation page shows the string “yamail-123456abcdef”, and you want to confirm the domain “techlanka.lk”. In this case, you should set the CNAME record like this,:
“yamail-123456abcdef.techlanka.lk.” (with a dot at the end).
In some control panels, the dot at the end is added automatically, or you don't need to enter the name of the domain being confirmed. In this case you have adda a dot manually for LK domains.

Value –
“mail.techlanka.lk.” 
The dot at the end of the server name is required for LK Domain.

To check the CNAME record, click the domain again in the list of domains, then click Check. Keep in mind that it may take up to 24 hours for DNS changes to take effect.
