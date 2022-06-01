PROG = blinky 

CC = arm-none-eabi-gcc
LD = arm-none-eabi-gcc
CP = arm-none-eabi-objcopy
CFLAGS = -g -mcpu=cortex-m4 -mthumb -o0 -Wall  		
LFLAGS = -nostdlib -T stm32f401-rom.ld -Wl,-Map=blinky.map

OBJS = startup.o \
	   main.o

all: $(PROG).elf

$(PROG).elf: $(OBJS)
	$(LD) $(LFLAGS) $^ -o $@
	$(CP) $(PROG).elf -O binary $(PROG).bin

%.o: %.c
	$(CC) -c $(CFLAGS) $< -o $@

clean:
	rm -f $(OBJS) $(PROG).elf 
	rm -f $(PROG).bin 
	rm -f $(PROG).map
	

