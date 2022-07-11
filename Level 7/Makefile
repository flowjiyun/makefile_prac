NAME := main

SRCS := main.c
OBJS := $(SRCS:.c=.o)

LIBFT := libft.a
LIB_SRCS := first.c second.c third.c
LIB_OBJS := $(LIB_SRCS:.c=.o)


CFLAGS := -Wall -Wextra -Werror
ARFLAGS := -rc
all : $(NAME)

clean :
		rm -f *.o
fclean: clean
		rm -f $(NAME) $(LIBFT)
re : fclean all

$(NAME) : $(OBJS) $(LIBFT)
		$(CC) $(CFLAGS) -o $@ $?
$(LIBFT) : $(LIB_OBJS)
		$(AR) $(ARFLAGS) $@ $?

%.o : %.c
		$(CC) $(CFLAGS) -c $<
.PHONY : all clean fclean