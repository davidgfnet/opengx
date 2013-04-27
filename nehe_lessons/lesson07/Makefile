

CC = powerpc-eabi-gcc -MMD -MP -Wall -DGEKKO -mrvl -mcpu=750 -meabi -mhard-float -DHW_RVL -DGAMECUBE_WII -ggdb
INCLUDE_FLAGS = -I ../../include/ -I ../../extlib/include/  -I $(DEVKITPPC)/include -I $(DEVKITPPC)/libogc/include
LIB_PATH = -L ../../extlib/lib -L ../../src/ -L $(DEVKITPPC)/lib/wii -L $(DEVKITPPC)/libogc/lib/wii

all:
	$(CC)   $(INCLUDE_FLAGS) -c lesson07.c
	$(CC)   lesson07.o -o lesson07.elf  -g -MMD -MP -Wl,-Map,$(notdir $@).map  $(LIB_PATH) -lopengx -lSDL -lfat -logc -lwiiuse -lwiikeyboard -lm -lbte
	elf2dol lesson07.elf lesson07.dol

clean:
	rm -f *.elf *.o *.dol *.d all.map lesson07

linux:
	gcc -o lesson07 lesson07.c -lGL -lGLU -lSDL

