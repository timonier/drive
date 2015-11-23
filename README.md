### Installation

Copy the script `bin/drive` into your executable folder (like `/usr/local/bin` or `$HOME/bin`).

```bash
sudo curl -sLo /usr/local/bin/drive https://github.com/mauchede/aria2/raw/master/bin/drive
sudo chmod +x /usr/local/bin/drive
```

### Usage

Run the script `drive`:

```bash
drive version
# drive version: 0.3.2
# ...

drive init ~/gdrive
cd ~/gdrive
drive pull
```

__Note__: By default, the version `0.3.2` will be used. To change the version, define the `TAG` before the command. For example:

```bash
drive version
# drive version: 0.3.2
# ...

TAG="0.2.9" drive version
# drive version: 0.2.9
# ...
```

### Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

### Links

* [image "mauchede/drive"](https://hub.docker.com/r/mauchede/drive/)
* [odeke-em/drive](https://github.com/odeke-em/drive)
