Float
=====

A floating Interactive Help client.


Introduction
------------

Float is a "Floating Interactive Help" application for RISC OS. It is intended to replace Acorn's Help application, providing interactive help in small "floating" panes that follow the mouse around the screen. This is similar to some of the systems available on other platforms.

Float will work with any application that supports Acorn's interactive help protocol, that is any application that works with Help.

Some of the "nice" features of Float are:

* Configurable pane appearance: font, colours and shadow can be user set
* Supports help on window tools
* Can ignore help from selected applications (such as Filer, Pinboard, etc)
* Supports full iconbar help
* Ability to quickly toggle panes on and off
* Full support of Help dictionary


Building
--------

Float consists of a collection of un-tokenised BASIC, which must be assembled using the [SFTools build environment](https://github.com/steve-fryatt). It will be necessary to have suitable Linux system with a working installation of the [GCCSDK](http://www.riscos.info/index.php/GCCSDK) to be able to make use of this.

With a suitable build environment set up, making Float is a matter of running

	make

from the root folder of the project. This will build everything from source, and assemble a working !Float application and its associated files within the build folder. If you have access to this folder from RISC OS (either via HostFS, LanManFS, NFS, Sunfish or similar), it will be possible to run it directly once built.

To clean out all of the build files, use

	make clean

To make a release version and package it into Zip files for distribution, use

	make release

This will clean the project and re-build it all, then create a distribution archive (no source), source archive and RiscPkg package in the folder within which the project folder is located. By default the output of `git describe` is used to version the build, but a specific version can be applied by setting the `VERSION` variable -- for example

	make release VERSION=1.23


Licence
-------

Float is licensed under the EUPL, Version 1.2 only (the "Licence"); you may not use this work except in compliance with the Licence.

You may obtain a copy of the Licence at <http://joinup.ec.europa.eu/software/page/eupl>.

Unless required by applicable law or agreed to in writing, software distributed under the Licence is distributed on an "**as is**"; basis, **without warranties or conditions of any kind**, either express or implied.

See the Licence for the specific language governing permissions and limitations under the Licence.