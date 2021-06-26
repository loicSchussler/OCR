CC=gcc
CFLAGS=-W -Wall -Wextra -Werror -g `pkg-config --cflags sdl` -MMD
LDFLAGS= `pkg-config --libs sdl` -lSDL_image

EXEC= main
SRCS= toBlackWhite.c pixel_operations.c new_try.c line_lib.c word_lib.c main.c
OBJS=$(SRCS:.c=.o)

all: $(EXEC)


$(EXEC): $(OBJS)
	$(CC) -o $@ $^ $(LDFLAGS)

#$(OBJS): $(SRCS)
#	$(CC) -c $? $(CFLAGS)

clean:
	rm -rvf *~
	rm -rvf \#*
	rm -rvf $(OBJS)
	rm -rvf *.d

fclean: clean
	rm -rvf $(EXEC)
	rm -rvf *.bmp

re: fclean $(EXEC)
