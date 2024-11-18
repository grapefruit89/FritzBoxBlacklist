:do_not_litter: (Fritz!Box)  Blocklist für die Internetkiste oder wie ich einfach Werbung loswerde
===================================
Readme inspired by [🚯 Fritz!Box Blacklist](https://github.com/fboes/fritzbox-blacklist) by [fboes](https://github.com/fboes)

Mein versuch die Welt mit möglichst einfachen Technischen Mitteln ein bisschen besser zu machen...
Da die unmodifizierte Fritzbox leider nur mit 500 Einträgen zurechtkommt, versuche ich hier eine möglichst kurze aber dennoch effektive Liste mit den Alltime TOP 500 geblockten webseiten zu erstellen.  
Mir ist bewusst das das WWW veränderlich ist und die ein oder andere Seite eines Tages nichtmehr aktuell ist aber einem großteil des InterCraps kann man somit vielleicht schon umgehen, auch ohne π **🕳**

Filter in der Fritzbox einsetzen
------------

1. [FritzBox-Kindersicherung - so funktioniert die Einrichtung](https://www.heise.de/tipps-tricks/FritzBox-Kindersicherung-so-funktioniert-die-Einrichtung-4048867.html)  
2. Inhalt der [Blacklist *Update 23.11.2020*](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Fritz%20500%202020-11-23.txt) in DEINE  [fritz.box](http://www.fritz.box/) kopieren  
* Natürlich könnt Ihr auch die Blacklisten aus ["Weiterführende Links"](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/README.md#weiterf%C3%BChrende-links-alles-n%C3%BCtzliche-zum-erstellen-einer-eigenen-liste) einsetzen 


läuft auch ohne ein Informatikstudium  
[Fritz!Box als AdBlocker fboës - Der Blog](http://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_internet_filter_blacklist). In der einfachheit der Liste liegt die Anwenderfreundlichkeit.  


[Funktion der Blockliste hier Testen](https://ads-blocker.com/testing/)


Neuen DNS Server (in der Fritzbox einsetzen)
-----------
Meiner Mutter würde ich die Funktion eines DNS Servers mit der Analogie eines Telefonbuch´s erklären.
In der Telefonzelle der Deutschen Post liegt auch ein Telefonbuch der Deutschen Post, wenn dem Telefonbuchhersteller ein Eintrag missfällt, so taucht er in diesem Telefonbuch nicht auf.  
Bei den DNS Servern gibt es dann noch die möglichkeit, dass sich jemand das Telefonbuch vorher anschaut und alles was mit Werbung oder Betrug zu tun hat mit einem Dicken Textmarker ausschwärzt, somit kann ich den Bösen weniger auf den Leim gehen.  
Dazu müssen wir uns erstmal für einen Vertrauenswürdigen DNS Server entscheiden  

[Privacy Handbuch](https://www.privacy-handbuch.de/handbuch_93d.htm)  
[Kuketz Empfehlungsecke](https://www.kuketz-blog.de/empfehlungsecke/#dns)  
[Malwaretips Privacy-Blockers - Application / OS / Lists](https://malwaretips.com/threads/privacy-blockers-application-os-lists.97289/)  
[Kuketz Werbung und Tracker unter iOS/Android systemweit verbannen](https://www.kuketz-blog.de/fuer-anfaenger-bequeme-werbung-und-tracker-unter-ios-android-systemweit-verbannen/)  
Mir hat der Der 2te Dismail DNS Server zugesagt IPv4: **159.69.114.157** für´s Handy unter Private DNS **fdns2.dismail.de**  
ansonsten gibt es noch DNS Server mit Integriertem Werbeblocker (Pihole)  Dismail ist soweit empfehlenswert, googleadservices. werden abgeschossen  
 [DNS Privacy](https://avoidthehack.com/best-dns-privacy#ataglance) soweit oke, da muss man halt vertrauen haben  
[pi-dns.com](https://pi-dns.com/)  soweit oke, da muss man halt vertrauen haben  
~~[Media Techport by Patrick Asmus](https://www.media-techport.de/free-dns-server/)   soweit oke, da muss man halt vertrauen haben~~  
[AdGuard DNS](https://adguard.com/de/adguard-dns/overview.html)  größerer Anbieter scheint soweit Seriös  
[AH DNS](https://ahadns.com/)


um zu testen ob alles geklappt hat
[Adblock Testseite](https://blockads.fivefilters.org/?pihole)  
[DNS Leak Test](https://www.dnsleaktest.com/)  
[Domain Name Speed Benchmark](https://www.grc.com/dns/benchmark.htm)  
Hierzu einfach die Standart Liste gegen [DNS Liste.ini](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/DNS%20Liste.ini) austauschen  
![Einstellungen in DNS Benchmark](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/rect875.jpg)  
  ![sieht das ganze dann so aus](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/servertest.png)

Weiterführende Links (alles Nützliche zum erstellen einer eigenen Liste)
------------
[Pi Hole in der Google Cloud](https://github.com/rajannpatel/Pi-Hole-PiVPN-on-Google-Compute-Engine-Free-Tier-with-Full-Tunnel-and-Split-Tunnel-OpenVPN-Configs)  
[The Firebog](https://firebog.net/)  
[StevenBlack/hosts](https://github.com/StevenBlack/hosts)  

Schwerpunkt Fritzbox  
[xobit.de/fritzbox-blacklist](https://www.xobit.de/fritzbox-blacklist)  
[fboes/fritzbox-blacklist](https://github.com/fboes/fritzbox-blacklist)  
[shizoworld.de/2019/12/blockliste-der-fritzbox-nutzen/](https://shizoworld.de/2019/12/blockliste-der-fritzbox-nutzen/)  
[Kuketzblog weiterführende diskussion](https://forum.kuketz-blog.de/viewtopic.php?t=5147)  
  
Kowabit Stuff  
[Fritzbox Blacklist 17.01.2020](https://kowabit.de/fritzbox-blacklist-17-01-2020/)  
[Den Einsatz der Blockliste erklärt (Update)](https://kowabit.de/den-einsatz-der-blockliste-erklaert/)  
[Blacklist – Sicherheit durch Zensur :c)](https://kowabit.de/blcklst/)    
  
  Eigene Filterliste erstellen  
  [Notepad++](https://notepad-plus-plus.org/)  
  [Textfixer Doppelte Zeilen entfernen](https://www.textfixer.de/tools/doppelte-zeilen-entfernen.php)  
  [Domain Extractor](https://de.rakko.tools/tools/62/) falls down [domaincheckplugin.com/extractor](http://domaincheckplugin.com/extractor)  
  [SPAMHAUS The 10 Most Abused Top Level Domainst](https://www.spamhaus.org/statistics/tlds/)  
  [AM-Deadlink](https://www.aignes.com/deadlink.htm)  checkt ob die Seite noch online ist bzw existiert  

-----------
Original: [Frank Boës](http://3960.org) and others
