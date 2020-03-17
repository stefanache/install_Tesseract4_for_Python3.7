Hi,

I intend to follow this tutorial
      https://www.pyimagesearch.com/2018/09/17/opencv-ocr-and-text-recognition-with-tesseract/
      
For that must to have
  Python 3.7
  OpenCV 4
  Tesseract
  ....
So need to have installed the Tesseract ...

About Tesseract
------------------

The Tesseract OCR engine has been around since the 1980s. 
As of 2018, it now includes built-in deep learning capability making it a robust OCR tool (just keep in mind that no OCR system is perfect). 
Using Tesseract with OpenCV’s EAST detector makes for a great combination.

Ref by:

      https://www.pyimagesearch.com/2017/07/10/using-tesseract-ocr-python/
      https://www.pyimagesearch.com/2018/09/17/opencv-ocr-and-text-recognition-with-tesseract/


The Tesseract used for extract text from image file or/and from pdf file.

So it is detectror of text.


Before at all:
---------------

I already have installed Python 3.7.7 on my windows 10 Pro (32 bits):

  cmd.exe
  
  C:\Users\{User}>python
  
Python 3.7.7 (tags/v3.7.7:d7c567b08f, Mar 10 2020, 11:52:54) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> CTRL+Z
 
 
I intend to install Tesseract 4 for my Python 3.7.7

I seen that it work good with OpenCV

            so before that see the my installement at https://github.com/stefanache/install_OpenCV4_on_w10Pro

Base of work:
--------------

For that I use/follow  this tutorial:

     https://github.com/nikhilkumarsingh/tesseract-python


Step 1
-------

Install Tesseract-OCR as standalone system which have api interface for Python,PhP...

For Windows download installer from 

      https://github.com/UB-Mannheim/tesseract/wiki
      
 I preffered this
 
      tesseract-ocr-w64-setup-v5.0.0-alpha.20200223.exe (64 bit) 
  
 because and python is for 64 bits(w64).
 
 The download will be doned into C:\Users\{User}\Downloads 
 
 After download click on the installer to run it:
 
       tesseract-ocr-w64-setup-v5.0.0-alpha.20200223.exe
       
 The tesseract will be install into 
 
       C:\Program Files\Tesseract-OCR
       
Remark :
--------
        -Add in System Variables PATH this link:
           
        C:\Program Files\Tesseract-OCR       
 
 Step 2
 ------
 
 To can call Tesseract into Python must to have one binding tool like pytesseract.
 
 So, install python binding for tesseract, pytesseract, using this pip command:
 
          C:\Users\{User}> python -m pip install pytesseract

Step 3
--------
Also install image processing library in python, pillow using this pip command:
           C:\Users\{User}> python -m pip install pillow




If want to work only images is enought to have pytesseract and pillow.

But if you want to work with pdf files need to install and other two components:

            - Imagemagick (standalone system with various api interfaces for Python,PhP...)
            
            and its bidding tool for python

            - wand
            
Remark: So is simmilar with previous installment:

           - tesseract-ocr (standalone system with various api interfaces for Python,PhP...)
           
           and its imagging tool for python
           
            - pillow

For working with pdf files:
----------------------------

Step 4
-------

Install imagemagick using one installer.
You find Imagemagick installer from

           https://imagemagick.org/script/download.php

find at Windows Binary Release the installer named:
 
          ImageMagick-7.0.10-1-Q16-x64-dll.exe
          
The download will be doned into C:\Users\{User}\Downloads 

After download then run this installer of Imagemagick

The standalone iMamagick will be reside into 

          C:\Program Files\ImageMagick-7.0.10-Q16
          
Then test it like in https://imagemagick.org/script/download.php

            magick logo: logo.gif
            magick identify logo.gif
            magick logo.gif win:

Remark :
--------
       - Check if is added in System Variables PATH this link:
        
        C:\Program Files\ImageMagick-7.0.10-Q16
        
        -Also can add new variable:
        
        MAGICK_HOME :                   C:\Program Files\ImageMagick-7.0.10-Q16
        
        WAND_MAGICK_LIBRARY_SUFFIX :   -7.Q16;-7.Q16HDRI;.Q16HDRI;.Q16
        
        -After that you then can ceheck with:
        
            C:\Users\{user}>set MAGIC_HOME
            
            MAGIC_HOME=C:\Program Files\ImageMagick-7.0.10-Q16

Step 5
-------

Install python binding for imagemagick, wand, using this pip command:

          C:\Users\{User}> python -m pip install wand
          
You can find documentation for wand at this link:

          http://docs.wand-py.org/en/0.5.9/
 
 Remark:
 --------
        -Is possible to help you this documentation:
        
        http://docs.wand-py.org/en/latest/guide/install.html#install-imagemagick-on-windows
        
        -For testing use the command:
 
              C:\Users\{user}> # Test installation
              C:\Users\{user}> python -mwand.version
              0.5.9
 
 
 Step 6
 ------
 
Now must to use these using samples from github's tutorial link:

     https://github.com/nikhilkumarsingh/tesseract-python
     
For that need to have git installed from     

      https://git-scm.com/downloads
      
After that use it to download :

cmd.exe

c:\Users\{User}> cd \

c:\> git clone https://github.com/nikhilkumarsingh/tesseract-python

c:\> cd tesseract-python

c:\tesseract-python> dir

             Volume in drive C has no label.
             Volume Serial Number is 32EF-A4A7

             Directory of C:\tesseract-python

            03/17/2020  08:31 AM    <DIR>          .
            03/17/2020  08:31 AM    <DIR>          ..
            03/17/2020  08:31 AM               148 image_example.py
            03/17/2020  08:31 AM                54 output.txt
            03/17/2020  08:31 AM               510 pdf_example.py
            03/17/2020  08:31 AM             1,028 README.md
            03/17/2020  08:31 AM            38,022 sample1.jpg
            03/17/2020  08:31 AM            28,983 sample2.pdf
                           6 File(s)         68,745 bytes
                           2 Dir(s)  32,357,650,432 bytes free

c:\tesseract-python> type image_example.py

            from PIL import Image
            import pytesseract

            im = Image.open("sample1.jpg")

            text = pytesseract.image_to_string(im, lang = 'eng')

            print(text)
            
c:\tesseract-python> type pdf_example.py

            import io
            from PIL import Image
            import pytesseract
            from wand.image import Image as wi

            pdf = wi(filename = "sample2.pdf", resolution = 300)
            pdfImage = pdf.convert('jpeg')

            imageBlobs = []

            for img in pdfImage.sequence:
                  imgPage = wi(image = img)
                  imageBlobs.append(imgPage.make_blob('jpeg'))

            recognized_text = []

            for imgBlob in imageBlobs:
                  im = Image.open(io.BytesIO(imgBlob))
                  text = pytesseract.image_to_string(im, lang = 'eng')
                  recognized_text.append(text)

            print(recognized_text)


So now we can run the samples:

cmd.exe

c:\Users\{User}> cd \tesseract-python

- a) check detection text from jpg image file(as natural scene) - for STEPS 1-3:

c:\tesseract-python> python image_example.py 

            The quick brown fox
            jumped over the 5
            lazy dogs!

- b) check detection text from pdf file(as natural scene) - for STEPS 4-8:

c:\tesseract-python> python pdf_example.py           

