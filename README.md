# README

Pull or push Google Drive files

If you like / use this project, please let me known by adding a ★ on the [GitHub repository](https://github.com/timonier/drive).

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://github.com/timonier/drive/raw/master/bin/installer" | sudo bash -s -- install
```

__Note 1__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

__Note 2__: `docker-for-mac` users have to configure [native NFS server](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc).

## Usage

Run the command `drive`:

```sh
# See all drive options

drive --help

# Run drive

drive init ~/gdrive
cd ~/gdrive
drive pull
```

## Links

* [odeke-em/drive](https://github.com/odeke-em/drive)
* [image "timonier/drive"](https://hub.docker.com/r/timonier/drive/)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/drive](https://github.com/timonier/drive)
