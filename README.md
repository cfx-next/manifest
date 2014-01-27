codefireX(periment)
===========


Getting Started
---------------

To get started with codefireX(periment), you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Init core trees without any device/kernel/vendor :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel

Init repo with all devices, kernels and vendors supported by codefireXperiment :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel -g all,kernel,device,vendor

Init repo only for a particular device :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel -g all,-notdefault,<devicename>,<vendorname>

for example, to init only trees needed to build mako :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel -g all,-notdefault,,mako,lge

Init repo for multiple devices :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel -g all,-notdefault,<devicename1>,<devicename2>,<devicename3>,<vendorname1>,<vendorname2>,<vendorname3>

for example, to init trees needed to build mako and grouper :

    $ repo init -u git://github.com/codefireXperiment/android_manifest.git -b kk-devel -g all,-notdefault,mako,grouper,lge,asus

Then to sync up:

    repo sync
