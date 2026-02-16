LOX_DIR = lox
TOOL_DIR = tool
BUILD_DIR = build
LOX_SOURCES = $(wildcard $(LOX_DIR)/*.java)
TOOL_SOURCES = $(wildcard $(TOOL_DIR)/*.java)

all: compile

compile:
	@mkdir -p $(BUILD_DIR)
	@javac -d $(BUILD_DIR) $(LOX_SOURCES)
	@javac -d $(BUILD_DIR) $(TOOL_SOURCES)

run: compile
	@java -cp $(BUILD_DIR) lox.Lox

run-args: compile
	@java -cp $(BUILD_DIR) lox.Lox $(ARGS)

gen-ast: compile
	@java -cp $(TOOL_DIR) tool.GenerateAst $(LOX_DIR)

clean:
	@rm -rf $(BUILD_DIR)
