# A Kernel Seedling
This module adds a file which reports the number of processes that are running. 

## Building
```shell
make
```
The make compiles the module

## Running
```shell
sudo insmod proc_count.ko
cat /proc/count
```
The insmod loads the module into the kernel 
The cat will open the file to show the process count

Results: 138
When opening the /proc/count file, it reported that 138 processes ran. 

## Cleaning Up
```shell
make clean
sudo rmmod proc_count.ko
```
The make clean removes the previous build information
The rmmod unloads the modules 

## Testing
```python
python -m unittest
```
Results: 
Ran 3 tests in 14.078s

OK

This command runs the included tests to see if the code works.

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

```shell
uname -r -s -v
```
Version: 5.14.8-arch1-1

This checks to see what kernel version this module was tested on. 

