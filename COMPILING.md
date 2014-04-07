# Compiling `ios_kexec_tools`

This release is compiled like a standard Apple B&I or Darwin project.

<pre>
$ git clone git://github.com/winocm/ios-kexec-utils
$ cd ios-kexec-utils
$ mkdir -p sym obj dst
$ make install RC_ARCHS=armv7 SDKROOT=<iPhoneOS_SDKDirectory> \
    OBJROOT=$(pwd)/obj DSTROOT=$(pwd)/dst SYMROOT=$(pwd)/sym
</pre>
