#******************************************************************************
#
# Makefile.driverlib-cm4f - Rules for building the driver library.
#
# Copyright (c) 2005-2012 Texas Instruments Incorporated.  All rights reserved.
# Software License Agreement
# 
# Texas Instruments (TI) is supplying this software for use solely and
# exclusively on TI's microcontroller products. The software is owned by
# TI and/or its suppliers, and is protected under applicable copyright
# laws. You may not combine this software with "viral" open-source
# software in order to form a larger program.
# 
# THIS SOFTWARE IS PROVIDED "AS IS" AND WITH ALL FAULTS.
# NO WARRANTIES, WHETHER EXPRESS, IMPLIED OR STATUTORY, INCLUDING, BUT
# NOT LIMITED TO, IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
# A PARTICULAR PURPOSE APPLY TO THIS SOFTWARE. TI SHALL NOT, UNDER ANY
# CIRCUMSTANCES, BE LIABLE FOR SPECIAL, INCIDENTAL, OR CONSEQUENTIAL
# DAMAGES, FOR ANY REASON WHATSOEVER.
# 
# This is part of revision 9453 of the Stellaris Peripheral Driver Library.
#
#******************************************************************************

#
# Defines the directory suffix that this project uses.
#
SUFFIX=-cm4f

#
# Set the processor variant.
#
VARIANT=cm4

#
# The base directory for StellarisWare.
#
ROOT=.

#
# Include the common make definitions.
#
include ${ROOT}/makedefs

#
# Where to find header files that do not live in the source directory.
#
IPATH=..

#
# The default rule, which causes the driver library to be built.
#
all: ${COMPILER}-cm4f
all: ${COMPILER}-cm4f/libdriver-cm4f.a
all:
	cp ${COMPILER}-cm4f/libdriver-cm4f.a yourlibdriverlib.a
#
# The rule to clean out all the build products.
#
clean:
	@rm -rf ${COMPILER}-cm4f ${wildcard *~}

objclean:
	@rm -f ${COMPILER}-cm4f/*.o
	@rm -f ${COMPILER}-cm4f/*.d
#
# The rule to create the target directory.
#
${COMPILER}-cm4f:
	@mkdir -p ${COMPILER}-cm4f

#
# Rules for building the driver library.
#
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/adc.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/aes.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/camera.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/cpu.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/crc.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/des.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/gpio.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/flash.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/hwspinlock.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/i2c.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/i2s.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/interrupt.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/pin.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/prcm.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/sdhost.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/shamd5.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/spi.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/systick.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/timer.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/uart.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/udma.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/utils.o
${COMPILER}-cm4f/libdriver-cm4f.a: ${COMPILER}-cm4f/wdt.o

#
# Include the automatically generated dependency files.
#
ifneq (${MAKECMDGOALS},clean)
-include ${wildcard ${COMPILER}-cm4f/*.d} __dummy__
endif
