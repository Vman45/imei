<div align=center>

# IMEI - ImageMagick Easy Install
#### Automated ImageMagick compilation from sources for Debian/Ubuntu including advanced delegate support.

[![Build](https://img.shields.io/github/workflow/status/SoftCreatR/imei/TestBuild?label=Build&style=flat-square)](https://github.com/SoftCreatR/imei/actions?query=workflow%3ATestBuild) [![Shellcheck](https://img.shields.io/github/workflow/status/SoftCreatR/imei/Shellcheck?label=Shellcheck&style=flat-square)](https://github.com/SoftCreatR/imei/actions?query=workflow%3AShellcheck)

[![Commits](https://img.shields.io/github/last-commit/SoftCreatR/imei?style=flat-square)](https://github.com/SoftCreatR/imei/commits/main) [![GitHub release](https://img.shields.io/github/release/SoftCreatR/imei?style=flat-square)](https://github.com/SoftCreatR/imei/releases) [![GitHub license](https://img.shields.io/github/license/SoftCreatR/imei?style=flat-square&color=lightgray)](https://github.com/SoftCreatR/imei/blob/main/LICENSE) ![Installs](https://img.shields.io/badge/dynamic/json?style=flat-square&color=blue&label=Installs&query=value&url=https%3A%2F%2Fapi.countapi.xyz%2Fget%2Fsoftcreatr%2Fimei) [![GitHub file size in bytes](https://img.shields.io/github/size/SoftCreatR/imei/imei.sh?style=flat-square)](https://github.com/SoftCreatR/imei/blob/main/imei.sh)

[![Codacy grade](https://img.shields.io/codacy/grade/325d797fcbbf44df9dbed8af3ba8e1f4?style=flat-square)](http://app.codacy.com/manual/SoftCreatR/imei/dashboard?token=hIBh9xPtZzernpa) [![CodeFactor Grade](https://img.shields.io/codefactor/grade/github/SoftCreatR/imei?style=flat-square)](https://www.codefactor.io/repository/github/softcreatr/imei)

</div>

---

<div align="center">

<a href="#features"> Features<a> •
<a href="#compatibility"> Compatibility</a> •
<a href="#usage"> Usage</a> •
<a href="#roadmap"> Roadmap</a> •
<a href="#contributing"> Contributing</a> •
<a href="#license"> License</a>

![Screenshot](https://raw.githubusercontent.com/SoftCreatR/imei/main/imei.png)

</div>

---

## Features

* Compiles the latest ImageMagick release
* Installs ImageMagick or replaces ImageMagick package previously installed
* Additional HEIF support
* Additional HEIX support
* Additional AVIF support
* Automated updates via cronjob (optional)

---

## Compatibility

Every IMEI build will be automatically tested against the latest Ubuntu LTS Versions (16.04 and newer) using Travis CI. Compatibility with other operating systems (such as Debian 10) is tested manually.

### Operating System

#### Recommended

* Ubuntu 20.04 LTS (__Focal__ Fossa)
* Ubuntu 18.04 LTS (__Bionic__ Beaver)
* Debian 10 (__Buster__)
* Raspbian 10 (__Buster__)

#### Also compatible

* Ubuntu 19.10 (__Eoan__ Ermine)
* Ubuntu 16.04 LTS (__Xenial__ Xerus)
* Debian 9 (__Stretch__)
* Raspbian 9 (__Stretch__)

---

## Usage

### One-Step Automated Install

```bash
bash <(wget -qO - 1-2.dev/imei || curl -sL 1-2.dev/imei)
```

### Alternative Install Method

```bash
git clone https://github.com/SoftCreatR/imei
cd imei
sudo imei.sh
```

#### Options available

Currently available build options are

* `--imagemagick-version` : Build the given ImageMagick version (e.g. `7.0.10-28`)
* `--aom-version` : Build the given aom version (e.g. `2.0.0`)
* `--libheif-version` : Build the given libheif version (e.g. `1.8.0`)
* `--log-file` : Log everything to the file provided
* `--work-dir` : Download, extract & build within the directory provided
* `--force-build` : Force building of components, even if they are already installed in a newer or the latest version

**Default options** :

<!-- versions start -->
* ImageMagick version: `7.0.10-31`
* libaom version: `2.0.0`
* libheif version: `1.9.1`<!-- versions end -->
* Log File: `/var/log/install-imagemagick.log`
* Work Dir: `/usr/local/src/imei`
* Force Build: No

---

## Roadmap

* [x] Add cronjob for automatic updates
* [ ] Add ImageMagick modules choice
* [ ] CentOS 8 compatibility

## Contributing

If you have any ideas, just open an issue and describe what you would like to add/change in IMEI.

If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

## License

[MIT](https://github.com/SoftCreatR/imei/blob/main/LICENSE) © [1-2.dev](https://1-2.dev)
