# brain-api-doc

## Installation MacOs

### Install with a Package Manager

If you have and use a package manager (such as [apt-get], [dnf], [homebrew],
[yum], [chocolatey], etc.) to install packages on your system, then you may
want to search for a "MkDocs" package and, if a recent version is available,
install it with your package manager (check your system's documentation for
details). That's it, you're done! Skip down to [Getting Started](#getting-started).

If your package manager does not have a recent "MkDocs" package, you can still
use your package manager to install "Python" and "pip". Then you can use pip to
[install MkDocs](#installing-mkdocs).

[apt-get]: https://help.ubuntu.com/community/AptGet/Howto
[homebrew]: http://brew.sh/
[dnf]: http://dnf.readthedocs.io/en/latest/index.html
[yum]: http://yum.baseurl.org/
[chocolatey]: https://chocolatey.org/

### Manual Installation

In order to manually install MkDocs you'll need [Python] installed on your
system, as well as the Python package manager, [pip]. You can check if you have
these already installed from the command line:

```bash
$ python --version
Python 2.7.2
$ pip --version
pip 1.5.2
```

MkDocs supports Python versions 2.6, 2.7, 3.3, 3.4, 3.5 and pypy.

#### Installing Python

Install [Python] by downloading an installer appropriate for your system from
[python.org] and running it.

!!! Note

    If you are installing Python on Windows, be sure to check the box to have
    Python added to your PATH if the installer offers such an option (it's
    normally off by default).

    ![Add Python to PATH](img/win-py-install.png)

[python.org]: https://www.python.org/downloads/

#### Installing pip

If you're using a recent version of Python, the Python package manager, [pip],
is most likely installed by default. However, you may need to upgrade pip to the
lasted version:

```bash
pip install --upgrade pip
```

If you need to install [pip] for the first time, download [get-pip.py].
Then run the following command to install it:

```bash
python get-pip.py
```

#### Installing MkDocs

Install the `mkdocs` package using pip:

```bash
pip install mkdocs
```

You should now have the `mkdocs` command installed on your system. Run `mkdocs
--version` to check that everything worked okay.

```bash
$ mkdocs --version
mkdocs, version 0.15.3
```
