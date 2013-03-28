EXE := lm4flash

CFLAGS := -Wall -g -O2 $(shell pkg-config --cflags libusb-1.0)
LDFLAGS := $(shell pkg-config --libs libusb-1.0)

all: $(EXE)

$(EXE): $(EXE).c
	gcc $(CFLAGS) $^ $(LDFLAGS) -o $@

clean:
	rm -f *.o $(EXE)

install:
	install -D -m755 lm4flash /usr/local/bin/lm4flash

.PHONY: all clean
