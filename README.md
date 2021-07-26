About airspy
============

Home: https://github.com/airspy/airspyone_host

Package license: BSD-3-Clause AND MIT AND GPL-2.0-or-later AND LGPL-2.1-or-later

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/airspy-feedstock/blob/master/LICENSE.txt)

Summary: Host software for AirSpy, a low cost, open source software radio platform

Development: https://github.com/airspy/airspyone_host

Airspy is a line of Popular Software-Defined Radio (SDR) receivers
developed to achieve High Performance and Affordable Price using innovative
combinations of DSP and RF techniques. The goal is to satisfy the most
demanding telecommunications professionals and radio enthusiasts while
being a serious alternative to both cost sensitive and higher end
receivers. Airspy Radios feature world class reception quality and ease of
use thanks to the tight integration with the de facto standard free SDR#
software for signal acquisition, analysis and demodulation.

The `libairspy` package contains the library for Airspy devices, and the
`airspy` package contains command line tools for using the devices.

For Linux users of `airspy`, you will likely want to link the provided
udev rule into your system installation in order for the hardware to have
the correct permissions:

    sudo ln -s $CONDA_PREFIX/lib/udev/rules.d/52-airspy.rules /etc/udev/rules.d/
    sudo udevadm control --reload
    sudo udevadm trigger

Then, make sure your user account belongs to the plugdev group in order to
be able to access your device:

    sudo usermod -a -G plugdev <user>

You may have to restart for this change to take effect.


Current build status
====================


<table><tr>
    <td>Travis</td>
    <td>
      <a href="https://travis-ci.com/conda-forge/airspy-feedstock">
        <img alt="macOS" src="https://img.shields.io/travis/com/conda-forge/airspy-feedstock/master.svg?label=macOS">
      </a>
    </td>
  </tr><tr>
    <td>Drone</td>
    <td>
      <a href="https://cloud.drone.io/conda-forge/airspy-feedstock">
        <img alt="linux" src="https://img.shields.io/drone/build/conda-forge/airspy-feedstock/master.svg?label=Linux">
      </a>
    </td>
  </tr>
    
  <tr>
    <td>Azure</td>
    <td>
      <details>
        <summary>
          <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
            <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master">
          </a>
        </summary>
        <table>
          <thead><tr><th>Variant</th><th>Status</th></tr></thead>
          <tbody><tr>
              <td>linux_64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=linux&configuration=linux_64_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>linux_aarch64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=linux&configuration=linux_aarch64_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>linux_ppc64le</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=linux&configuration=linux_ppc64le_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>osx_64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=osx&configuration=osx_64_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>osx_arm64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=osx&configuration=osx_arm64_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>win_64</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=13511&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/airspy-feedstock?branchName=master&jobName=win&configuration=win_64_" alt="variant">
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </details>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-airspy-green.svg)](https://anaconda.org/conda-forge/airspy) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/airspy.svg)](https://anaconda.org/conda-forge/airspy) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/airspy.svg)](https://anaconda.org/conda-forge/airspy) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/airspy.svg)](https://anaconda.org/conda-forge/airspy) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-libairspy-green.svg)](https://anaconda.org/conda-forge/libairspy) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/libairspy.svg)](https://anaconda.org/conda-forge/libairspy) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/libairspy.svg)](https://anaconda.org/conda-forge/libairspy) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/libairspy.svg)](https://anaconda.org/conda-forge/libairspy) |

Installing airspy
=================

Installing `airspy` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `airspy, libairspy` can be installed with:

```
conda install airspy libairspy
```

It is possible to list all of the versions of `airspy` available on your platform with:

```
conda search airspy --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.com/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating airspy-feedstock
=========================

If you would like to improve the airspy recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/airspy-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@ryanvolz](https://github.com/ryanvolz/)

