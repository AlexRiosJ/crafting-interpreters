# Directories
SRC_DIR = java/lox
BUILD_DIR = java/build

# Sources
SOURCES = $(wildcard $(SRC_DIR)/*.java)

all: compile

compile:
    mkdir -p $(BUILD_DIR)
    javac -d $(BUILD_DIR) $(SOURCES)

run: compile
    java -cp $(BUILD_DIR) lox.Lox

run-args: compile
    java -cp $(BUILD_DIR) lox.Lox $(ARGS)

clean:
    rm -rf $(BUILD_DIR)
