Guy who made a SRB2 Uncapped Plus Appimage for Linux.

STEP 1
--To get the git and build it:
```
git clone https://git.do.srb2.org/Fafabis/SRB2.git
cd SRB2
git checkout uncapped-plus --You can select uncapped-plus-test to get tests for uncapped plus if you want.
```

--Alright, now we need to get the steps for getting discord rich presence to work. Credits to https://kart.moe/building-srb2-kart-for-linux/ for the help.
--However, if you don't want discord rich presence enabled, you can just type the following in:

On Ubuntu 20.04 and below, or Debian 10 and below:

```
LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme make -C src/ LINUX64=1 --64 Bit Linux
LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme make -C src/ LINUX=1 --32 Bit Linux
```

On Ubuntu 20.10 and above, Debian 11 and above, or Arch:

Run this command first:

```
sudo apt install pkg-config
```

Then:

```
make -C src/ LINUX64=1 --Linux 64 Bit
make -C src/ LINUX=1 --Linux 32 Bit
```

Alright, first, in order to enable discord rich presence, you're going to want to https://github.com/discord/discord-rpc/releases and get the most recent Linux discord rich presence (discord-rpc) build.

Next, once you get these files, you're going to want to extract and get the following files:

```
discord_register.h
discord_rpc.h
libdiscord-rpc.so
```

Once you get these, you'll want to run the following command in your terminal to access your root files:

```
sudo chown -R $USER /usr/local
sudo chown -R $USER /usr/local/lib --Or /usr/lib/ if putting ```libdiscord-rpc.so``` in usr/local/lib happens to not work.
```

Now, put ```discord_register.h``` and ```discord_rpc.h``` into /usr/local/include/, and put ```libdiscord-rpc.so``` into /usr/local/lib/ --if srb2 doesn't run once you make the git repository then take ```libdiscord-rpc.so``` from /usr/local/lib/ and place it into /usr/lib/.

Alright, now you can finally make your srb2 build. Run the following command into the terminal:

On Ubuntu 20.04 and below, or Debian 10 and below:

```
LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme make -C src/ LINUX64=1 HAVE_DISCORDRPC=1 --64 Bit Linux
LIBGME_CFLAGS=-I/usr/include LIBGME_LDFLAGS=-lgme make -C src/ LINUX=1 HAVE_DISCORDRPC=1 --32 Bit Linux
```

On Ubuntu 20.10 and above, Debian 11 and above, or Arch:

Run this command first:

```
sudo apt install pkg-config
```

Then:

```
make -C src/ LINUX64=1 HAVE_DISCORDRPC=1 --Linux 64 Bit
make -C src/ LINUX=1 HAVE_DISCORDRPC=1 --Linux 32 Bit

```

Once you finally get the notice that your build is done, you can grab lsdl2srb2 in the /bin folder in your git repository.
You can even rename, or put .AppImage at the end of the lsdl2srb2 file it if you want!

--To Pull/Update:

```
cd SRB2
git pull
```

Then compile it all over again.

Or if you want to do it the easy way, just download the AppImage file from my releases tab and just get the necessary srb2 resources (like srb2.pk3 and stuff) from here https://github.com/STJr/SRB2/releases/download/SRB2_release_2.2.9/SRB2-v229-Full.zip
