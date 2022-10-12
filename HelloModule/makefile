CXX = /usr/bin/g++-11
CXXFLAGS = -Wall -std=c++20 -fmodules-ts
EXECNAME = hello

SYSTEM_HEADERS = iostream

all: system-header hello.o main.o
	$(CXX) $(CXXFLAGS) -o $(EXECNAME) hello.o main.o

main.o: main.cc
	$(CXX) $(CXXFLAGS) -c main.cc

hello.o: hello.cc
	$(CXX) $(CXXFLAGS) -c hello.cc

system-header:
	@for header in $(SYSTEM_HEADERS); do \
		$(CXX) $(CXXFLAGS) -xc++-system-header $$header; \
		echo "Compiling Header Module:" $$header; \
	done

.PHONY: clean
clean:
	rm *.o
	rm -r gcm.cache
	rm $(EXECNAME)
