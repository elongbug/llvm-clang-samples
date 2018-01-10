CC = clang++
#CC = g++
TARGET1 = access_debug_metadata
SOURCE1 = $(TARGET1).cpp

TARGET2 = analyze_geps
SOURCE2 = $(TARGET2).cpp

TARGET3 = bb_toposort_sccs
SOURCE3 = $(TARGET3).cpp

TARGET3 = replace_threadidx_with_call
SOURCE3 = $(TARGET3).cpp

TARGET4 = simple_bb_pass
SOURCE4 = $(TARGET4).cpp

TARGET5 = simple_module_pass
SOURCE5 = $(TARGET5).cpp

.PHONY: all
all: $(TARGET1) $(TARGET2) $(TARGET3) $(TARGET4) $(TARGET5)

$(TARGET1) : $(SOURCE1)
	$(CC) $(SOURCE1) -o $(TARGET1) -g -O3 `llvm-config --cxxflags --ldflags --system-libs --libs core mcjit native`

$(TARGET2) : $(SOURCE2)
	$(CC) $(SOURCE2) -o $(TARGET2) -g -O3 `llvm-config --cxxflags --ldflags --system-libs --libs core mcjit native`

$(TARGET3) : $(SOURCE3)
	$(CC) $(SOURCE3) -o $(TARGET3) -g -O3 `llvm-config --cxxflags --ldflags --system-libs --libs core mcjit native`

$(TARGET4) : $(SOURCE4)
	$(CC) $(SOURCE4) -o $(TARGET4) -g -O3 `llvm-config --cxxflags --ldflags --system-libs --libs core mcjit native`

$(TARGET5) : $(SOURCE5)
	$(CC) $(SOURCE5) -o $(TARGET5) -g -O3 `llvm-config --cxxflags --ldflags --system-libs --libs core mcjit native`

.PHONY: clean 
clean :
	rm $(TARGET1) $(TARGET2) $(TARGET3) $(TARGET4) $(TARGET5)
