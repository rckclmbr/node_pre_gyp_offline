# node-pre-gyp offline POC

This example demonstrates that node-pre-gyp cannot work in offline mode.  

# Usage

First, disable network access.  Then just try to install the packages

  yarn install --offline --frozen-lockfile &> logs.txt

[logs.txt](logs.txt) has been committed as an example.

The npm packages get installed correctly, but node-pre-gyp first fails
downloading the binary, then fails compiling.  There is no option to install
the binaries from an offline location, like the node_modules
