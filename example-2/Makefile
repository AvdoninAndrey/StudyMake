# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg
SOURCE        = hello.cpp

all: debug release

debug: $(DEBUG_EXEC)

hello-dbg: $(SOURCE)
	g++ $(DEBUG_FLAGS) $< -o $@

release: $(RELEASE_EXEC)

hello: $(SOURCE)
	g++ $(RELEASE_FLAGS) $< -o $@

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
