
AS := arm-none-eabi-as
LD := arm-none-eabi-ld

SRCS := $(wildcard *.s)
OBJS := $(patsubst %.s,%.o,$(SRCS))
TARGETS := $(patsubst %.s,%,$(SRCS))

.PHONY: all clean

all: $(TARGETS)

%: %.s
	$(AS) -o $(<:.s=.o) $<
	$(LD) -o $@ $(<:.s=.o)

clean:
	rm -f $(OBJS) $(TARGETS)

.PHONY: all clean
