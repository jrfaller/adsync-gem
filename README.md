# AdSync

An Android Directory Synchronizer

## Configuration

To use AdSync, you need to have unlocked developer options, enabled USB debugging and trusted the computer where AdSync will run.

AdSync needs a config file located in `$HOME/.adsync` and also the Android SDK tools installed and available in the path (most importantly `adb`). The YAML config file look like this:

```
DEVICE_ID_1:
  BACKUP_NAME_1:
    - PATH/TO/DEVICE/FOLDER
    - PATH/TO/BACKUP/FOLDER
  BACKUP_NAME_2:
    - PATH/TO/DEVICE/FOLDER
    - PATH/TO/BACKUP/FOLDER
DEVICE_ID_2:
  BACKUP_NAME_3:
    - PATH/TO/DEVICE/FOLDER
    - PATH/TO/BACKUP/FOLDER
```

A backup configuration is given for each device. It consists of a dictionnary having device id for keys. For each key, the corresponding value is a dictionnary of named backups where the key is a unique name and the value is a pair of source folder on the device and backup folder on the computer.

## Usage

* `adsync status`: displays the current status (configuration, connected device, folder requiring synchronization)
* `adsync version`: displays adsync's version
* `adsync sync`: starts synchronization for the currently connected device (use the `-- confirm` flag to actually synchronize and `--verbose` to have the details of the file to be synchronized)
* `adsync doctor`: check your adsync installation 
