# SCSI2SD-S3000XL

Here is the configuration file that was the result of a successful installation of a [codesrc SCSI2SD](http://www.codesrc.com/mediawiki/index.php?title=SCSI2SD) board in my Akai S3000XL sampler. It's set to work with SD cards 2GB and larger (though due to limitations within the S3000XL only 2GB will be useable). Hopefully it may be of use to other adopters of this cool storage method.

## Installation

Use codesrc's [scsi2sd-util](http://www.codesrc.com/mediawiki/index.php?title=SCSI2SD_UserManual#Changing_Configuration) to load this configuration file onto your SCSI2SD board via USB.

## Usage

Once the configuration file is loaded onto the SCSI2SD board disconnect from the computer, connect up your 5V power supply and you should be ready to roll (assuming hardware installation is complete).

This configuration file assumes you are running default SCSI settings on your S3000XL (HD SCSI ID 5; sector size 512kb). By using this configuration file the card will be segmented into four 510MB 'disks', with SCSI IDs descending from 5 to 2. The S3000XL can only address one hard drive at once though, so to jump between the disks you must go to the sampler's SCSI settings (in Load or Save Modes) and set the SCSI ID to the desired value.

All disks are set to run as SCSI-2, with all other options deselected. The scsi2sd-util tool can be used to adjust the settings if needed. __Note:__ hot-swapping of SD cards has not been enabled in this configuration, and I don't know if the S3000XL supports such a feature.

When up and running, head to the S3000XL's Save Mode and select "FORM" (F6) to format your disks; each must be partitioned as there is a maximum limit of 60MB per partition on the S3000XL. Refer to the S3000XL Operations Manual for instructions on this procedure.