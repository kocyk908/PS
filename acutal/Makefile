NAME	:= push_swap

CC	:= gcc

CFLAGS	:= -Wall -Wextra -Werror -Iheaders/

PS_SRC	:= $(wildcard functions/S_P_R_RR/*.c)
COMM_SRC := $(wildcard functions/commands/*.c)
LIBFT_SRC := $(wildcard utils/libft/*.c)
PRINTF_SRC := $(wildcard utils/ft_printf/*.c)

PS_OBJ := $(PS_SRC:.c=.o)
COMM_OBJ := $(COMM_SRC:.c=.o)
LIBFT_OBJ := $(LIBFT_SRC:.c=.o)
PRINTF_OBJ := $(PRINTF_SRC:.c=.o)

OBJ := $(PS_OBJ) $(COMM_OBJ) $(LIBFT_OBJ) $(PRINTF_OBJ)

GREEN := \033[0;32m
NC := \033[0m

all: $(NAME)

$(NAME): $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)
	@echo "$(GREEN)Build successful!$(NC)"

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf $(OBJ)

fclean: clean
	rm -rf $(NAME)

re: fclean all

