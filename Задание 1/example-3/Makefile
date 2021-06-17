# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg
KAZINO_FILE       = Kazino-Royal.cpp

all: debug release

debug: $(DEBUG_EXEC)

hello-dbg: $(KAZINO_FILE)
	g++ $(DEBUG_FLAGS) $(KAZINO_FILE) -o $(DEBUG_EXEC) 

release: $(RELEASE_EXEC)

hello: $(KAZINO_FILE)
	g++ $(RELEASE_FLAGS) $(KAZINO_FILE) -o $(RELEASE_EXEC)

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

