# ApplePhotoProgram
Script to download photos from Apple's Photo application in iCloud

I have created a quick python program to download your Apple Photos direct from icloud to your NAS. It works great for me, but do remember that this is not a formal licensed program but instead is just a python script used for my own purposes and as such no guarantees or rights, etc... It is two files, main.py which is the python program and then config.ini which holds the configuration items. Since this post does not let me attach them as files, I will add the text below and you can cut and past into files and then run them with python to do your bidding.

The program does require some libraries to be installed via pip (see the import section) if you have not loaded them. The big one that lets you get into icloud is called pyicloud and is a great library and does more than just icloud photos. I am running the beta version of Python 3.9 as some of the imports are 3.7 and above I believe. I just run it via python main.py and it goes. It is a little verbose as again it is just me getting started with the program.

A few items to keep in mind. In the config file there are two ways to download photos. One is all photos based on their added date (the date added to your library in photos on icloud) back to the "date_from" date in config.ini. The format is specific year-month-day so keep to that format (shown in the ini file). The other way is by album, but also constrained by the added date as all photos would be. So if you want all photos in the album, just put an old date out there.

Another constraint which is in there to keep me from messing up is a parameter in the ini file for maxphotos. This limits the number of photos downloaded during a session. I set it low when I started to ensure it was doing what I wanted.

As far as where the photos go, it will go to the directory that you add in ini file and then automatically builds a structure based on the photo's created date /directory/2022/06/21/... That is sadly hard coded in the program, so feel free to change that if you want.
