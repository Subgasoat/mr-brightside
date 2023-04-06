Name:
	Max Riverside - Mr. Brightside
Date: 
	2023-03-29
		till
	
Report:
	MrB#1

# 0. $You've-got-mail!  ==Discovery ==
## 0.1 First notice
On the 29<sup>th</sup> of March 2023 a company received a suspicious email. It got brought under my attention and today i will start discovering how much I can identify about the source. I will save all the reports, scans, names, anything I can find. Let's dive into it!

## 0.2 The email
### 0.2.1 Redaction
As you can see in the [[Screenshot_20230406_104508.jpg]] I redacted the company name out of the mail, if I want to mention the company in the future I will call it *"the victim"*. I also added the full (redacted) [source code ](source_redacted.htm.md) of the Outlook export (the first 700ish lines is just style code, nothing special).
For testing purposes, I changed all the links that were revering to ``` @[Redacted]``` to a throw-away mail: ```nova.nexus.llc@proton.me```, a company completely imagined by chatGPT. For shits and giggles I've [[Sus mails, files, everything Sus/MrB1 - Pishing - Office - Mail/header|added]] that conversation in this folder as well. 

### 0.2.2 Victim's findings
When receiving the mail a couple of things were immediatly obviously suspicious for the victim:

1. The victim does not have a Microsoft account. 99% of the time they use Google Docs

But of course, maybe someone else did send something from Microsoft 365? On further investigation, they quickly found out that it was indeed spam:

2. The ```sender-domain``` *(everything between the ```@``` and the ```.``` in an email address)* and ```sender-tld``` *(everything after ```.```)* is the same as the victims

As if they had sent themselves an email. But with a different ```username``` *(everything before ```@```)*, unknown to the victim.
``` html
<span style='color:black'> [Redacted] Office Document
&lt;secured_file87987@[Redacted]&gt;<o:p></o:p></span></p>
```

Lastly:

3. The button in the mail redirects to a strange link: ```https://ty.ck1588.top/awa/#max.riverside.llc@proton.me``` *note: in the real email instead of *
``` html
<p class=MsoNormal style='margin:1.5pt'><span style='mso-fareast-font-family:
                "Times New Roman"'><a
                href="https://ty.ck1588.top/awa/#nova.nexus.llc@proton.me"
                style='float:Center'><span style='font-size:13.0pt;color:#CED4E0;
                background:#0C59F2;text-decoration:none;text-underline:none'><o:p></o:p></span></a></span></p>
                <p class=MsoNormal align=center style='margin:1.5pt;text-align:
                center'><span style='font-size:13.0pt;mso-fareast-font-family:"Times New Roman";
                color:#CED4E0;background:#0C59F2'><a
                href="https://ty.ck1588.top/awa/#nova.nexus.llc@proton.me"><span
                style='color:#CED4E0;text-decoration:none;text-underline:none'>Get
                your file</span></a></span></p> 	
```

The victim did not know this site. Strange I know, like who does not know about this superdupersite?

## 0.3 Summary
URL found:
```https://ty.ck1588.top/awa/#max.riverside.llc@proton.me``` 

----


# 1.  $Let's-start ==Gathering information==
## 1.1  What are you?
### 1.1.1 My hypothesis based on the information I have now
The attacker made sure that on first sight the email looks legit; it has the same colors as Microsoft uses, the same font, the whole lay-out. Especially if someone does not use the Office Suite that often. 
The attackers got around some possible firewall difficulties by spoofing ```@victimsowndoma.in```. In the end this was their downfall as well; the victim didn't recognize the username in front of it since it is a one person company.
This makes me think that this attack wasn't focussed on the victim, but more like throwing spaghetti to a wall and see what sticks. 

### 1.1.2 <header /header>
Enough talk, let's find out how the attacker hid his email and passed the firewall.
I remember from computer science years ago when I was still in high school that you can fake the sender email. It has something to do with the [header](header.md) of the email.

A quick Google search on "email header analyzer" brought me to multiple online analyzers, I tried them and they are all in Japan and Taiwan, which makes it very plausible that they are from Asia. Unfortuanitly this is where it stops for this project. All the IP's are dead, so there is no trail to follow anymore. Next time I'll start faster!
## Summary
Start faster next time ;)
