# Python for Actions
This repository contains the code and scripts that we use to build Python packages used in [runner-images](https://github.com/actions/runner-images) and accessible through the [setup-python](https://github.com/actions/setup-python) Action.
File [versions-manifest.json](./versions-manifest.json) contains the list of available and released versions.

> Caution: this is prepared for and only permitted for use by actions `runner-images` and `setup-python` action.

Some versions are pre-installed on [runner-images](https://github.com/actions/runner-images) images.
More versions are available to install on-the-fly through the [`setup-python`](https://github.com/actions/setup-python) action.

## Building installation packages
**Ubuntu:** The official Python sources are downloaded from [python.org](https://www.python.org/ftp/python/), built with additional configurations using the make tool and archived along with the installation script for further distribution and installation. We build a Python version against all available [Ubuntu versions](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#supported-runners-and-hardware-resources).

**macOS:** 
- Python < 3.11. The official Python sources are downloaded from [python.org](https://www.python.org/ftp/python/), built with additional configurations using the make tool and archived along with the installation script for further distribution and installation. We build a Python version against the oldest available macOS version for backward compatibility. Available macOS GitHub-hosted runners can be found [here](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#supported-runners-and-hardware-resources).
- Python >= 3.11. The official macOS `universal2` Python binaries are simply downloaded from [python.org](https://www.python.org/ftp/python/) and archived along with the installation script for further distribution and installation.

**Windows:** The official Python executables are simply downloaded from [python.org](https://www.python.org/ftp/python/) and archived along with the installation script for further distribution and installation.

## Support policy
We aim to make new versions of Python available as soon as they are released. Both stable and prerelease versions are considered for building and releasing. Please open an issue in [actions/setup-python](https://github.com/actions/setup-python) if a version you're looking for isn't available.

When a new version of an operating system is released and made available for use with [GitHub hosted runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#supported-runners-and-hardware-resources), we will provide the **latest existing patch versions of Python for all major versions that have not reached [end-of-life](https://devguide.python.org/versions/)**.  Any subsequent Python versions will be made available for the new OS as well.

## Contribution
Contributions are welcome! See [Contributor's Guide](./CONTRIBUTING.md) for more details about contribution process and code structure
