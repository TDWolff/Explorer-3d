CXX = clang++
CXXFLAGS = -std=c++17 -Wall $(shell sdl2-config --cflags)
LDFLAGS = $(shell sdl2-config --libs) -framework OpenGL

SRC = $(wildcard src/*.cpp)
OBJ = $(SRC:.cpp=.o)
TARGET = explorer3d

all: $(TARGET)

$(TARGET): $(OBJ)
    $(CXX) -o $@ $^ $(LDFLAGS)

%.o: %.cpp
    $(CXX) $(CXXFLAGS) -c $< -o $@

clean:
        rm -f $(OBJ) $(TARGET)