..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _platform_lattice_ice40:

Lattice iCE40
=============

:Registry:
  `https://registry.platformio.org/platforms/platformio/lattice_ice40 <https://registry.platformio.org/platforms/platformio/lattice_ice40>`__
:Configuration:
  :ref:`projectconf_env_platform` = ``lattice_ice40``

The iCE40 family of ultra-low power, non-volatile FPGAs has five devices with densities ranging from 384 to 7680 Look-Up Tables (LUTs). In addition to LUT-based,low-cost programmable logic, these devices feature Embedded Block RAM (EBR), Non-volatile Configuration Memory (NVCM) and Phase Locked Loops (PLLs). These features allow the devices to be used in low-cost, high-volume consumer and system applications.

For more detailed information please visit `vendor site <http://www.latticesemi.com/Products/FPGAandCPLD/iCE40.aspx?utm_source=platformio.org&utm_medium=docs>`_.

.. contents:: Contents
    :local:
    :depth: 1


Examples
--------

Examples are listed from `Lattice iCE40 development platform repository <https://github.com/platformio/platform-lattice_ice40/tree/master/examples?utm_source=platformio.org&utm_medium=docs>`_:

* `leds <https://github.com/platformio/platform-lattice_ice40/tree/master/examples/leds?utm_source=platformio.org&utm_medium=docs>`_
* `counter <https://github.com/platformio/platform-lattice_ice40/tree/master/examples/counter?utm_source=platformio.org&utm_medium=docs>`_

Stable and upstream versions
----------------------------

You can switch between `stable releases <https://github.com/platformio/platform-lattice_ice40/releases>`__
of Lattice iCE40 development platform and the latest upstream version using
:ref:`projectconf_env_platform` option in :ref:`projectconf` as described below.

Stable
~~~~~~

.. code-block:: ini

    ; Latest stable version, NOT recommended
    ; Pin the version as shown below
    [env:latest_stable]
    platform = lattice_ice40
    board = ...

    ; Specific version
    [env:custom_stable]
    platform = lattice_ice40@x.y.z
    board = ...

Upstream
~~~~~~~~

.. code-block:: ini

    [env:upstream_develop]
    platform = https://github.com/platformio/platform-lattice_ice40.git
    board = ...


Packages
--------

.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - `toolchain-icestorm <https://registry.platformio.org/tools/platformio/toolchain-icestorm>`__
      - Tools for analyzing and creating bitstream files for FPGA IceStorm

    * - `toolchain-iverilog <https://registry.platformio.org/tools/platformio/toolchain-iverilog>`__
      - Verilog simulation and synthesis tool

.. warning::
    **Linux Users**:

        * Install "udev" rules :ref:`platformio_udev_rules`
        * Raspberry Pi users, please read this article
          `Enable serial port on Raspberry Pi <https://hallard.me/enable-serial-port-on-raspberry-pi/>`__.


    **Windows Users:**

        Please check that you have a correctly installed USB driver from board
        manufacturer


Boards
------

.. note::
    * You can list pre-configured boards by :ref:`cmd_boards` command
    * For more detailed ``board`` information please scroll the tables below by
      horizontally.

FPGAwars
~~~~~~~~

.. list-table::
    :header-rows:  1

    * - Name
      - Debug
      - MCU
      - Frequency
      - Flash
      - RAM
    * - :ref:`board_lattice_ice40_icezum`
      - No
      - ICE40-HX1K-TQ144
      - 12MHz
      - 32KB
      - 32KB

Lattice
~~~~~~~

.. list-table::
    :header-rows:  1

    * - Name
      - Debug
      - MCU
      - Frequency
      - Flash
      - RAM
    * - :ref:`board_lattice_ice40_icestick`
      - No
      - ICE40-HX1K-TQ144
      - 12MHz
      - 32KB
      - 32KB
