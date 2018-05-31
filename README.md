[![logo](https://github.com/ctuning/ck-guide-images/blob/master/logo-powered-by-ck.png)](https://github.com/ctuning/ck)

This repository contains raw experimental results in [the CK format](https://github.com/ctuning/ck)
for this [image classification workflow](https://github.com/ctuning/ck-request-asplos18-caffe-intel)
from the [ReQuEST tournament at ASPLOS'18](http://cknowledge.org/request-cfp-asplos2018.html) 
on reproducible SW/HW co-design of deep learning (speed, accuracy, energy, costs).
You can see at least some of them in the [live ReQuEST scoreboard](http://cKnowledge.org/request-results).

## Installation

### Minimal CK installation

The minimal installation requires:

* Python 2.7 or 3.3+ (limitation is mainly due to unitests)
* Git command line client.

You can install CK in your local user space as follows:

```
$ git clone http://github.com/ctuning/ck
$ export PATH=$PWD/ck/bin:$PATH
$ export PYTHONPATH=$PWD/ck:$PYTHONPATH
```

You can also install CK via PIP with sudo to avoid setting up environment variables yourself:

```
$ sudo pip install ck
```

### Install this CK repository and dependencies

```
$ ck pull repo:ck-request-asplos18-results-caffe-intel
```

### List available experiments
```
$ ck ls ck-request-asplos18-results-caffe-intel:experiment:*
```

### Replay experiment

```
$ ck replay experiment:{name from above list}
```

Note that CK will try to automatically rebuild experimental setup 
by detecting already installed software dependencies and installing missing ones
using shared [CK packages](https://github.com/ctuning/ck/wiki/Shared-packages).

If you want to have a software setup as close to the original one 
as possible, install packages before running replay as described in 
[the ReadMe](https://github.com/ctuning/ck-request-asplos18-caffe-intel)
of the related CK workflow.

### Start dashboard to visualize/compare results

```
$ ck dashboard request.asplos18 --results=ck-request-asplos18-results-caffe-intel
```

### View results in the live scoreboard

[Link](http://cKnowledge.org/request-results)

