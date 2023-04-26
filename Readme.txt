;installation:
;=============
;-------------------------------------------------------------------
;  mkdir gitclone-rockchip,
;  git clone https://github.com/Lorenzo1205/rkdeveloptool.git
;-------------------------------------------------------------------
;1  >sudo apt-get install libudev-dev libusb-1.0-0-dev dh-autoreconf
;    > sudo apt-get install pkg-config libusb-1.0 
;2 go into root of rkdeveloptool
;3 aclocal
;4.autoreconf -i
;5.autoheader
;5.automake --add-missing
;4 ./configure
;5 make
;6 sudo cp rkdeveloptool /usr/local/bin/
;7 sudo ldconfig
;8 test version using > rkdeveloptool -v
;outcome should be [ rkdeveloptool ver 1.32 ]
;if outcome is correct, you have working rkdeveltool version 1.32
;
;---------------------------------------------------------------------
;info
;===============
;rkdeveloptool usage,input "rkdeveloptool -h" to see
;
;example:
;1.download kernel.img
;sudo ./rkdeveloptool db RKXXLoader.bin    //download usbplug to device
;sudo ./rkdeveloptool wl 0x8000 kernel.img //0x8000 is base of kernel partition,unit is sector.
;sudo ./rkdeveloptool rd                   //reset device
;
;compile error fixed.
;check and if not edit main.cpp :
;*******************************
; line 1491 in main.cpp 
; from:
; char buffer[5];
; to
; char buffer[558]; 
************************************
;
;### GREEETZZ Lorenzo1205 ####
