PF is an Arduino Library wrapper for Petit FatFs:

http://elm-chan.org/fsw/ff/00index_p.html


Edit pffArduino.h to set the SD chip select pin and select
an SPI SCK divisor of 2 or 4.

Edit pffconfig.h to select options.  The default is to select
most options.  You can save flash by limiting options.

The PetitFS.ino example uses 5,806 bytes with the default options.

PetitFS.ino uses 4,940 bytes if only _USE_READ and _FS_FAT32 are
selected.

Create TEST.TXT in the root directory of an SD. and run the
PetitFS.ino example.

<h1>Functions</h1>

FRESULT PF.begin(&FATFS);
________________________________________________
FRESULT PF.open(const char* filename); <b>//it must be an upper case value</b>
________________________________________________
FRESULT PF.readFile(uint8_t buffer[], const int size, &unsigned int wrote);
_________________________________________________
PF.writeFile();
_________________________________________________
PF.openDirectory();
_________________________________________________
PF.readDirectory();
_________________________________________________

