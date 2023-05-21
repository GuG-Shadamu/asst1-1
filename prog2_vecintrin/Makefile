
all: myexp
debug: myexp_debug

logger.o: logger.cpp logger.h CS149intrin.h CS149intrin.cpp
	g++ -c logger.cpp

CS149intrin.o: CS149intrin.cpp CS149intrin.h logger.cpp logger.h
	g++ -c CS149intrin.cpp

myexp: CS149intrin.o logger.o main.cpp
	g++ -I../common logger.o CS149intrin.o main.cpp -o myexp

myexp_debug: CS149intrin.o logger.o main.cpp
	g++ -I../common logger.o CS149intrin.o main.cpp -o myexp -DDEBUG -g

clean:
	rm -f *.o myexp *~
