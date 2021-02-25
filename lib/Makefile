TARGET = lib.a

LIBFILES_UNSORTED = $(notdir $(foreach x,$(wildcard $(TOPDIR)/lib/*.c),$(patsubst %.c,%.o,$(x))))
LIBFILES = $(sort $(LIBFILES_UNSORTED))


EFI_INCLUDES    = -I$(EFI_INCLUDE) -I$(EFI_INCLUDE)/$(ARCH) -I$(EFI_INCLUDE)/protocol -I$(TOPDIR)/../include \
		  -I$(TOPDIR)/CryptLib/Include/openssl/

lib.a: $(LIBFILES)
	$(AR) rcs lib.a $(LIBFILES)

all: $(TARGET)

clean:
	rm -f lib.a
	rm -f $(LIBFILES)

