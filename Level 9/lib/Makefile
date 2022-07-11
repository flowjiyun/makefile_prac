all : libft.a

clean :
		rm -f *.o

fclean : clean
		rm -f libft.a

re : fclean all

libft.a : first.o second.o third.o
		ar -rc $@ $?
.PHONY : all clean fclean re