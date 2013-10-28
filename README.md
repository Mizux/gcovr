Overview
--------

Gcovr provides a utility for managing the use of the GNU gcov utility
and generating summarized code coverage results. This command is
inspired by the Python coverage.py package, which provides a similar
utility in Python. The gcovr command produces either compact
human-readable summary reports, machine readable XML reports (in
Cobertura format) or simple HTML reports. Thus, gcovr can be viewed
as a command-line alternative to the lcov utility, which runs gcov
and generates an HTML-formatted report.

Gcovr is available under the BSD License.

A user guide can be downloaded from http://gcovr.com.

Gcovr development moved to this repository in September, 2013 from
Sandia National Laboratories.

qiBuild Integration
-------------------

qiBuild repository: https://github.com/aldebaran/qibuild

> qibuild configure -c toolchain --coverage  
> qibuild make -c toolchain  
> ./build-toolchain/sdk/bin/mytest

> gcovr -d -r . --exclude test build-toolchain --html --html-detail -o out.html

Option:  
--delete -d : avoid to have results merged with the previous run (i.e. clean gcov stat).  
--root -r : specify the root point (i.e. filter all files not in this repository our below).  
--exclude "pattern" : remove all files matching the pattern (i.e. remove test directory from coverage report).  

