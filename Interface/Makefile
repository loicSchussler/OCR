# Makefile

CC = gcc -fsanitize=address
CFLAGS = `pkg-config --cflags sdl` `pkg-config --cflags gtk+-3.0` -O3 -MMD
LDFLAGS = `pkg-config --libs gtk+-3.0` `pkg-config --libs sdl` -lSDL_image -lm

SRC = alpaal.c ../XOR/XOR.c ../XOR/launch.c ../Treatment/toBlackWhite.c ../Treatment/pixel_operations.c ../Treatment/new_try.c ../Treatment/line_lib.c ../Treatment/word_lib.c ../Treatment/seg.c
OBJS=$(SRC:.c=.o)

all: 4puterscanread

alpaal: $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS) $(LDFLAGS)

clean:
	rm -rvf *~
	rm -rvf $(OBJS)
	rm -rvf *.d

fclean: clean
	rm -rvf 4puterscanread

re: fclean 4puterscanread
