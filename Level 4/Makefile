NAME := libft.a
SRCS := first.c second.c third.c
OBJS := $(SRCS:.c=.o)
ARFLAGS := -rc

CFLAGS := -Wall -Wextra -Werror

all : $(NAME)

$(NAME) : $(OBJS)
		$(AR) $(ARFLAGS) $@ $?

%.o : %.c
		$(CC) $(CFLAGS) -c $<

clean :
		rm -f *.o
fclean : clean
		rm -f $(NAME)
re : fclean all

.PHONY : all clean fclean
