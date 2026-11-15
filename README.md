# POX OS Source Manifest

<p align="center">
  <img src="https://avatars.githubusercontent.com/u/338706181?v=4" width="150" alt="POX OS Logo" />
  <br>
  <b>Reinventing Android Aesthetics & Performance</b>
</p>

POX OS is a clean, modern, and highly aesthetic custom Android distribution built on top of LineageOS and AOSP.

---

## Getting Started

### 1. Initialize the Source Repository
```bash
repo init -u https://github.com/pox-os/manifest -b pox-15.0 --git-lfs
```

### 2. Synchronize Source Tree
```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### 3. Build for Your Device
```bash
source build/envsetup.sh
lunch pox_<device_codename>-userdebug
m pox
```
