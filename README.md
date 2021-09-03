# What is this?
This is a simple local manifest for me to use when I sync. This is NOT meant for CI services like cirrus and has ONLY been tested on my local PC running Zorin OS 15.3 (5.4.0-81-generic) with a normal Android build environment setup. Instructions for usage can be found below.

## Sync instructions
<br>

```
$ repo init -u https://github.com/ProjectRadiant/manifest -b eleven
$ cd .repo
$ git clone --single-branch --branch eleven https://github.com/Maitreya29/local_manifest local_manifests
$ cd ..
$ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## Build instructions
<br>

```
$ . build/env*
$ lunch radiant_dumpling-user
$ mka bacon -j12
```

and the OTA zip will be available in `out/target/product/dumpling`.