# POX OS Source Manifest (Pure AOSP Base)

<p align="center">
  <img src="https://avatars.githubusercontent.com/u/338706181?v=4" width="150" alt="POX OS Logo" />
  <br>
  <b>Reinventing Android Aesthetics & Performance on Pure AOSP</b>
  <br>
  <i>Engineered to DevSkill Standards: Project Treble, GSI Ready, Strict SELinux & Stable AIDL</i>
</p>

---

## 🏛️ Architecture & Upstream Base

POX OS is built directly upon the official **Android Open Source Project (AOSP)** upstream (`android-15.0.0_r14`):
- **Upstream Foundation**: Pure Google AOSP platform tree (`https://android.googlesource.com`).
- **Treble Segregation**: Pure separation between `/system` and `/vendor` partitions using Stable AIDL HALs.
- **Custom Enhancements**: Concentrated in `vendor/pox`, `frameworks/base`, `packages/apps/Settings`, and `packages/apps/PoxHub` (placed in `/system_ext`).

---

## 🚀 Getting Started

### 1. Initialize the Source Repository
```bash
repo init -u https://github.com/pox-os/manifest -b pox-15.0 --git-lfs
```

### 2. Synchronize the Source Tree
```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### 3. Build for Generic Target (ARM64 GSI / Emulator)
```bash
source build/envsetup.sh
lunch pox_arm64-trunk_staging-userdebug
m pox
```
