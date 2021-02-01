# Qualcomm-BYPASS-2021-for-test
for test will repper some code for this Projects
this script not full to now 
this script need some edite 
by Chernobylll


connecting https://www.facebook.com/Chernobyllll


Installation

Get python >= 3.7 64-Bit


For UFS Flash
./edl.py printgpt --memory=ufs --lun=0 -> to print gpt on lun 0
./edl.py printgpt --memory=ufs -> to print gpt of all lun
./edl.py rf lun0.bin --memory=ufs --lun=0 -> to dump whole lun 0
./edl.py rf flash.bin --memory=ufs -> to dump all luns as lun0_flash.bin, lun1_flash.bin, ...
./edl.py rl dumps --memory=ufs --lun=0 --skip=userdata,vendor_a -> to dump all partitions from lun0 to directory dumps for device with ufs and skip userdata and vendor_a partition
./edl.py rl dumps --memory=ufs --genxml -> to dump all partitions from all lun to directory dumps and write rawprogram[lun].xml
./edl.py rs 0 15 data.bin --memory=ufs --lun=0 -> to dump 15 sectors from starting sector 0 from lun 0 to file data.bin
./edl.py r boot_a boot.img --memory=ufs --lun=4 -> to dump the partition "boot_a" from lun 4 to the filename boot.img
./edl.py r boot_a boot.img --memory=ufs -> to dump the partition "boot_a" to the filename boot.img using lun autodetection
./edl.py r boot_a,boot_b boot_a.img,boot_b.img --memory=ufs -> to dump multiple partitions to multiple filenames
./edl.py footer footer.bin --memory=ufs -> to dump the crypto footer
./edl.py w boot boot.img --memory=ufs --lun=4 -> to write boot.img to the "boot" partition on lun 4 on the device with ufs flash
./edl.py w gpt gpt.img --memory=ufs --lun=4 -> to write gpt partition table from gpt.img to the lun 4 on the device with ufs flash
./edl.py wl dumps --memory=ufs --lun=0 -> to write all files from "dumps" folder to according partitions to flash lun 0
./edl.py wl dumps --memory=ufs -> to write all files from "dumps" folder to according partitions to flash and try to autodetect lun
./edl.py wf dump.bin --memory=ufs --lun=0 -> to write the rawimage dump.bin to flash lun 0
./edl.py e misc --memory=ufs --lun=0 -> to erase the partition misc on lun 0
./edl.py gpt . --genxml --memory=ufs -> dump gpt_main[lun].bin/gpt_backup[lun].bin and write rawpartition[lun].xml to current directory (".")

