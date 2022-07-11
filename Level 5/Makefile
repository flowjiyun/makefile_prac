NAME := libft.a
SRCS := first.c second.c third.c
OBJS := $(SRCS:.c=.o)
ARFLAGS := -rc

CFLAGS := -Wall -Wextra -Werror

$(NAME) : $(OBJS)
		$(AR) $(ARFLAGS) $@ $?

%.o : %.c
		$(CC) $(CFLAGS) -c $<

