# RISC OS Scripts
## Introduction
This repository contains a number of scripts to run on RISC OS. Zip files in this directory have been created on RISC OS, so the necessary file type information should be present.

The majority of files in this repository have been created in Python 3. You will need to have this installed on your machine. It is available through **Packman**. Some scripts may require you to install additional libraries. These are referred to below where required.

## Installation
You should place the files in the directory <code>!Boot.Library</code>.

## The scripts
### sequence
This script can be used to rename the files in a directory using sequential numbering. You can specify the files using wildcards, in which case the normal sorting order is employed, or you can list the filenames separated by spaces. The script will prefix the number by sufficient 0s to ensure that all the names have the same number of digits—ensuring that they will sort in the order you would expect.

File names can have an optional prefix and/or suffix. For more details, type:

	sequence -h

after the file has been installed.

### check-pdf
Some PDF files have the **mediabox** set different to the **cropbox**. This can cause issues when you're trying to convert them to a set of images. **check-pdf** is intended to solve this problem. If you run

	check-pdf <file>

it will tell you whether any pages have issues, and if so how many there are (usually, every page will be affected, or none at all). If there are any problems, repeat the command adding the option <code>--fix</code>, and the problems will be corrected, and a new PDF file written with <code>_fix</code> appended to it. Any file extension present will be kept. The PDF file to be checked must have the correct RISC OS filetype <code>&adf</code>. For more details, type:

	check-pdf -h

