Orfox
=====

September 2018
--------------

Since 2015, Orfox has been the only mobile app recommended by the Tor Project to utilize the privacy protections of Tor on Android. The Tor Project has launched an official browser, Tor Browser for Android, now in its alpha release. Orfox will be sunsetted by early 2019 when the stable Tor Browser for Android comes out. To experience real private browsing without tracking, surveillance, or censorship, download Tor Browser for Android from Google Play here: https://play.google.com/store/apps/details?id=org.torproject.torbrowser_alpha.

You will still be able to use Orbot to route the traffic of all your other apps on Android over Tor.

About This Project
------------------

This is a privacy-enhanced browser for Android, based on Mozilla Firefox,
configured by default to work with Orbot: Tor for Android.

You can learn more about the design of Tor Browser here:
https://www.torproject.org/projects/torbrowser/design/

Review the "Orfox Spec" document in this repo for more information on the
design goals and defaults for this browser.

Building
--------

You can find the source information on building "Fennec" for Android (aka
Firefox) from source here:
https://wiki.mozilla.org/Mobile/Fennec/Android#Building_Fennec

Additionally, it is easiest to build when using a specific Android SDK setup
to make sure that the version of things are correct, like the Support libs.

    cd /opt
    wget https://dl.google.com/android/android-sdk_r24.3.4-linux.tgz
    tar xzf android-sdk_r24.3.4-linux.tgz
    export ANDROID_HOME=/opt/android-sdk-linux
    export PATH="$ANDROID_HOME/tools:$PATH"
    android update sdk --no-ui --filter tools,platform-tools,build-tools-23.0.1,android-22
    cd $ANDROID_HOME
    mkdir -p extras/android
    cd extras/android
    wget https://dl.google.com/android/repository/support_r22.2.1.zip
    unzip support_r22.2.1.zip
    chmod -R a+rX $ANDROID_HOME
    find $ANDROID_HOME -executable |xargs chmod a+x
