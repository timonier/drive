# README

## Installation

Copy the script `bin/drive` into your executable folder (like `/usr/local/bin` or `$HOME/bin`).

```sh
sudo curl -sLo /usr/local/bin/drive "https://github.com/timonier/drive/raw/master/bin/drive"
sudo chmod +x /usr/local/bin/drive
```

Linux users can use the [installer](https://github.com/timonier/drive/blob/master/bin/installer):

```sh
curl -sL "https://github.com/timonier/drive/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the script `drive`:

```sh
drive init ~/gdrive
cd ~/gdrive
drive pull
```

__Note__: By default, the version `0.3.3` will be used. To change the version, define the `TAG` before the command:

```sh
drive version
# drive version: 0.3.3
# ...

TAG="0.3.2" drive version
# drive version: 0.3.2
# ...
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [drive](https://github.com/odeke-em/drive)
* [image "timonier/drive"](https://hub.docker.com/r/timonier/drive/)
