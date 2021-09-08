Guy who made a SRB2 Uncapped Plus Appimage

--To get the git and build it:
```
git clone https://git.do.srb2.org/Fafabis/SRB2.git
cd SRB2
git checkout uncapped-plus
make LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme -C src/ LINUX64=1
```

--To Pull/Update:
```
cd SRB2
git pull
```
Then compile it all over again:
```
make LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme -C src/ LINUX64=1
```

Or if you want to do it the easy way, just download the AppImage file from my releases tab and just get the necessary srb2 resources (like srb2.pk3 and stuff) from here:

https://github.com/STJr/SRB2/releases/download/SRB2_release_2.2.9/SRB2-v229-Full.zip
