# android-7.1
Main repository with Android 7.1 releases

## Prepare device for flashing

1. Compile and install `rkflashtool`:
    ```bash
    git clone https://github.com/ayufan-rock64/rkflashtool
    make -C rkflashtool
    sudo make -C rkflashtool install
    ```

1. Connect USB A-to-A cable to upper USB 2.0 port and your computer,

1. Start Rock64 in Loader mode:
    1. Press and hold Recovery Bt
    1. Press Reset Btn,
    1. Stop holding Recovery Btn after 3s.

    To verify device:

    ```bash
    rkflashtool n
    ...
    ```

    You can also start device in Maskrom mode:
    1. Shorten eMMC PIN,
    2. Start device.

## Download release

1. Go to: https://github.com/ayufan-rock64/android-7.1/releases

2. Download and extract one of the releases (without `-update.zip` at end), ex.: https://github.com/ayufan-rock64/android-7.1/releases/download/0.1.0/android-7.1-rock-64-rk3328_box-v0.1.0-r37.zip,

The releases:
1. Without `-update.zip` are for manual procedure on Linux/OSX,
2. With `-update.zip` are for Android Upgrade Tool for Windows,

## Install on Linux/OSX

1. Create a installation script:

```bash
sudo tee /usr/local/bin/rkinstall <<"EOF"
#!/bin/bash

set -xe

rkflashtool P < parameter.txt
for i in uboot trust misc kernel boot recovery system; do
    rkflashtool w $i < $i.img
done
rkflashtool b
EOF

sudo chmod +x /usr/local/bin/rkinstall
```

2. Execute script from within directory:

```bash
$ rkinstall
```

## Upgrade on Linux/OSX

1. Create upgrade script

```bash
sudo tee /usr/local/bin/rkupgrade <<"EOF"
#!/bin/bash

set -xe

for i in uboot trust kernel boot recovery system; do
    rkflashtool w $i < $i.img
done

rkflashtool b
EOF

sudo chmod +x /usr/local/bin/rkupgrade
```

2. Execute upgrade script from within directory:

```bash
$ rkupgrade
```

## Author

Kamil Trzciński, 2017, https://ayufan.eu
