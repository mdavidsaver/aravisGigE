TOP=../..

include $(TOP)/configure/CONFIG

# -------------------------------
# Build an Diamond Support Module
# -------------------------------

# Build some little helper functions
#PROD_IOC += aravisTest
#aravisTest_SRCS_DEFAULT += aravisTest.c
#aravisTest_LIBS += $(EPICS_BASE_IOC_LIBS)

LIBRARY_IOC += aravisCamera

# The following are compiled and added to the support library
aravisCamera_SRCS += aravisCamera.cpp

DBD += aravisCameraSupport.dbd

USR_CPPFLAGS += $(shell pkg-config --cflags glib-2.0 aravis-0.4)
USR_LDFLAGS += $(shell pkg-config --libs glib-2.0 aravis-0.4)

include $(TOP)/configure/RULES
