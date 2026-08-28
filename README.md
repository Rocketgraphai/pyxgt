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

## Getting Started

Two pieces: a Rocketgraph server, and the Python client you talk to it with.

### Install Rocketgraph

The [Rocketgraph installer](https://github.com/Rocketgraphai/install) covers
Windows, macOS and Linux. It brings its own dependencies, including Docker,
starts the containers and opens
[Mission Control](https://rocketgraph.com/introduction-to-mission-control/) in
your browser when it finishes.

On Linux or macOS that is one command:

```bash
$ curl -sSL https://install.rocketgraph.com/install.sh | sh
```

Windows and macOS also have graphical installers, listed in that repository.

### Install the client

The client runs from any Python 3.10 to 3.14 environment, including Jupyter
Notebook and Jupyter Lab:

```bash
$ pip install --upgrade grpcio jupyter pandas protobuf xgt
```

If you need a Python first, [anaconda](https://anaconda.org/) brings one along
with Jupyter. Otherwise `brew install python3` on macOS, `sudo apt install
python3 python3-dev python3-pip` on debian-based systems, or `sudo yum install
python3 python3-devel python3-pip` where `yum` is the package manager.

On a system that manages its own Python packages, pip may refuse to install into
it. A virtual environment is the usual answer:

```bash
$ python3 -m venv xgt-env
$ source xgt-env/bin/activate
$ pip install --upgrade grpcio jupyter pandas protobuf xgt
```

## Demos

There are several [demo notebooks](demos/) available within this repo.

## Other ways to run a server

The installer above is the shortest path. These remain for the cases it does not
cover.

### On AWS

1.  Running xGT on your own AWS instances from the [AWS Marketplace](https://aws.amazon.com/marketplace).
    * This process requires subscribing to the [Rocketgraph xGT product](https://aws.amazon.com/marketplace/pp/B09QXZBS55). 
    * All AWS instances with 8 vCPUs or fewer are free for the software; AWS charges for the hardware may apply.
    * See [Instructions for launching on the AWS Marketplace](AWS/Marketplace.md).

### On your own systems

1.  A docker daemon running on your platform (on-premises).
    * Any x86 system running docker can be used.
    * Perform the equivalent of `docker pull rocketgraph/xgt`.
    * More information is available at [rocketgraph/xgt](https://hub.docker.com/r/rocketgraph/xgt).
1.  A docker daemon (docker desktop) running on your laptop.
    * The [docker desktop](https://www.docker.com/get-started) hosting environment can run on:
        - Windows (with WSL2 enabled)
        - Mac Intel Chips
        - Native Linux
