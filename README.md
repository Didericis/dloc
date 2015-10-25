# Didericis's Library for Open Computers (dloc)

dloc is a very small, npm-ish package manager for [opencomputers](http://ocdoc.cil.li/). It was created because oppm (the current pacakage management system for opencomputers) does not allow for multiple versions of the same dependencies.

### Requirements ###

* bash
* [jq](https://stedolan.github.io/jq/)
* git - Must be installed to the command line/accessible to bash scripts

### Installation ###

1. Clone using `git clone https://github.com/Didericis/dloc.git`
* Add to your path. 
  * EX: If you cloned to `~/dloc`, add `PATH=$PATH:~/opt/bin` to your .bash_profile 
* Make sure it's executable by doing `sudo chmod 744 dloc`
* Point dloc to an installation location
  * Create a new folder in one of your opencomputers filesystem folders called `dloc`
  * Set the variable `dlocDir` within the script to the absolute path of this folder
  
### Usage ###

Go a folder containing a `dloc.json` and type `dloc install`.

### Specification ###

* The main file must be called `main.lua`.
* The package must be defined in `dloc.json` and be formatted like so [* will be required]:
```
{
  "name*":
  "version*":
  "repo": 
  "dependencies": {
    [name]: [version]
  }
}
```

### ToDo ###

* Use `.cfg` instead of `.json`
* Allow for github repo specifications
* Convert to lua
