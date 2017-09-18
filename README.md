# README

Pull or push Google Drive files

## Installation

Copy `bin/drive` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/drive "https://github.com/timonier/drive/raw/master/bin/drive"
sudo chmod +x /usr/local/bin/drive
```

Linux users can use the [installer](https://github.com/timonier/drive/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/drive/raw/master/bin/installer" | sudo sh -s -- install
```

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

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [odeke-em/drive](https://github.com/odeke-em/drive)
* [image "timonier/drive"](https://hub.docker.com/r/timonier/drive/)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
