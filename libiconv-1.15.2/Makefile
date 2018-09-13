CC = arm-linux-androideabi-gcc
TARGET = libiconv.so
SRC_FILES = lib/iconv.c \
		libcharset/lib/localcharset.c \
		lib/relocatable.c

CFLAGS_INCLUDE = -I ./include \
		-I ./ \
		-I libcharset \
		-I libcharset/include

CFLAGS_LIBRARY = -Wno-multichar -D_ANDROID -DLIBDIR="c" -DBUILDING_LIBICONV -DBUILDING_LIBCHARSET -DIN_LIBRARY

$(TARGET) : $(SRC_FILES)
	$(CC) -shared -fPIC $(SRC_FILES) -o $(TARGET) $(CFLAGS_INCLUDE) $(CFLAGS_INCLUDE) $(CFLAGS_LIBRARY)

clean:
	rm -rf $(TARGET)
