# VACUUM firmware builder

This is a rewritten version of imagebuilder(https://github.com/dgiese/dustcloud).

Added the ability to run custom scripts (plugins).

Added functionality through custom scripts.

### For more information run:
./builder_vacuum.sh --run-custom-script=ALL --help

<details><summary>CLICK ME</summary>
<p>


```
Usage: sudo ./builder_vacuum.sh --firmware=v11_003194.pkg [--unpack-and-mount|--run-custom-script=SCRIPT|--help]

Custom parameters for './custom-script/custom_adbd.sh':
[--replace-adbd]

Custom parameters for './custom-script/custom_appproxy_patcher.sh':
[--enable-appproxy-patcher]

Custom parameters for './custom-script/custom_bin_addon.sh':
[--enable-addon]

Custom parameters for './custom-script/custom_bin_addon_sox.sh':
[--enable-addon-sox]

Custom parameters for './custom-script/custom_binding.sh':
[--enable-binding]

Custom parameters for './custom-script/custom_dns.sh':
[--dnsserver=ADDRESS]

Custom parameters for './custom-script/custom_dummycloud.sh':
[--dummycloud-path=PATH]

Custom parameters for './custom-script/custom_enable_local_ota.sh':
[--enable-local-ota]

Custom parameters for './custom-script/custom_example1.sh':
[--example1 --param1=PARAM]

Custom parameters for './custom-script/custom_example2.sh':
[--example2 --param2=PARAM]

Custom parameters for './custom-script/custom_fixreset.sh':
[--fix-reset]

Custom parameters for './custom-script/custom_greeting.sh':
[--enable-greeting]

Custom parameters for './custom-script/custom_history.sh':
[--enable-history]

Custom parameters for './custom-script/custom_hostname.sh':
[--hostname=roborock]

Custom parameters for './custom-script/custom_multisound.sh':
[--enable-multisound]

Custom parameters for './custom-script/custom_ntp.sh':
[--ntpserver=ADDRESS]

Custom parameters for './custom-script/custom_off_cn_ny.sh':
[--enable-turn-off-ny]

Custom parameters for './custom-script/custom_off_logs.sh':
[--disable-logs]

Custom parameters for './custom-script/custom_off_updates.sh':
[--disable-firmware-updates]

Custom parameters for './custom-script/custom_ramdisk.sh':
[--enable-ramdisk]

Custom parameters for './custom-script/custom_random_phrases.sh':
[--enable-random-phrases]

Custom parameters for './custom-script/custom_replace_miio.sh':
[--replace-miio]

Custom parameters for './custom-script/custom_rrlogd_patcher.sh':
[--enable-rrlogd-patcher]

Custom parameters for './custom-script/custom_sound.sh':
[--soundfile=english.pkg]

Custom parameters for './custom-script/custom_add_ssh_keys.sh':
[--public-key=id_rsa.pub]

Custom parameters for './custom-script/custom_timezone.sh':
[--timezone=Europe/Berlin]

Custom parameters for './custom-script/custom_unprovisioned.sh':
[--unprovisioned|--ssid YOUR_SSID|--psk YOUR_WIRELESS_PASSWORD]

Custom parameters for './custom-script/custom_vacuum.sh':
[--root-password=PASSWORD|--custom-user=USER|--custom-user-pass=PASSWORD|
--convert2prc|--convert2eu]

Custom parameters for './custom-script/custom_valetudo.sh':
[--valetudo-path=PATH]

Custom parameters for './custom-script/custom_valetudo_re.sh':
[--valetudo-re-path=PATH]
[--valetudo-re-nodeps]

Custom parameters for './custom-script/custom_valetudo_wo_dummycloud.sh':
[--valetudo-path-wod=PATH]

Custom parameters for './custom-script/custom_dns_catcher.sh':
[--enable-dns-catcher]

Options:
  -h, --help                 Prints this message
  -f, --firmware=PATH        Path to firmware file
  --unpack-and-mount         Only unpack and mount image
  --run-custom-script=SCRIPT Run custom script (if 'ALL' run all scripts from custom-script)

Each parameter that takes a file as an argument accepts path in any form

Report bugs to: https://github.com/zvldz/vacuum/issues
Original Author: Dennis Giese [dgiese@dontvacuum.me], https://github.com/dgiese/dustcloud

Custom options for './custom-script/custom_adbd.sh':
  --replace-adbd             Replace xiaomis custom adbd with generic adbd version

Custom options for './custom-script/custom_appproxy_patcher.sh':
  --enable-appproxy-patcher  AppProxy patch to disable timezone checking

Custom options for './custom-script/custom_bin_addon.sh':
  --enable-addon             Extract addon.tgz to firmware

Custom options for './custom-script/custom_bin_addon_sox.sh':
  --enable-addon-sox         Extract sox.tgz to firmware (SoX console audio player)

Custom options for './custom-script/custom_binding.sh':
  --enable-binding           Adding keybinding for bash

Custom options for './custom-script/custom_dns.sh':
  --dnsserver=ADDRESS        Set your DNS server (ex: "8.8.8.8, 1.1.1.1")

Custom options for './custom-script/custom_dummycloud.sh':
  --dummycloud-path=PATH     Provide the path to dummycloud

Custom options for './custom-script/custom_enable_local_ota.sh':
  --enable-local-ota         Enable local ota on 2008+ firmware

Custom options for './custom-script/custom_example1.sh':
  --example1                 Example1
  --param1=PARAM             Param1

Custom options for './custom-script/custom_example2.sh':
  --example2                 Example2
  --param2=PARAM             Param2

Custom options for './custom-script/custom_fixreset.sh':
  --fix-reset                Apply firmware reset fix

Custom options for './custom-script/custom_greeting.sh':
  --enable-greeting          Add greeting to ssh

Custom options for './custom-script/custom_history.sh':
  --enable-history           Add buildnumber and firmware version to history file

Custom options for './custom-script/custom_hostname.sh':
  --hostname=HOSTNAME        Sets a custom hostname

Custom options for './custom-script/custom_multisound.sh':
  --enable-multisound        Make robot use different sounds at the same event

Custom options for './custom-script/custom_ntp.sh':
  --ntpserver=ADDRESS        Set your local NTP server

Custom options for './custom-script/custom_off_cn_ny.sh':
  --enable-turn-off-ny       Turn off Chinese New Year

Custom options for './custom-script/custom_off_logs.sh':
  --disable-logs             Disables most log files creations and log uploads on the vacuum

Custom options for './custom-script/custom_off_updates.sh':
  --disable-firmware-updates Disable xiaomi servers using hosts file for firmware updates

Custom options for './custom-script/custom_ramdisk.sh':
  --enable-ramdisk           Put rrlog directory to RAM-disk to prevent wearing out FLASH memory

Custom options for './custom-script/custom_random_phrases.sh':
  --enable-random-phrases    Adding random phrases when cleaning

Custom options for './custom-script/custom_replace_miio.sh':
  --replace-miio             Replaces miio to version 3.3.9

Custom options for './custom-script/custom_rrlogd_patcher.sh':
  --enable-rrlogd-patcher    Patch rrlogd to disable log encryption (only use with dummycloud or dustcloud)

Custom options for './custom-script/custom_sound.sh':
  -s, --soundfile=PATH       Path to sound file

Custom options for './custom-script/custom_add_ssh_keys.sh':
  -k, --public-key=PATH      Path to ssh public key to be added to authorized_keys file
                             if need to add multiple keys set -k as many times as you need:
                             -k ./local_key.pub -k ~/.ssh/id_rsa.pub -k /root/ssh/id_rsa.pub

Custom options for './custom-script/custom_timezone.sh':
  -t, --timezone             Timezone to be used in vacuum

Custom options for './custom-script/custom_unprovisioned.sh':
  --unprovisioned            Access your network in unprovisioned mode (currently only wpa2psk is supported)
                             --unprovisioned wpa2psk
                             --ssid YOUR_SSID
                             --psk YOUR_WIRELESS_PASSWORD

Custom options for './custom-script/custom_vacuum.sh':
  --root-pass=PASSWORD         Set password for root and custom user
  --custom-user=USER           Add custom user
  --custom-user-pass=PASSWORD  Set password for custom user
  --convert2prc                Convert to Mainland China region
  --convert2eu                 Convert to EU region

Custom options for './custom-script/custom_valetudo.sh':
  --valetudo-path=PATH       The path to Valetudo(https://github.com/Hypfer/Valetudo) to include it into the image

Custom options for './custom-script/custom_valetudo_re.sh':
  --valetudo-re-path=PATH    The path to Valetudo RE(https://github.com/rand256/valetudo) to include it into the image
  --valetudo-re-nodeps       Do not add libstd++ dependencies if using binary built with partial static linking

Custom options for './custom-script/custom_valetudo_wo_dummycloud.sh':
  --valetudo-path-wod=PATH   The path to valetudo(without dummycloud) to include it into the image

Custom options for './custom-script/custom_dns_catcher.sh':
  --enable-dns-catcher       Redirect and spoof outgoing dns requests(for xiaomi servers)
```

</p>
</details>

### Major changes
[Link](https://raw.githubusercontent.com/zvldz/vacuum/master/changes.txt)

### History of stock firmware
[Link](http://htmlpreview.github.io/?https://raw.githubusercontent.com/zvldz/vacuum/master/history.html)

### Already builded firmwares
[GEN1](https://vacuumz.info/download/gen1/)

[GEN2](https://vacuumz.info/download/gen2/)

### Thanks
* **https://github.com/dgiese/dustcloud**
* https://github.com/JohnRev
* _https://github.com/Hypfer/Valetudo_
* https://github.com/rand256/valetudo
* https://github.com/LazyT/rrcc
