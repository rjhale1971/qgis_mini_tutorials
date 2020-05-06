Software: QGIS

Platform: Ubuntu Linux 

Due to numerous questions from other people and some emails from people I'm hopefully going to describe how to install QGIS for Linux - specifially the Ubuntu Desktop. Of course - as always the definitive source is https://qgis.org/en/site/forusers/alldownloads.html#debian-ubuntu

First thing you need to figure out is *what version are you running?*. I will assume for the tutorial is that you are on one of these two Ubuntu versions: 

* 17.10 - artful 
* 18.04 - bionic 
* 18.10 
* 19/04 - disco

Run this command: 

***sudo sh -c 'echo "deb https://qgis.org/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/qgis.list'*** 

Then run: 

***wget -O - https://qgis.org/downloads/qgis-2017.gpg.key | gpg --import***

This is going to make sure the server is who the server says it is. Security is **important**. Check the output: 

***gpg --fingerprint CAEB3DC3BDF7FB45***

Which should show you: 

***pub   2048R/BDF7FB45 2017-08-16 [expires: 2019-08-16]
      Key fingerprint = 61E0 A086 749E 463E DE50  2255 CAEB 3DC3 BDF7 FB45
uid                  QGIS Archive Automatic Signing Key (2017) <qgis-developer@lists.osgeo.org>
sub   2048R/E959BBCF 2017-08-16 [expires: 2019-08-16]***

If it all matches then do: 

***gpg --export --armor CAEB3DC3BDF7FB45 | sudo apt-key add -***

after all that is done you're almost at the end! Just run: 

***sudo apt-get update***

***sudo apt-get install qgis python-qgis qgis-plugin-grass***  

Questions: 

What about Linux Mint? *I don't know* 

What about something based on Debian but not Ubuntu? *I don't know* 

As always - check the official documentation for QGIS as that will always be the gold standard. 


