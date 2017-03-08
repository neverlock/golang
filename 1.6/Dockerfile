FROM  golang:1.6

MAINTAINER Chanchai Junlouchai "neverlock@gmail.com"

RUN apt-get update && apt-get install -y vim && apt-get clean
RUN mkdir -p /root/.vim/bundle
RUN git clone https://github.com/gmarik/Vundle.vim.git /root/.vim/bundle/Vundle.vim
COPY vimrc /root/.vimrc
RUN git clone https://github.com/fatih/vim-go.git /root/.vim/bundle/vim-go
RUN echo "alias ls='ls --color'" >> /root/.bashrc

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

WORKDIR $GOPATH

