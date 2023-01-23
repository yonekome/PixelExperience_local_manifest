# How to build unofficial Pixel Experience

###  Install the platform-tools ###

```bash
# Initialize local repository
[repo init -u https://github.com/Evolution-X/manifest -b tiramisu](https://dl.google.com/android/repository/platform-tools-latest-linux.zip)

# Clone my custom manifest
git clone -b tiramisu https://github.com/nattolecats/local_manifests .repo/local_manifests

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

```

### Build ###

```bash

# Set up environment
. build/envsetup.sh

# Choose a target
lunch evolution_denniz-userdebug

# Build the code
m evolution
```
