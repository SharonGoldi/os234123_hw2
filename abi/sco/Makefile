#	$Id: Makefile,v 1.9 2001/10/22 12:51:07 hch Exp $

O_TARGET        := dummy.o

list-multi      := abi-sco.o
abi-sco-objs	:= sysent.o misc.o mmap.o ptrace.o secureware.o \
		   stat.o statvfs.o

# various ioctl emulation stuff
abi-sco-objs	+= ioctl.o termios.o tapeio.o vtkbd.o


obj-$(CONFIG_ABI_SCO)		+= abi-sco.o


include $(TOPDIR)/Rules.make

abi-sco.o: $(abi-sco-objs)
	$(LD) -r -o $@ $(abi-sco-objs)
