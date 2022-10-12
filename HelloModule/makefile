CXX = /usr/bin/g++-11
CXXFLAGS = -Wall -std=c++20 -fmodules-ts
EXECNAME = hello

all: hello.o main.o
	$(CXX) $(CXXFLAGS) -o $(EXECNAME) hello.o main.o

main.o: main.cc
	$(CXX) $(CXXFLAGS) -c main.cc

hello.o: hello.cc
	$(CXX) $(CXXFLAGS) -c hello.cc

.PHONY: clean
clean:
	rm *.o
	rm -r gcm.cache
	rm $(EXECNAME)
