CC = /usr/bin/g++-4.8

CFLAGS = -I. -Wall
//CPPFLAGS = -std=c++0x -I~/opt/casablanca/include -Wall -ggdb -c
CPPFLAGS = -std=c++0x -I/home/genius3/opt/casablanca/include -Wall -ggdb -c
LDFLAGS = -L/home/genius3/opt/casablanca/bin -lcpprest -lpthread -ggdb -Wall

CTAGS = ctags --recurse=yes
CLEAN_CTAGS = clean_tags

TRIAL_SRC =  main.cpp
TRIAL_OBJ = main.o
TARGET = tryCasandra

all: $(TARGET)

$(TARGET): $(TRIAL_OBJ)
	$(CC) -o $(TARGET) $(TRIAL_OBJ) $(LDFLAGS)

#.o.cpp:
.cpp.o :
	$(CC) $(CPPFLAGS) -o $@ $< > buildlog 2>&1

ctags:
	$(CTAGS)

$(CLEAN_CTAGS) :
	rm tags
 
clean: 
	-rm -f core
	-rm -f $(TRIAL_OBJ)
	-rm $(TARGET)
	-make $(CLEAN_CTAGS)
