Getting started
===============
In order to get started with bombard, one must needs to first install requirements. Once the requirements have been satisfied, then it can be configured ande compiled

Note: In order to compile from source system development packages maybe required

```
./configure
make
sudo make install
```

Requirements
------------

[See Requirements](Requirements.md)

Running bombard
---------------
Need to create a file that contains all the urls that will need to be under siege. This can be done like this

```
echo "http://mywebsite.com/blah" >> ~/urls.txt
echo "http://mywebsite2.com/blah2" >> ~/urls.txt
```

Example:

```
bombard -f ~/urls.txt -s 10 -i 3
```

-s 10 means, first run will be done using 10 users
-i 3 means, that every run (default 10) will be done in multiples of 3

This will generate .png graphs etc in directory named such as ~/160213.

