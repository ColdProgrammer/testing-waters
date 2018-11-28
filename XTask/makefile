SRCS = \
	main.c

OBJS = $(subst .c,.o,$(SRCS))

CFLAGS = -Wall
LIBS = -lOpenCL
TARGET = cl-fib
ifeq ($(OS),Windows_NT)
TARGET := $(TARGET).exe
endif

.SUFFIXES: .c .o

all : $(TARGET)

$(TARGET) : $(OBJS)
	gcc -o $@ $(OBJS) $(LIBS)

.c.o :
	gcc -c $(CFLAGS) -I. $< -o $@

clean :
	rm -f *.o $(TARGET)

 gcc -I /path-to-NVIDIA/OpenCL/common/inc -L /path-to-NVIDIA/OpenCL/common/lib/Linux64 -o hello hello.c -lOpenCL

