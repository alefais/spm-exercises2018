CXX      = g++
CXXFLAGS = -Wall -Wextra -std=c++11

LDFLAGS  = -pthread
OPTFLAGS = -O3

DEPS = channel_queue.h collection.h modules.h utils.h
OBJS = collection.o main.o modules.o utils.o

.PHONY: main clean cleanall

%.o: %.cpp $(DEPS)
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $(OPTFLAGS) -o $@ -c $<

main: $(OBJS)
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $(OPTFLAGS) -o $@ $^

clean:
	rm -f $(OBJS)

cleanall: clean
	rm -f *.o *~