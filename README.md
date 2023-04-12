# reportlab-experimenting
Some playing around with reportlab to generate PDF files using Python

All code in the iPython [notebook](reportlab-experimenting.ipynb)

## Requirements

Although not replicated to the repo, this notebook runs from a virtual environment based on Python 3.11.1

Use the following sequence of steps to create the virtual environment, and to ensure all necessary libraries are installed for that venv (this assumes a Windows PC - modify as required for other platforms):

1. Assuming that your repo is in the following path  
`C:\GitHub\reportlab-experimenting`  
using a command prompt at that path, create your virtual environment, in this case named "base":  
`C:\GitHub\reportlab-experimenting>python -m venv base`

2. Activate your new "base" virtual environment:  
`C:\GitHub\reportlab-experimenting>base\Scripts\activate.bat`

3. Install the necessary libraries into the activated environment:  
`(base) C:\GitHub\reportlab-experimenting>pip install numpy`  
`(base) C:\GitHub\reportlab-experimenting>pip install reportlab`  
`(base) C:\GitHub\reportlab-experimenting>pip install lorem`

4. The installation of reportlab should also install pillow library, if required

5. Once reportlab is installed, download additional font files, specifically a barcode39 font named "LibreBarcode39-Regular.ttf" - search for the download location currently on [google fonts](https://fonts.google.com/specimen/Libre+Barcode+39). If necessary, unzip the archive file and drop the file named LibreBarcode39-Regular.ttf into the folder  
`C:\GitHub\reportlab-experimenting\base\Lib\site-packages\reportlab\fonts`  
Alternatively, you can download a similar font from [barcodesinc](https://www.barcodesinc.com/free-barcode-font/) and then extract the extended font file `fre3of9x.ttf`

6. In your development environment (I use VS-Code) choose your Python interpreter to point to the "base" virtual environment you just created, as well as the Python kernel

7. When running the code, you may be prompted to install the iPython kernel in order to run iPython notebooks within VS-Code - accept the installation

Your environment should be ready to use with the [notebook](reportlab-experimenting.ipynb)

The result of running the code is to generate the file [reportlab_pdf.pdf](reportlab_pdf.pdf)

## Real-world Example

As an additional exercise, I attempt to replicate a sample PDF file that can be downloaded from the Adobe website at:

https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf

This file has been downloaded to the repo and can be seen [here](c4611_sample_explain.pdf)

The code to reproduce this file is located in the [real-world-example.ipynb](real-world-example.ipynb) notebook file and the resulting output is located in file [real-world-example.pdf](real-world-example.pdf)

This code has additional functionality to add things like bookmarks and encryption not available in the sample file provided by Adobe