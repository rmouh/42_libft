# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rmouhoub <rmouhoub@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/11/10 16:09:23 by rmouhoub          #+#    #+#              #
#    Updated: 2022/11/12 19:40:52 by rmouhoub         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SRCS		= ft_memset.c \
			  ft_bzero.c \
			  ft_memcpy.c \
			  ft_memmove.c \
			  ft_memchr.c \
			  ft_memcmp.c \
			  ft_strlen.c \
			  ft_strlcpy.c \
			  ft_strlcat.c \
			  ft_strchr.c \
			  ft_strrchr.c \
			  ft_strnstr.c \
			  ft_strncmp.c \
			  ft_atoi.c \
			  ft_isalpha.c \
			  ft_isdigit.c \
			  ft_isalnum.c \
			  ft_isascii.c \
			  ft_isprint.c \
			  ft_toupper.c \
			  ft_tolower.c \
			  ft_calloc.c \
			  ft_strdup.c \
			  ft_substr.c \
			  ft_strjoin.c \
			  ft_strtrim.c \
			  ft_split.c \
			  ft_itoa.c \
			  ft_strmapi.c \
			  ft_putchar_fd.c \
			  ft_putstr_fd.c \
			  ft_putendl_fd.c \
			  ft_putnbr_fd.c
			  
OBJS	=	${SRCS:.c=.o}

BNS_SRCS	= ft_lstnew.c \
			  ft_lstadd_front.c \
			  ft_lstsize.c \
			  ft_lstlast.c \
			  ft_lstadd_back.c \
			  ft_lstdelone.c \
			  ft_lstclear.c \
			  ft_lstmap.c \
			  ft_lstiter.c

BONUS_OBJS = ${BNS_SRCS:.c=.o}

NAME	= libft.a

CC		= gcc
CFLAGS	= -Wall -Wextra -Werror

so:
	$(CC) -nostartfiles -fPIC $(CFLAGS) $(SRCS) ${BNS_SRCS}
	gcc -nostartfiles -shared -o libft.so $(OBJS) ${BONUS_OBJS}

.c.o:
				${CC} ${CFLAGS} -c $< -o ${<:.c=.o}

all:		${NAME}

$(NAME):	${OBJS}
				ar rc ${NAME} ${OBJS}
				ranlib ${NAME}

clean:
				rm -f ${OBJS} ${BONUS_OBJS}

fclean:		clean
				rm -f ${NAME}

re:				fclean all

rebonus:		fclean bonus

bonus:		${OBJS} ${BONUS_OBJS}
				ar rc ${NAME} ${OBJS} ${BONUS_OBJS}
				ranlib ${NAME}

.PHONY:			all clean fclean re bonus rebonus