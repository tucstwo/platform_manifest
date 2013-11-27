Kitkat local_manifest
======================
 
Local Manifest for building AOKP on our supported Devices
 
Getting Started
---------------
 
To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).
 
Make a build directory:
 
        mkdir Andoid (or whatever name you choose)
        cd Android (or the name  you chose)
        mkdir .repo/local_manifests
 
Init repo only for official devices first:
 
    repo init -u https://github.com/AOKP/platform_manifest.git -b jb-kitkat -g all,-notdefault,jfltevzw,samsung
 
Then download additional repo's for unofficial devices:
 
    curl -L -o .repo/local_manifests/droidfx.xml -O -L https://raw.github.com/usmcamgrimm/local_manifest/kitkat/usmcamgrimm.xml
 
        ( or Download: https://github.com/usmcamgrimm/local_manifest/blob/kitkat/usmcamgrimm.xml
                and place it in your ~/Android/.repo/local_manifest.xml (or ~/'name you choose'/.repo)
 
Then sync up:
 
    repo sync
