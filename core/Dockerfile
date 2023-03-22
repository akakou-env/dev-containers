FROM ubuntu:latest AS core
RUN yes | unminimize
RUN apt-get update
RUN apt-get install -y zsh git python3 python3-pip vim udev curl wget build-essential
WORKDIR /root
RUN git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime \
    && sh ~/.vim_runtime/install_awesome_vimrc.sh
RUN curl -L https://raw.github.com/liangxianzhe/oh-my-vim/master/tools/install.sh | sh
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)";
RUN chsh -s /bin/zsh
