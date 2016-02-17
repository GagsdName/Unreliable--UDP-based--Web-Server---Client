BIN = ../bin/
OBJ = ../obj/
SRC = ../src/
INCLUDE = -I../include
CC = gcc
CFLAGS = -c -Wall -g

all:$(BIN)http_udp_server $(BIN)http_udp_client $(BIN)index.html

$(BIN)index.html:$(SRC)index.html 
	mv $(SRC)index.html $(BIN).

$(BIN)http_udp_server:$(OBJ)http_udp_server.o
	$(CC) -o http_udp_server $(OBJ)http_udp_server.o
	mv ./http_udp_server $(BIN)

$(OBJ)http_udp_server.o:$(SRC)http_udp_server.c ../include/header.h
	$(CC) $(CFLAGS) $(SRC)http_udp_server.c  $(INCLUDE)
	mv ./http_udp_server.o $(OBJ)

$(BIN)http_udp_client:$(OBJ)http_udp_client.o
	$(CC) -o http_udp_client $(OBJ)http_udp_client.o
	mv ./http_udp_client $(BIN)

$(OBJ)http_udp_client.o:$(SRC)http_udp_client.c ../include/header.h
	$(CC) $(CFLAGS) $(SRC)http_udp_client.c  $(INCLUDE)
	mv ./http_udp_client.o $(OBJ)

clean :
	rm $(OBJ)*.o
	rm $(BIN)*
