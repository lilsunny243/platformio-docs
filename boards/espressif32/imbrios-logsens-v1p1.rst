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

.. _board_espressif32_imbrios-logsens-v1p1:

Imbrios LogSens V1P1
====================

.. contents::

Hardware
--------

Platform :ref:`platform_espressif32`: ESP32 is a series of low-cost, low-power system on a chip microcontrollers with integrated Wi-Fi and Bluetooth. ESP32 integrates an antenna switch, RF balun, power amplifier, low-noise receive amplifier, filters, and power management modules.

.. list-table::

  * - **Microcontroller**
    - ESP32
  * - **Frequency**
    - 240MHz
  * - **Flash**
    - 4MB
  * - **RAM**
    - 320KB
  * - **Vendor**
    - `Imbrios <https://www.imbrios.com/products/logsens?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``imbrios-logsens-v1p1`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:imbrios-logsens-v1p1]
  platform = espressif32
  board = imbrios-logsens-v1p1

You can override default Imbrios LogSens V1P1 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `imbrios-logsens-v1p1.json <https://github.com/platformio/platform-espressif32/blob/master/boards/imbrios-logsens-v1p1.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:imbrios-logsens-v1p1]
  platform = espressif32
  board = imbrios-logsens-v1p1

  ; change microcontroller
  board_build.mcu = esp32

  ; change MCU frequency
  board_build.f_cpu = 240000000L


Uploading
---------
Imbrios LogSens V1P1 supports the following uploading protocols:

* ``espota``
* ``esptool``

Default protocol is ``esptool``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:imbrios-logsens-v1p1]
  platform = espressif32
  board = imbrios-logsens-v1p1

  upload_protocol = esptool

Debugging
---------
:ref:`piodebug` currently does not support Imbrios LogSens V1P1 board.

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_arduino`
      - Arduino Wiring-based Framework allows writing cross-platform software to control devices attached to a wide range of Arduino boards to create all kinds of creative coding, interactive objects, spaces or physical experiences

    * - :ref:`framework_espidf`
      - ESP-IDF is the official development framework for the ESP32 and ESP32-S Series SoCs.