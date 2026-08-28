# PyxGT: Explore your data with Deep Analytics

---

#### PyPi

[![Latest Version](https://img.shields.io/pypi/v/xgt.svg)](https://pypi.python.org/pypi/xgt)
[![Latest Version](https://img.shields.io/pypi/pyversions/xgt.svg)](https://pypi.python.org/pypi/xgt)
[![License](https://img.shields.io/pypi/l/xgt.svg)](https://pypi.python.org/pypi/xgt)
[![PyPI - Downloads](https://img.shields.io/pypi/dw/xgt.svg)](https://pypi.org/project/xgt/#history)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/xgt.svg)](https://pypi.org/project/xgt/#history)

#### GitHub

[![GitHub stars](https://img.shields.io/github/stars/Rocketgraphai/pyxgt.svg?style=social&label=Stars)](https://github.com/Rocketgraphai/pyxgt)

[Rocketgraph xGT](https://www.rocketgraph.com/) is the fastest Deep Analytics Platform on the market and perfect for your mission-critical applications.
With performance speeds 100's of times that of current market options, you can now empower your data scientist with the best development environment to meet your needs.

## Demos

There are several [demo notebooks](demos/) available within this repo.

## Getting Started

You need to set up a Rocketgraph xGT server on a platform that makes sense for you, and set up a Python environment from which the Rocketgraph xGT client is run.
It is best to set up your client environment first as some Python packages are needed in order to set up some of the server environments.

### Client Setup

The client can run from any Python environment, including Jupyter Notebook and Jupyter Lab.

#### Anaconda

One of the easiest ways to get a Jupyter environment is to install [anaconda](https://anaconda.org/).
Once installed, open an "anaconda prompt" window and run these commands:

```Python
pip install --upgrade grpcio jupyter pandas protobuf xgt
```

If an AWS instance will be used for running the Rocketgraph xGT server, then you should also do this command:

```Python
pip install --upgrade boto3
```

An alternative to the anaconda prompt/command-line method, is to launch a Jupyter Notebook and perform these commands in notebook cells.

#### Command-line on Mac

The first step on a Mac is to ensure that a Python (version 3.10 - 3.14) is installed along with a `pip` package.
If you are using [Homebrew](https://brew.sh) as your package manager, these packages can be installed by doing this command in a `Terminal` window (or your favorite alternative to a `bash` shell):

```bash
$ brew install python3
```

#### Command-line on Linux

The first step on a native Linux platform is to ensure that a Python (version 3.10 - 3.14) is installed.
For those distributions that use RPM and the `yum` package manager:

```bash
$ sudo yum install python3 python3-devel python3-pip
```

On debian-based systems with the `apt` package manager:

```bash
$ sudo apt install python3 python3-dev python3-pip
```

After these O/S packages are installed, the Python packages can be installed:

```bash
$ pip install --upgrade boto3 grpcio jupyter pandas protobuf xgt
```

On a system that manages its Python packages, pip may refuse to install into it.
A virtual environment is the usual answer:

```bash
$ python3 -m venv xgt-env
$ source xgt-env/bin/activate
$ pip install --upgrade boto3 grpcio jupyter pandas protobuf xgt
```

### Server Setup

#### The installer

The quickest way to get a server running is the
[Rocketgraph installer](https://github.com/Rocketgraphai/install), which covers
Windows, macOS and Linux. It brings its own dependencies, including Docker, sets
the containers going and opens
[Mission Control](https://rocketgraph.com/introduction-to-mission-control/) in
your browser when it is done.

On Linux or macOS that is one command:

```bash
$ curl -sSL https://install.rocketgraph.com/install.sh | sh
```

Windows and macOS have graphical installers, listed in that repository.

#### On AWS

1.  Running xGT on your own AWS instances from the [AWS Marketplace](https://aws.amazon.com/marketplace).
    * This process requires subscribing to the [Rocketgraph xGT product](https://aws.amazon.com/marketplace/pp/B09QXZBS55). 
    * All AWS instances with 8 vCPUs or fewer are free for the software; AWS charges for the hardware may apply.
    * See [Instructions for launching on the AWS Marketplace](AWS/Marketplace.md).
1.  An AWS cloud instance running xGT.
    * The instance is run in your own account and is set up using this [cloudformation](AWS/cfxgt.json).
    * Launching requires use of the [boto3](https://pypi.org/project/boto3/) Python package.
    * [Launch AWS EC2](AWS/launchxGT.ipynb)

#### On your own systems

1.  A docker daemon running on your platform (on-premises).
    * Any x86 system running docker can be used.
    * Perform the equivalent of `docker pull rocketgraph/xgt`.
    * More information is available at [rocketgraph/xgt](https://hub.docker.com/r/rocketgraph/xgt).
1.  A docker daemon (docker desktop) running on your laptop.
    * The [docker desktop](https://www.docker.com/get-started) hosting environment can run on:
        - Windows (with WSL2 enabled)
        - Mac Intel Chips
        - Native Linux
