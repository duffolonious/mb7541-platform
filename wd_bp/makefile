#Makefile for DOS DJGPP
#DIRECT_IO_ACCESS always defined


ifeq ($(DJGPP),)
$(error *** Abort the build. \
            This makefile ONLY work for DJGPP. \
            Try other Makefile ***)
endif

default: config
	cd src
	make
	cd ..

config:
	del  .\include\config.h
	echo //Created by Makefile, do not edit it >> .\include\config.h
	-echo #define DIRECT_IO_ACCESS >> .\include\config.h
	-echo #undef LANNER_DRIVER >> .\include\config.h


clean:
	del .\include\config.h
	cd src
	make clean
	cd ..

.PHONY: default clean config
