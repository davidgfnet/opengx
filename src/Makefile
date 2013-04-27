

CC = powerpc-eabi-gcc
AR = powerpc-eabi-ar
CFLAGS = -MMD -MP -Wall -DGEKKO -mrvl -mcpu=750 -meabi -mhard-float  -DHW_RVL -O2 -ggdb
INCLUDE_FLAGS = -I $(DEVKITPPC)/include -I ../include/ -I $(DEVKITPPC)/libogc/include

all:
	$(CC) $(CFLAGS) $(INCLUDE_FLAGS) -c gc_gl.c
	$(CC) $(CFLAGS) $(INCLUDE_FLAGS) -c image_DXT.c
	$(AR) rcs libopengx.a gc_gl.o image_DXT.o

clean:
	rm -f gc_gl.o image_DXT.o libopengx.a *.d


