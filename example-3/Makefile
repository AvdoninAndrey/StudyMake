# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean
Komp=g++
#Компляция с++ программ

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = Kazino-Royal
DEBUG_EXEC    = Kazino-Royal-dbg
SOURCE        = Kazino-Royal.cpp

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)
	$(Komp) $(DEBUG_FLAGS) $< -o $@

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)
		$(Komp) $(RELEASE_FLAGS) $< -o $@

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
