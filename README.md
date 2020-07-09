:do_not_litter: (Fritz!Box)  Bl**o**cklist für die Internetkiste
===================================
Readme inspired by [🚯 Fritz!Box Blacklist](https://github.com/fboes/fritzbox-blacklist) by [fboes](https://github.com/fboes)

Mein versuch die Welt mit möglichst einfachen Technischen Mitteln ein bisschen besser zu machen...
Da die unmodifizierte Fritzbox leider nur mit 500 Einträgen zurechtkommt, versuche ich hier eine möglichst kurze aber dennoch effektive Liste mit den Alltime TOP 500 geblockten webseiten zu erstellen.  
Mir ist bewusst das das WWW veränderlich ist und die ein oder andere Seite eines Tages nichtmehr aktuell ist aber einem großteil des InterCraps kann man somit vielleicht schon umgehen, auch ohne π **🕳**

Instructions
------------

Short instructions:

1. See [AVM's instructions on how to setup a blacklist in your Fritz!Box](http://en.avm.de/service/fritzbox/fritzbox-7490/knowledge-base/publication/show/8_Restricting-Internet-access-using-parental-controls/)
2. Copy contents of [fritzbox-blacklist.txt](https://raw.githubusercontent.com/fboes/fritzbox-blacklist/master/fritzbox-blacklist.txt) to your Fritz!Box' blacklist
2. Copy contents of [fritzbox-blacklist-extra.txt](https://raw.githubusercontent.com/fboes/fritzbox-blacklist/master/fritzbox-blacklist-extra.txt) to your Fritz!Box' blacklist for the removal of possibly nice services
4. Be sure to check if HTTPS traffic is still allowed

This will work with a standard firmware.

There is also an [extended instruction on how to set up your Fritz!Box as an AdBlocker](https://journal.3960.org/posts/2015-07-02-fritz-box-als-adblocker/) (German).



Development
-----------

There is a maximum of 500 entries for the Fritz Box' blacklist. Choose each entry wisely.

Put each domain in a single line. Do not enter comments or anything else.

E.g.: To block `http://ads.example.com/some_script.js` enter `ads.example.com` or just `example.com`. `example.com` will also block all files from `www.example.com` and any other subdomain.

On the structure of URLs for this blacklist consult [AVM's documentation for blacklists](http://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_internet_filter_blacklist). Keep in mind to keep this list as simple as possible, to keep it useful for other routers as well.

Contributing
------------

I am happy to merge your contributions to this file. Please make sure that the blacklist is ordered alphabetically, and you have removed any unneccessary whitespaces.

Legal stuff
-----------

Author: [Frank Boës](http://3960.org) and others

Copyright & license: See LICENSE.txt

These instructions are NOT affiliated with, endorsed, or sponsored by AVM.
