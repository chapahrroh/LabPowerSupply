default:
		avr-gcc -Os -DF_CPU=16000000UL -mmcu=atmega328p -c -o test.o test.c
		avr-gcc -o test.bin test.o
		avr-objcopy -O ihex -R .eeprom test.bin test.hex
load:
		sudo avrdude -F -V -c arduino -p ATmega328P -P /dev/ttyUSB1 -b 57600 -U flash:w:test.hex