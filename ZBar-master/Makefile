GCC = arm-linux-androideabi-gcc
TARGET = libzar.so
SRC_FILES = java/zbarjni.c \
		zbar/img_scanner.c \
		zbar/decoder.c \
		zbar/image.c \
		zbar/symbol.c \
		zbar/convert.c \
		zbar/config.c \
		zbar/scanner.c \
		zbar/error.c \
		zbar/refcnt.c \
		zbar/video.c \
		zbar/video/null.c \
		zbar/decoder/code128.c \
		zbar/decoder/code39.c \
		zbar/decoder/code93.c \
		zbar/decoder/codabar.c \
		zbar/decoder/databar.c \
		zbar/decoder/ean.c \
		zbar/decoder/i25.c \
		zbar/decoder/qr_finder.c \
		zbar/qrcode/bch15_5.c \
		zbar/qrcode/binarize.c \
		zbar/qrcode/isaac.c \
		zbar/qrcode/qrdec.c \
		zbar/qrcode/qrdectxt.c \
		zbar/qrcode/rs.c \
		zbar/qrcode/util.c

CFLAGS_INCLUDE = -I./include \
		-Iandroid/jni \
		-Izbar \
		-I../libiconv-1.15.2/include/

CFLAGS_LIBS = -L../libiconv-1.15.2 -liconv -llog

$(TARGET) : $(SRC_FILES)
	$(GCC) -shared -fPIC -o $(TARGET) $(SRC_FILES) $(CFLAGS_INCLUDE) $(CFLAGS_LIBS)

clean:
	rm -rf $(TARGET)