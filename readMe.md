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

The standalone iMageMagick 7.0.10 (Q16) will be reside into 

          C:\Program Files\ImageMagick-7.0.10-Q16
          
 You can see and identify that:
 
          Major version number:   7
          Magick Quantum:         Q16
          Optional HDRI-Support:  blanck(not exist!)
          
Then test it like in https://imagemagick.org/script/download.php

            cmd.exe

            C:\Users\{user}>magick logo: logo.gif
            C:\Users\{user}>magick identify logo.gif
            C:\Users\{user}>magick logo.gif win:

If need to have some informationa about Visual Studio do that:
                  From Windows Menu Go
                  In Visual Studio, then Tab 'Help'-> 'About Microsoft Visual Studio' should give you the desired infos.
                  
                  I have Microsoft Visual C++ 2017 -see info copied:
                  
                        Microsoft Visual Studio Community 2017 
                        Version 15.9.4
                        VisualStudio.15.Release/15.9.4+28307.222
                        Microsoft .NET Framework
                        Version 4.8.03752

                        Installed Version: Community

                        Visual C++ 2017   00369-60000-00001-AA459
                        Microsoft Visual C++ 2017

                        Application Insights Tools for Visual Studio Package   8.14.11009.1
                        Application Insights Tools for Visual Studio

                        ASP.NET and Web Tools 2017   15.9.04012.0
                        ASP.NET and Web Tools 2017

                        ASP.NET Core Razor Language Services   15.8.31590
                        Provides languages services for ASP.NET Core Razor.

                        ASP.NET Web Frameworks and Tools 2017   5.2.60913.0
                        For additional information, visit https://www.asp.net/

                        Azure App Service Tools v3.0.0   15.9.03024.0
                        Azure App Service Tools v3.0.0

                        Azure Data Lake Node   1.0
                        This package contains the Data Lake integration nodes for Server Explorer.

                        Azure Data Lake Tools for Visual Studio   2.3.3000.2
                        Microsoft Azure Data Lake Tools for Visual Studio

                        Azure Functions and Web Jobs Tools   15.9.02046.0
                        Azure Functions and Web Jobs Tools

                        Azure Stream Analytics Tools for Visual Studio   2.3.3000.2
                        Microsoft Azure Stream Analytics Tools for Visual Studio

                        C# Tools   2.10.0-beta2-63501-03+b9fb1610c87cccc8ceb74a770dba261a58e39c4a
                        C# components used in the IDE. Depending on your project type and settings, a different version of the compiler may be used.

                        Common Azure Tools   1.10
                        Provides common services for use by Azure Mobile Services and Microsoft Azure Tools.

                        Cookiecutter   15.9.18254.1
                        Provides tools for finding, instantiating and customizing templates in cookiecutter format.

                        Extensibility Message Bus   1.1.49 (remotes/origin/d15-8@ee674f3)
                        Provides common messaging-based MEF services for loosely coupled Visual Studio extension components communication and integration.

                        Fabric.DiagnosticEvents   1.0
                        Fabric Diagnostic Events

                        JavaScript Language Service   2.0
                        JavaScript Language Service

                        JavaScript Project System   2.0
                        JavaScript Project System

                        JavaScript UWP Project System   2.0
                        JavaScript UWP Project System

                        Microsoft Azure HDInsight Azure Node   2.3.3000.2
                        HDInsight Node under Azure Node

                        Microsoft Azure Hive Query Language Service   2.3.3000.2
                        Language service for Hive query

                        Microsoft Azure Service Fabric Tools for Visual Studio   2.4
                        Microsoft Azure Service Fabric Tools for Visual Studio

                        Microsoft Azure Stream Analytics Language Service   2.3.3000.2
                        Language service for Azure Stream Analytics

                        Microsoft Azure Stream Analytics Node   1.0
                        Azure Stream Analytics Node under Azure Node

                        Microsoft Azure Tools   2.9
                        Microsoft Azure Tools for Microsoft Visual Studio 2017 - v2.9.10730.2

                        Microsoft Continuous Delivery Tools for Visual Studio   0.4
                        Simplifying the configuration of Azure DevOps pipelines from within the Visual Studio IDE.

                        Microsoft JVM Debugger   1.0
                        Provides support for connecting the Visual Studio debugger to JDWP compatible Java Virtual Machines

                        Microsoft Library Manager   1.0
                        Install client-side libraries easily to any web project

                        Microsoft MI-Based Debugger   1.0
                        Provides support for connecting Visual Studio to MI compatible debuggers

                        Microsoft Visual C++ Wizards   1.0
                        Microsoft Visual C++ Wizards

                        Microsoft Visual Studio Tools for Containers   1.1
                        Develop, run, validate your ASP.NET Core applications in the target environment. F5 your application directly into a container with debugging, or CTRL + F5 to edit & refresh your app without having to rebuild the container.

                        Microsoft Visual Studio VC Package   1.0
                        Microsoft Visual Studio VC Package

                        MLGen Package Extension   1.0
                        MLGen Package Visual Studio Extension Detailed Info

                        Mono Debugging for Visual Studio   4.13.12-pre (9bc9548)
                        Support for debugging Mono processes with Visual Studio.

                        MySQL for Visual Studio   1.2.9
                        Data design and management tools for MySQL. Copyright (c) 2007, 2019, Oracle and/or its affiliates. All rights reserved.

                        Node.js Tools   1.4.21001.1 Commit Hash:8dd15923800d931b153ab9e4de74e42a74eba5e6
                        Adds support for developing and debugging Node.js apps in Visual Studio

                        NuGet Package Manager   4.6.0
                        NuGet Package Manager in Visual Studio. For more information about NuGet, visit http://docs.nuget.org/.

                        Office Developer Tools for Visual Studio 2017 ENU   15.0.28224.00
                        Microsoft Office Developer Tools for Visual Studio 2017 ENU

                        ProjectServicesPackage Extension   1.0
                        ProjectServicesPackage Visual Studio Extension Detailed Info

                        Python   15.9.18254.1
                        Provides IntelliSense, projects, templates, debugging, interactive windows, and other support for Python developers.

                        Python - Django support   15.9.18254.1
                        Provides templates and integration for the Django web framework.

                        Python - IronPython support   15.9.18254.1
                        Provides templates and integration for IronPython-based projects.

                        Python - Profiling support   15.9.18254.1
                        Profiling support for Python projects.

                        ResourcePackage Extension   1.0
                        ResourcePackage Visual Studio Extension Detailed Info

                        ResourcePackage Extension   1.0
                        ResourcePackage Visual Studio Extension Detailed Info

                        SQL Server Data Tools   15.1.61810.11040
                        Microsoft SQL Server Data Tools

                        Test Adapter for Boost.Test   1.0
                        Enables Visual Studio's testing tools with unit tests written for Boost.Test.  The use terms and Third Party Notices are available in the extension installation directory.

                        Test Adapter for Google Test   1.0
                        Enables Visual Studio's testing tools with unit tests written for Google Test.  The use terms and Third Party Notices are available in the extension installation directory.

                        ToolWindowHostedEditor   1.0
                        Hosting json editor into a tool window

                        TypeScript Tools   15.9.20918.2001
                        TypeScript Tools for Microsoft Visual Studio

                        Visual Basic Tools   2.10.0-beta2-63501-03+b9fb1610c87cccc8ceb74a770dba261a58e39c4a
                        Visual Basic components used in the IDE. Depending on your project type and settings, a different version of the compiler may be used.

                        Visual C++ for Cross Platform Mobile Development (Android)   15.0.28107.00
                        Visual C++ for Cross Platform Mobile Development (Android)

                        Visual C++ for Linux Development   1.0.9.28218
                        Visual C++ for Linux Development

                        Visual F# Tools 10.2 for F# 4.5   15.8.0.0.  Commit Hash: 6e26c5bacc8c4201e962f5bdde0a177f82f88691.
                        Microsoft Visual F# Tools 10.2 for F# 4.5

                        Visual Studio Code Debug Adapter Host Package   1.0
                        Interop layer for hosting Visual Studio Code debug adapters in Visual Studio

                        Visual Studio Tools for Apache Cordova   15.123.7408.1
                        Visual Studio Tools for Apache Cordova

                        Visual Studio Tools for CMake   1.0
                        Visual Studio Tools for CMake

                        Visual Studio Tools for Containers   1.0
                        Visual Studio Tools for Containers

                        Visual Studio Tools for Unity   3.9.0.3
                        Visual Studio Tools for Unity

                        Visual Studio Tools for Universal Windows Apps   15.0.28307.208
                        The Visual Studio Tools for Universal Windows apps allow you to build a single universal app experience that can reach every device running Windows 10: phone, tablet, PC, and more. It includes the Microsoft Windows 10 Software Development Kit.

                        VisualStudio.Mac   1.0
                        Mac Extension for Visual Studio

                        Workflow Manager Tools 1.0   1.0
                        This package contains the necessary Visual Studio integration components for Workflow Manager.

                        Xamarin   4.12.3.77 (d15-9@e3f40b477)
                        Visual Studio extension to enable development for Xamarin.iOS and Xamarin.Android.

                        Xamarin Designer   4.16.13 (45a16efd4)
                        Visual Studio extension to enable Xamarin Designer tools in Visual Studio.

                        Xamarin Templates   1.1.128 (6f5ebb2)
                        Templates for building iOS, Android, and Windows apps with Xamarin and Xamarin.Forms.

                        Xamarin.Android SDK   9.1.4.2 (HEAD/8255f42fc)
                        Xamarin.Android Reference Assemblies and MSBuild support.

                        Xamarin.iOS and Xamarin.Mac SDK   12.2.1.12 (65ec520)
                        Xamarin.iOS and Xamarin.Mac Reference Assemblies and MSBuild support.

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

