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
```
$ sudo apt-get install libpng-dev libjpeg-dev libtiff-dev zlib1g-dev  
$ sudo apt-get install gcc g++  
$ sudo apt-get install autoconf automake libtool checkinstall  
```

### Need image processing toolkit Leptonica to build Tesseract.  
```
$ cd ~  
$ wget http://www.leptonica.org/source/leptonica-1.73.tar.gz  
$ tar -zxvf leptonica-1.73.tar.gz  
$ cd leptonica-1.73  
$ ./configure  
$ make  
$ sudo checkinstall  
$ sudo ldconfig  

$ sudo apt-get install tesseract-ocr  
```

## tesseract usage  
```
$ tesseract --help  
```

## List available languages for tesseract engine  
```
$ sudo tesseract --list-langs List of available languages (3):  
osd  
eng  
equ   
```

## Install Thai package
```
$ sudo apt-get install tesseract-ocr-tha 

$ sudo tesseract --list-langs List of available languages (4):  
tha  
osd  
eng  
equ   
```

## Using Python and Tesserect
```
$ sudo pip install pytesseract
```

### Python program
```
from PIL import Image
import pytesseract

img_path = 'data-test-img/text-img.png'
txtImg = Image.open(img_path)
text = pytesseract.image_to_string(txtImg)

print text
```

## Outline
- [Tesseract ocr](https://github.com/mrolarik/Tesseract-Thai/blob/master/tesseract-ocr.ipynb)  
- [Tesseract English Language](https://github.com/mrolarik/Tesseract-Thai/blob/master/tesseract-ocr-English-language.ipynb)  
- [Tesseract Thai Language](https://github.com/mrolarik/Tesseract-Thai/blob/master/tesseract-ocr-Thai-language.ipynb)  
- [Tesseract Other Languages](https://github.com/mrolarik/Tesseract-Thai/blob/master/tesseract-ocr-other-languages.ipynb)
