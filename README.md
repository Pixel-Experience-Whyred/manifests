# TwistUI #

## Initialization and Syncing:
1. Initialize your local repository:
    ```bash
    repo init --no-repo-verify --git-lfs -u https://github.com/TwistUI/manifests.git -b 13 -g default,-mips,-darwin,-notdefault
    ```
   Or If you wish to save some system space and don't care about repo history depths:
    ```bash
    repo init --depth=1 --no-repo-verify --git-lfs -u https://github.com/TwistUI/manifests.git -b 13 -g default,-mips,-darwin,-notdefault
    ```
2. Sync up with the remote repository:
    ```bash
    repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
    ```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -j$(nproc --all)
```

### A rom based on Pixel Experience Thirteen ###

### Credits ###

- Pixel Experience
- Omni Rom
- Project Matrixx
- crDroid
