# Installing compton on Fedora 30

Let me prefix this by saying that English is not my native language so there might be some strange grammar mistakes in this. You have been warned. I'm also relatively new to Linux so i solved my problems with trial and error, but i think i have it boiled down to the least amount of steps and packages.

## Dependencies

These are the names of the required packages in Fedora 30. A list of the dependencies can be found over on [tryone's github](https://github.com/tryone144/compton#Building)
```
libXcomposite-devel
libXdamage-devel
libconfig-devel
mesa-libGL-devel
dbus-devel
asciidoc
``` 

All of these can be installed using dnf: 
```
$ sudo dnf install libXcomposite-devel libXdamage-devel libconfig-devel mesa-libGL-devel dbus-devel asciidoc
```

## Get repo and install

All there is left to do now is grab the repo and install compton:
```bash
# Clone the repo
$ git clone https://github.com/tryone144/compton
# cd into the cloned repo
$ cd compton
# Make the main program
$ make
# Make docs
$ make docs
# Install (this will likely require root privileges)
$ make install
```

Then you should be able to start compton from the commandline using:  
```bash
compton
```

And that's it!