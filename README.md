# oscillo-monitor
Monitoring an oscilloscope display using VISA API


## Installation

```shell
git clone https://github.com/mao-wfs/oscillo-monitor.git
cd oscillo-monitor
poetry install
```

## Usage

1. Get the resource name of an oscilloscope
    ```shell
    $ poetry run bin/resources
    USB0::...::INSTR
    ...
    ```
1. Run the monitor script with the resource name
    ```shell
    $ VISA_RESOURCE="USB0::...::INSTR" poetry run bin/monitor
    ```

## Troubleshoot

If you cannot find any resource names, please check this out. 

> On Unix system, one may have to modify udev rules to allow non-root access to the device you are trying to connect to. The following tutorial describes how to do it http://ask.xmodulo.com/change-usb-device-permission-linux.html.
> https://pyvisa.readthedocs.io/projects/pyvisa-py/en/stable/installation.html