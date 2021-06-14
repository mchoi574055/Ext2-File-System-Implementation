# Ext2 File System Implementation in C

This code seeks to create a valid ext2 filesystem in c by creating a .img that
can be mounted to a directory that holds all the files.

## Building

Simply build the program by typing "make".

## Running

Show how to compile, mount, and example output of `ls -ain` your mounted
filesystem.

Compilation is done when after building with "make". Execute the program by
typing "./ext2-create". This will create a file called cs111-base.img, which
you can mount to a directory. For example, create a directory called mnt by
typing "mkdir mnt", then mount with "sudo mount -o loop cs111-base.img mnt".
Go to the directory by typing "cd mnt". Now you can type "ls -ain" to see all
the files in that directory. It should display as something like this:

total 7
     2 drwxr-xr-x 3    0    0 1024 Jun  6 15:53 .
941125 drwxr-xr-x 3 1000 1000 4096 Jun  6 15:56 ..
    13 lrwxr-xr-x 1 1000 1000   11 Jun  6 15:53 hello -> hello-world
    12 -rwxr-xr-x 1 1000 1000   12 Jun  6 15:53 hello-world
    11 drwxr-xr-x 2    0    0 1024 Jun  6 15:53 lost+found


## Cleaning up

Explain briefly how to unmount the filesystem, remove the mount directory, and
clean up all binary files.

Unmount the filesystem by going back to the lab-04 directory and typing
"sudo umount mnt". Remove the directory by typing "rmdir mnt". Simply clean
all binary files by typing "make clean".
