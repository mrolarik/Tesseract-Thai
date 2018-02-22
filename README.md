# Tesseract-Thai
Tesseract-ocr for Thai language

## Thai Text Image  

![Thai text image](https://github.com/mrolarik/Tesseract-Thai/blob/master/data-text-img/thai-text.png)

## Thai Text 

[ปั้นบบุฒ่สุดปธะเสธีฐิเลิศคุณค่า  
กฮ่าปรอีดาฟู0ส้ดว๋เดธับิฉาบ  
ออน่ำกันทัฒนคุอิชากาธ  
อย่าลี้าป๋ผถิาญฤๆเย่นยำบิทาไคธ  
ไม่ทีอโทษโกรธเเซ่น๊ซัดอึดอัดด่า  
หัด๏กัยเหมือนกิทำอัปั๊ณาสี้ย  
ปฏิฌิปธะพฤดิกฏกําหนดไบิ  
พูดจาไหัอัะ ๆ อ่า ๆ ปาฟั0[อยฯ  
]

## Install Tesseract
$ sudo apt-get install libpng-dev libjpeg-dev libtiff-dev zlib1g-dev  
$ sudo apt-get install gcc g++  
$ sudo apt-get install autoconf automake libtool checkinstall  

### Need image processing toolkit Leptonica to build Tesseract.
$ cd ~
$ wget http://www.leptonica.org/source/leptonica-1.73.tar.gz
$ tar -zxvf leptonica-1.73.tar.gz
$ cd leptonica-1.73 
$ ./configure
$ make
$ sudo checkinstall
$ sudo ldconfig

$ sudo apt-get install tesseract-ocr  

## tesseract usage
$ tesseract --help  
Usage:  
  tesseract --help | --help-psm | --version  
  tesseract --list-langs [--tessdata-dir PATH]  
  tesseract --print-parameters [options...] [configfile...]  
  tesseract imagename|stdin outputbase|stdout [options...] [configfile...]  
  
OCR options:  
  --tessdata-dir PATH   Specify the location of tessdata path.  
  --user-words PATH     Specify the location of user words file.  
  --user-patterns PATH  Specify the location of user patterns file.  
  -l LANG[+LANG]        Specify language(s) used for OCR.  
  -c VAR=VALUE          Set value for config variables.  
                        Multiple -c arguments are allowed.  
  -psm NUM              Specify page segmentation mode.  
NOTE: These options must occur before any configfile.  
  
Page segmentation modes:  
  0    Orientation and script detection (OSD) only.  
  1    Automatic page segmentation with OSD.  
  2    Automatic page segmentation, but no OSD, or OCR.  
  3    Fully automatic page segmentation, but no OSD. (Default)  
  4    Assume a single column of text of variable sizes.  
  5    Assume a single uniform block of vertically aligned text.  
  6    Assume a single uniform block of text.  
  7    Treat the image as a single text line.  
  8    Treat the image as a single word.  
  9    Treat the image as a single word in a circle.  
 10    Treat the image as a single character.  
  
Single options:  
  -h, --help            Show this help message.  
  --help-psm            Show page segmentation modes.  
  -v, --version         Show version information.  
  --list-langs          List available languages for tesseract engine.  
  --print-parameters    Print tesseract parameters to stdout.  
