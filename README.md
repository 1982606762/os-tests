# os-tests

## Introduction

os-tests is a lightweight, fast check and tests collection for Linux OS.

## Installation

`# pip install os-tests`

## Run test

### Run all os_tests supported cases

`# python3 -m unittest -v os_tests.os_tests_all`

### Run all cases in one file

`# python3 -m unittest -v os_tests.tests.test_general_check`

### Run single case in one file

`# python3 -m unittest -v os_tests.tests.test_general_test.TestGeneralTest.test_change_clocksource`

### The log file

The console only shows the case test result as summary.
The test debug log file are saved in "/tmp/os_tests_result" following case name by default.
You can change "results_dir" in "cfg/os-tests.yaml" to save log in other place.

Below is an example:

```bash
# python3 -m unittest -v os_tests.tests.test_general_test.TestGeneralTest.test_change_clocksource
test_change_clocksource (os_tests.tests.test_general_test.TestGeneralTest) ... ok

----------------------------------------------------------------------
Ran 1 test in 0.117s

OK
# ls -l /tmp/os_tests_result/
total 8
-rw-r--r--. 1 root root 4224 Aug 26 10:11 os_tests.tests.test_general_test.TestGeneralTest.test_change_clocksource.debug
```

### The installed files

All test files are located in "os_tests/tests" directory.

```bash
# pip3 show -f os_tests
Name: os-tests
Version: 0.0.1
Summary: Lightweight, fast check and tests collection for Linux OS
Home-page: https://github.com/liangxiao1/os-tests
Author: Xiao Liang
Author-email: xiliang@redhat.com
License: GPLv3+
Location: /usr/local/lib/python3.6/site-packages
Requires: PyYAML
Files:
  os_tests-0.0.1.dist-info/INSTALLER
  os_tests-0.0.1.dist-info/METADATA
  os_tests-0.0.1.dist-info/RECORD
  os_tests-0.0.1.dist-info/WHEEL
  os_tests-0.0.1.dist-info/top_level.txt
  os_tests/__init__.py
  os_tests/__pycache__/__init__.cpython-36.pyc
  os_tests/__pycache__/os_tests_all.cpython-36.pyc
  os_tests/cfg/os-tests.yaml
  os_tests/data/base.json
  os_tests/libs/__init__.py
  os_tests/libs/__pycache__/__init__.cpython-36.pyc
  os_tests/libs/__pycache__/utils_lib.cpython-36.pyc
  os_tests/libs/utils_lib.py
  os_tests/os_tests_all.py
  os_tests/tests/__init__.py
  os_tests/tests/__pycache__/__init__.cpython-36.pyc
  os_tests/tests/__pycache__/test_general_check.cpython-36.pyc
  os_tests/tests/__pycache__/test_general_test.cpython-36.pyc
  os_tests/tests/test_general_check.py
  os_tests/tests/test_general_test.py

```
