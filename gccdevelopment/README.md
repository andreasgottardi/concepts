# Setting up gcc for C/C++ development

It can be tricky to get a compiler suite up and running and there are a few things to keep in mind when setting up these programs. This guide provides assistance to achieve this goal.

## Goals and scopes

When implemented a program called "gcc" will be available globally. This means, that a console like PowerShell or cmd can be opened anywhere on the system and the command "gcc" is available and can be executed to compile a regular c file.

```bash
goa@MY-HOST MINGW64 ~
$ gcc
gcc.exe: fatal error: no input files
compilation terminated.
```

This is the output when called without a c file specified. It fails, but the program is available. To achieve this goal a system called "[Msys2](https://www.msys2.org)" is used. There is an installer available and feel free to use it. In this guide here the tar.gz distribution is used to demonstrate the whole process of integration.

## Acquiring the software

Unfortunately the tar.gz distribution is hidden and not directly accessible from the website. The distributions are listed on [this page](https://repo.msys2.org/distrib/x86_64). Take the latest version. For example the archive https://repo.msys2.org/distrib/x86_64/msys2-base-x86_64-20210105.tar.xz is from the 5th of January 2021 and it is the latest version there was when writing this tutorial. Look at the list and pick the latest version. Save it somewhere on your system.

To extract you need a program like [PeaZip](https://peazip.github.io) or [7zip](https://www.7-zip.de). Whith this tools you can extract the tar.gz file. The filename indicates, that that it is a tar file (**t**ape **ar**chiver) that is compressed with **gz**ip. Thus it has to be extracted twice because it is a uncompressed archive in a compressed archive. Most archivers can uncompress the file in one run.

## Install location

## Integration into system

## Updating

## The first program
