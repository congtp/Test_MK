# -c : Generate object file
## LINKER FLAGS
# -lm: link math.h library, link at the .o -> .exe
## COMPILER FLAGS
# -Wall: turn on warning for all
# -Werror: turn on Error notify


# MODULE_NAME is a Macro
MODULE_NAME = sqrt_test

TARGET_DIR = ../../bins
TARGET_NAME = sqrt_test_bin
TARGET = $(TARGET_DIR)/$(TARGET_NAME)

# OBJ files
OBJ_DIR = ../../objs
OBJ1 = $(OBJ_DIR)/$(MODULE_NAME).o

# Compiler Flags
CFLAGS = -Wall -Werror

# Linker Flags
LDFLAGS = -lm

$(TARGET): $(OBJ1)
# $(^) : Dependency = $^
# $(@) : TARGET = $@
	gcc $(^) -o $(@) $(LDFLAGS)

$(OBJ1): $(MODULE_NAME).c
	gcc $(CFLAGS) -c $(^) -o $(@)

clean: 
	rm $(TARGET) $(OBJ1) 	