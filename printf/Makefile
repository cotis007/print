CFILES = cleaning.c doping.c parsing_field.c parsing_flag.c flags.c this.c this_utils.c out.c parser.c precision.c ft_printf.c char_min.c utils.c floats.c parsing_utils.c itoa.c ful.c
OBJS = $(CFILES:.c=.o)
NAME = libftprintf.a
FLAGS = -Wall -Wextra -Werror -O2
LIBFT = libft
all: $(NAME)
$(NAME): $(OBJS)
	@make -sC $(LIBFT)
	@cp libft/libft.a ./$(NAME)
	@ar rc $(NAME) $(OBJS)
	@ranlib $(NAME)
%.o:%.c
	@gcc $(FLAGS) -o $@ -c $<
include $(wildcard *.d)
clean:
	@rm -f $(OBJS)
	@rm -rf $(DIR_O)
	@make clean -C $(LIBFT)
fclean: clean
	@rm -rf $(OBJS)
	@rm -f $(NAME)
	@make fclean -C $(LIBFT)
re: fclean all
