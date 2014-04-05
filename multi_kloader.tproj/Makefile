Project = multi_kloader
ProductType = tool
Install_Dir = /usr/bin

CFILES = multi_kloader.c

Extra_CC_Flags = -Wall  -DINLINE_IT_ALL -no-integrated-as
Extra_LD_Flags = -framework IOKit -framework CoreFoundation

include $(MAKEFILEPATH)/CoreOS/ReleaseControl/BSDCommon.make

after_install:
	$(INSTALL_DIRECTORY) "$(DSTROOT)"/usr/libexec
	$(INSTALL_FILE) entitlements "$(DSTROOT)"/usr/libexec
	codesign -s- --entitlements $(DSTROOT)/usr/libexec/entitlements  $(DSTROOT)/$(Install_Dir)/$(ProductName)
	rm -f $(DSTROOT)/usr/libexec/entitlements

