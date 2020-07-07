# FritzBoxBlacklist
kurze aber knackige Blacklist für die Fritzbox (unter 500 Einträge), blockiert schonmal einen großen Teil Werbung und Scripte
🚯 Fritz!Box Blacklist
A list of domains to be blocked in my Fritz!Box (and maybe yours).

This project is meant to help some companies to see the benefits of HTTPS. 😃

Instructions
Short instructions:

See AVM's instructions on how to setup a blacklist in your Fritz!Box
Copy contents of fritzbox-blacklist.txt to your Fritz!Box' blacklist
Copy contents of fritzbox-blacklist-extra.txt to your Fritz!Box' blacklist for the removal of possibly nice services
Be sure to check if HTTPS traffic is still allowed
This will work with a standard firmware.

There is also an extended instruction on how to set up your Fritz!Box as an AdBlocker (German).

Know issues
Domain	Issue
conduit.com	This entry may prevent some Netflix clients like Wii U from using Netflix (see issue #6 for details)
googleadservices.com	This entry makes the paid links in Google search results unclickable
Development
There is a maximum of 500 entries for the Fritz Box' blacklist. Choose each entry wisely.

Put each domain in a single line. Do not enter comments or anything else.

E.g.: To block http://ads.example.com/some_script.js enter ads.example.com or just example.com. example.com will also block all files from www.example.com and any other subdomain.

On the structure of URLs for this blacklist consult AVM's documentation for blacklists. Keep in mind to keep this list as simple as possible, to keep it useful for other routers as well.

Contributing
I am happy to merge your contributions to this file. Please make sure that the blacklist is ordered alphabetically, and you have removed any unneccessary whitespaces.

Legal stuff
Author: Frank Boës and others

Copyright & license: See LICENSE.txt

These instructions are NOT affiliated with, endorsed, or sponsored by AVM.
