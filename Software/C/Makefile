default:
		avr-gcc -Os -DF_CPU=16000000UL -mmcu=atmega328p -c -o build/test.o src/main.c
		avr-gcc -o build/test.bin build/test.o
		avr-objcopy -O ihex -R .eeprom build/test.bin build/test.hex
load:
		sudo avrdude -F -V -c arduino -p ATmega328P -P /dev/ttyUSB1 -b 57600 -U flash:w:build/test.hex