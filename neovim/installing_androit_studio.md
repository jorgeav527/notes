1. Install java
   - `sudo apt update && sudo apt install default-jdk -y && java --version`
2. Download the [Android Studio Koala Feature Drop | 2024.1.2 RC 1](https://developer.android.com/studio/preview)
3. To install Android Studio on Linux, follow these steps:
   - Required libraries for 64-bit machines Debian 12
     - `sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386`
   - Unpack the .tar.gz file you downloaded to an appropriate location for your applications, such as within /usr/local/ for your user profile or /opt/ for shared users.
   - `cd Downloads/ && sudo tar -xzvf android-studio-2024.1.2.11-linux.tar.gz -C /usr/local/`
   - To launch Android Studio, open a terminal, navigate to the android-studio/bin/ directory, and execute studio.sh.
   - `cd /usr/local/android-studio/bin/ && ./studio.sh`
   - Complete the Android Studio Setup Wizard, which includes downloading the Android SDK components that are required for development.
