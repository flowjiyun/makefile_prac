.PHONY : all clean fclean

NAME := main

SRC_DIR = ./src/
SRC_NAME = main.c \
			fourth.c
SRC = $(addprefix $(SRC_DIR),$(SRC_NAME))

OBJ_DIR = ./obj/
OBJ_NAME = $(SRC_NAME:.c=.o)
OBJ = $(addprefix $(OBJ_DIR),$(OBJ_NAME))

LIB_DIR = ./lib/
LIB_NAME = ft
LIB = $(LIB_DIR)lib$(LIB_NAME).a


CFLAGS := -Wall -Wextra -Werror
INCLUDE := -I./include -I./lib

all : $(NAME)

clean :
		rm -rf $(OBJ)
		make -C $(LIB_DIR) clean

fclean : clean
		rm -f $(NAME)

re : fclean all

run : all
		./$(NAME)

$(NAME) : $(LIB) $(OBJ)
		$(CC) $(CFLAGS) -o $@ $^
$(LIB) :
		make -C $(LIB_DIR) all
$(OBJ_DIR)%.o : $(SRC_DIR)%.c
		mkdir -p $(OBJ_DIR)
		$(CC) $(CFLAGS) $(INCLUDE) -c $< -o $@
