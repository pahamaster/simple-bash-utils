# Makefile

CFLAGS=-c -Wall -Werror -Wextra

all: build

rebuild: clean all

test: build test_cat
	cp -f s21_cat ./test/s21_cat
	cd test && ./test

test_cat: test.o test_cat.o
	gcc test.o test_cat.o -o test/test

test.o: ../test/test.c
	gcc $(CFLAGS) ../test/test.c -o test.o

test_cat.o: test/test_cat.c
	gcc $(CFLAGS) test/test_cat.c -o test_cat.o

# "Build"
build: s21_cat

s21_cat: s21_cat.o
	gcc s21_cat.o -o s21_cat

s21_cat.o: s21_cat.c
	gcc $(CFLAGS) s21_cat.c -o s21_cat.o

clean:
	rm -f *.o *.a *.so s21_cat
	cd test && rm -f *.o e1 e2 r r1 r2 s21_cat test valgrind.txt
