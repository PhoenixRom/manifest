<p align="center">
<img src="https://i.imgur.com/vizqDrY.png" > 
</p>

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Prepare Your Environment:

```bash
sudo apt install git-core gperf bc bison build-essential ccache curl flex g++-multilib gcc-multilib git gnupg gperf imagemagick
lib32ncurses5-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libwxgtk3.0-dev libxml2
libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc libc6-dev-i386 x11proto-core-dev libx11-dev libgl1-mesa-dev
zip unzip zlib1g-dev -y
```

Install Repo:

```bash
mkdir -p ~/bin
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```

To initialize your local repository, use a command like this:

	repo init -u https://github.com/Project-Titanium/manifest.git -b 10.0

Then to sync up:

	repo sync --force-sync --no-tags --no-clone-bundle -j$(nproc --all)

----------------------------------
 Compilation of ProjectTitanium
 ==================

From root directory of the ROM, perform following commands in terminal


```bash
source build/envsetup.sh

lunch pti_<codename>

brunch <codename>
```
