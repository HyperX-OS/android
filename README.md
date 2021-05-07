## Build the ROM!
To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).
### Initialize your local repository using this command:
```bash
repo init -u https://github.com/HyperX-OS/android -b 11
```
### Sync the ROM sources using this command:
```bash
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```
### Initiate build:
```bash
source build/envsetup.sh
lunch hyper_<devicecodename>-userdebug
make bacon
```
