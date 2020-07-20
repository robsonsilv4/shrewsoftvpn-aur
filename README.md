# Shrew Soft VPN Client (ike)

Shrew Soft VPN Client (ike) for Arch Linux, Manjaro and derivated.

This repository contains the builded package ready for install and the PKGBUILD updated with fixes, patches and files for build.

## How to install

1 - Clone the repository:

```sh
git clone https://github.com/robsonsilv4/shrewsoftvpn-archlinux.git

cd shrewsoftvpn-archlinux
```

2 - Install the package:

```sh
sudo pacman -U ike-2.2.1-6-x86_64.pkg.tar.xz
```

3 - Enable and/or start iked service:

```sh
sudo systemctl enable iked.service
# and/or
sudo systemctl start iked.service
```

4 - If you use LDAP, also install _openldap_ (optional):

```sh
sudo pacman -Sy openldap
```

5 - Just if you want to compile the package again (optional):

```sh
makepkg -si
```

## How to use

1 - Copy your configuration files to sites folder:

```sh
mkdir -p ~/.ike/sites

cp YOUR_SETTINGS ~/.ike/sites
```

2 - And run with:

```sh
ikec -r YOUR_SETTINGS -u user -p password -a
```

## Tips

- For disconnect, type _d_.
- And for reconnect, type _c_.

## Credits

- All credits reserved for Shrew Soft, the author of [Shrew Soft VPN Client (ike)](https://www.shrew.net/download/ike).
- Original [AUR PKGBUILD](https://aur.archlinux.org/packages/ike/) and the contributors.

## License

This repository is under the terms of [MIT License](./LICENSE).
