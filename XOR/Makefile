# Makefile

CC = gcc -fsanitize=address
CPPFLAGS = -MMD -D_XOPEN_SOURCE=500
CFLAGS = -Wall -Wextra -std=c99 -O3 -g 
LDFLAGS = 
LDLIBS = -lm

OBJ = XOR.o main.o
DEP = ${OBJ:.o=.d}

all: main

main: ${OBJ}

clean:
	${RM} ${OBJ} ${DEP} main
	rm finalresult.txt
-include ${DEP}
remove:
	${RM} ${OBJ} ${DEP} main
-include ${DEP}

# END
