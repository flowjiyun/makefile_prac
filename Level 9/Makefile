NAME := main

SRC_DIR = ./src/
SRC_NAME = main.c \
					first.c \
					second.c \
					third.c
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
		rm -f $(OBJ)

fclean : clean
		rm -f $(NAME)

re : fclean all

run : all
		./$(NAME)

$(NAME) : $(OBJ)
		$(CC) $(CFLAGS) -o $@ $^
$(LIBFT) : $(LI
		$(AR) $(ARFLAGS) $@ $?
$(OBJ_DIR)%.o : $(SRC_DIR)%.c
		@mkdir -p $(OBJ_DIR)
		$(CC) $(CFLAGS) $(INCLUDE) -c $< -o $@

.PHONY : all clean fclean