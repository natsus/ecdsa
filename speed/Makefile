CXX = g++
LIBS = -ltepla -lcrypto -lgmp
CXXFLAGS  = -Wall -g -O4

TARGET = speed_check
OBJ = speed_check.o
LIBDIR = -L/usr/local/lib
INCDIR = -I/usr/local/include

all: $(TARGET)

%: %.o
	$(CXX) $(CXXFLAGS) -o $@ $< $(INCDIR) $(LIBDIR) $(LIBS)
 
%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< $(INCDIR)

$(OBJ): ../ecdsa.h

.PHONY: clean
clean:
	$(RM) *~ $(TARGET) $(OBJ)
