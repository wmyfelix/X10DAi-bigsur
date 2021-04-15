## running macOS on Supermicro X10DAi 
|Support macOS ver.|11.2|
|:-|-|
|Bootloader|OpenCore 0.67 DBG|
|CPU Platform|Haswell-EP(E5v3)

|System Configuraion||notes|
|:-|:-:|:-:|
|CPU|Xeon E5 2695v3 ES x2|XCPM work,but not sure if cpu Scheduling correct|
|Graphics|Radeon Pro Duo Fiji |Mod to add GoP support| 
|BIOS|X10DAi9.C16|Mod to unblock cfg lock and add nvme support|
|Sounds|Creative usb external card|Use soundsource to adjust volume|
|Keyboard|ikbc F87|Update [firmware](https://share.weiyun.com/riG5w1hT) to solve typing problem|
|Disk|WD sn720 x4 |via PCIE|added deviceproperties and set to "bulit-in"|
|Monitor|3840x2160 27' |Connect via DP|
* __issues__ 
  * __Sleep__
  * __Unpredictable window freeze,to fix:__ type`defaults write com.apple.coremedia hardwareVideoDecoder disable`in terminal
  * __Onboard-audio not test but should work__ *//my alc888 is broken*
  * _Some logs uploaded,feel free to contact me._  
*** 
__For v4 cpu user,needs to change some stuffs like fake cpu id,more info: [dortania guide](https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/broadwell-e.html#acpi/)__  

# Hack for belief
![interview](https://github.com/wmyfelix/X10DAi-hackintosh/blob/main/interview.png?raw=true)
