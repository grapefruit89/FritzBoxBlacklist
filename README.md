:do_not_litter: (Fritz!Box)  Blocklist für die Internetkiste oder wie ich einfach Werbung loswerde
===================================
Readme inspired by [🚯 Fritz!Box Blacklist](https://github.com/fboes/fritzbox-blacklist) by [fboes](https://github.com/fboes)

Mein versuch die Welt mit möglichst einfachen Technischen Mitteln ein bisschen besser zu machen...
Da die unmodifizierte Fritzbox leider nur mit 500 Einträgen zurechtkommt, versuche ich hier eine möglichst kurze aber dennoch effektive Liste mit den Alltime TOP 500 geblockten webseiten zu erstellen.  
Mir ist bewusst das das WWW veränderlich ist und die ein oder andere Seite eines Tages nichtmehr aktuell ist aber einem großteil des InterCraps kann man somit vielleicht schon umgehen, auch ohne π **🕳**

Filter in der Fritzbox einsetzen
------------

1. [FritzBox-Kindersicherung - so funktioniert die Einrichtung](https://www.heise.de/tipps-tricks/FritzBox-Kindersicherung-so-funktioniert-die-Einrichtung-4048867.html)  
2. Inhalt der [Blacklist](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Fritz%20500.txt) in die  [Fritzbox](http://www.fritz.box/)kopieren  

läuft auch ohne ein Informatikstudium  
[Fritz!Box als AdBlocker fboës - Der Blog](http://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_internet_filter_blacklist). In der einfachheit der Liste liegt die Anwenderfreundlichkeit.  


[hier den Adblocker Testen](https://ads-blocker.com/testing/)


Neuen DNS Server (in der Fritzbox einsetzen)
-----------
Meiner Mutter würde ich die Funktion eines DNS Servers mit der Analogie eines Telefonbuch´s erklären.
In der Telefonzelle der Deutschen Post liegt auch ein Telefonbuch der Deutschen Post, wenn dem Telefonbuchhersteller ein Eintrag missfällt, so taucht er in diesem Telefonbuch nicht auf.  
Bei den DNS Servern gibt es dann noch die möglichkeit, dass sich jemand das Telefonbuch vorher anschaut und alles was mit Werbung oder Betrug zu tun hat mit einem Dicken Textmarker ausschwärzt, somit kann ich den Bösen weniger auf den Leim gehen.  
Dazu müssen wir uns erstmal für einen Vertrauenswürdigen DNS Server entscheiden  

[Privacy Handbuch](https://www.privacy-handbuch.de/handbuch_93d.htm)  
[Kuketz Empfehlungsecke](https://www.kuketz-blog.de/empfehlungsecke/#dns)  
Mir hat der Der 2te Dismail DNS Server zugesagt IPv4: **159.69.114.157** für´s Handy unter Private DNS **fdns2.dismail.de**  
ansonsten gibt es noch DNS Server mit Integriertem Werbeblocker (Pihole)  
~~[PUBLIC-PIHOLE POWERED BY FREEK.WS](https://public-pihole.com/)~~   --> [AdHole](https://adhole.org/)  
[pi-dns.com](https://pi-dns.com/)  
[Media Techport by Patrick Asmus](https://www.media-techport.de/free-dns-server/)  

um zu testen ob alles geklappt hat
[Adblock Testseite](https://blockads.fivefilters.org/?pihole)  
[DNS Leak Test](https://www.dnsleaktest.com/)  
[Wer selbst für sich nach dem schnellsten DNS Server suchen möchte](https://www.grc.com/dns/dns.htm)  
Hierzu einfach die Standart Liste gegen [Beispiel DNS Server](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Beispiel%20DNS%20Server.ini) austauschen  
  ![sieht das ganze dann so aus](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/DNS%20Benchmark.png)

Weiterführende Links (alles Nützliche zum erstellen einer eigenen Liste)
------------
[xobit.de/fritzbox-blacklist](https://www.xobit.de/fritzbox-blacklist)  
[Frank Boës](https://github.com/fboes/fritzbox-blacklist)  
[Shizoworld](https://shizoworld.de/2019/12/blockliste-der-fritzbox-nutzen/)  
[Kowabit](https://kowabit.de/fritzbox-blacklist-17-01-2020/)·····[Kowabit erklärt](https://kowabit.de/den-einsatz-der-blockliste-erklaert/)·····[Kowabit Bl*cklist](https://kowabit.de/blcklst/)  
[Kuketzblog weiterführende diskussion](https://forum.kuketz-blog.de/viewtopic.php?t=5147)  
[Textfixer Doppelte Zeilen entfernen](https://www.textfixer.de/tools/doppelte-zeilen-entfernen.php)  
Legal stuff
-----------
Original: [Frank Boës](http://3960.org) and others
