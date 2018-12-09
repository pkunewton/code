cc = gcc
src = $(shell find ./ -name "*.c")
deps = "$(shell find ./ -name "*.h") ../include/apue.h"
obj = $(src:%.c=%.o)
progs = $(src:%.c=%)

all: ${progs}

# %.o: %.c ${deps}
# 	${cc} -I../include -c $< -o $@

%: %.c
	${cc}-I../include $@.c -o $@ -L../lib -lapue
	
clean:
	rm -rf ${obj} ${progs}