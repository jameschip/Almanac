# Almanac
A small shell script for life journaling. 

I wrote this as a simple way for me to keep track of the progress i have made on projects. If you find it usefull too then that is a bonus.

Entries can be added to the almanac and are date/time stamped with when they were entered. Each entry has an associated subject tag, the default tag is "personal" but a custom tag can be set. The default tag can be changes in __~/.almanac.d/config__. The log file itself is in __~/.almanac.d/log__.

# Install

* Clone this repo.
* chmod +x almanac
* Copy _almanac_ to a location in your path.
* Log things and enjoy.

# Use

### Add an entry to the almanac.
```
almanac -m "This is the message to log"
```
This will add an entry to the almanac with the default tag of 'personal' or what you have set the tag in the config file to  

### Add an entry to the almanac with a different tag
```
almanac -s work -m "This is the message to log"
```
This will add an entry to the almanac with the tag specified after the -s flag.

### Display the whole almanac
```
almanac -A
```
This will display all of the entries in the almanac to the cli.

### Display all entries for tag
```
almanac -S work
```
This will display any entries in the almanac for the given tag.

### Display entries by date
The -Y and -M tags display entries from the given year or month respectivley. They can be combined like so.
```
almanac -M 1 -Y 19
```
This will display all of the entries for January 2019. These can also be combined with a tag search:
``` 
almanac -S work -Y 19
```
Will display all of the entries in 2019 with the work tag.

### Display used tags
```
almanac -T
```
### Display the number of posts for each tag
```
almanac -C
```

### Display the last entry inserted into the almanac
```
almanac -l
```

### Remove an entry from the almanac
```
almanac --remove-entry <the long number at the start of the entry goes here>
```
Note that this has the ability to remove MANY entries from the almanac at once, it works by regex matching the number at the start of the entry. If you put 010119 then any entries with a number that starts 010119 will be permenantly removed from the log. THIS CAN NOT BE UNDONE SO IF YOU REMOVE THINGS YOU WANT TO KEEP ITS ON YOU! This command will print out the entries that will be removed and ask you if you really want to proceed. you have to input y or Y to proceed otherwise the log stays untouched.


```
