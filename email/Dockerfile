FROM ubuntu:20.04

RUN apt update

RUN apt upgrade -y

RUN apt install postfix dovecot-imapd dovecot-pop3d -y

#COPY main.cf /etc/postfix
#
#COPY 10-auth.conf /etc/dovecot/conf.d

#Add User
RUN useradd -m gabriel

# Set user passord
RUN echo "gabriel:123"|chpasswd

#Add User
RUN useradd -m almeida

# Set user passord
RUN echo "almeida:123"|chpasswd

CMD ["/bin/bash", "-c", "service dovecot start; postfix start-fg"]