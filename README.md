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
