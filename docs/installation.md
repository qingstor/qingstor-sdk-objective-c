# Installation Guide

## Requirement

To use the QingStor SDK for Objective C, you need:

* Visual Studio 2013 or later
* OR GNU Compiler Collection (GCC) 4.1.2 or later
    * 4GB of RAM
    * 4GB of RAM is required to build some of the larger clients.

Additional Requirements for Linux Systems

To compile on Linux, you must have the header files (-dev packages) for libcurl, libopenssl. Typically, you'll find the packages in your system's package manager.

To install these packages on Debian/Ubuntu-based systems
``` bash
$ sudo apt-get install libcurl4-openssl-dev libssl-dev
```

To install these packages on Redhat/Fedora-based systems
``` bash
$ sudo yum install libcurl-devel openssl-devel
```


## Install from source code

Clone with Git:

``` bash
$ git clone https://github.com/yunify/qingstor-sdk-objective-c.git
```

You can also download a specified version of zipped source code in the repository [releases page](https://github.com/yunify/qingstor-sdk-objective-c/releases). The zipped source code only contains source code without unit test files.


### Creating an Out-of-Source Build (Recommended):
To create an **out-of-source build**:
1. Install CMake and the relevant build tools for your platform. Ensure these are available in your executable path.
2. Create your build directory. Replace BUILD_DIR with your build directory name:

```
cd BUILD_DIR
cmake <path-to-root-of-this-source-code>
```

You can use the following variations to create your build directory:
* For Auto Make build systems:
`make`


To create a **release build**, do the following:
* For Auto Make build systems:
```
cmake -DCMAKE_BUILD_TYPE=Release  <path-to-root-of-this-source-code>
make
sudo make install
```

To create a **debug build with symbolic information**, do the following:
* For Auto Make build systems:
```
cmake -DCMAKE_BUILD_TYPE=Debug  <path-to-root-of-this-source-code>
make
sudo make install
```

To create a **static library**, do the following:
* For Auto Make build systems:
```
cmake -DBUILD_STATICLIB=ON  <path-to-root-of-this-source-code>
make
sudo make install
```

To create a **build with C style interface (defaul is off)**, do the following:
```
cmake -DBUILD_C_STYLE_INTERFACE=ON  <path-to-root-of-this-source-code>
make
sudo make install
```

## Examples
We provide a sample for C and a sample for C++. The samples show how to use cmake to introduce SDK to build project:
`samples/samples_sdk_c` and `samples/samples_sdk_cpp`.


