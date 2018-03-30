CFLAGS=-Wall -ggdb
LDFLAGS=/usr/lib/arm-linux-gnueabihf/libmosquitto.so.1 

.PHONY: all clean

all : mqtt_test

mqtt_test : mqtt_test.o
	${CC} $^ -o $@ ${LDFLAGS}

mysql_log.o : mqtt_test.c
	${CC} -c $^ -o $@ ${CFLAGS} -I../../lib

clean : 
	-rm -f *.o mqtt_test
