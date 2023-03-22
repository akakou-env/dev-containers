FROM core-akakou-devcontainer:latest

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs > install.sh 
RUN sh install.sh -y 
RUN pip3 install nrfutil
RUN apt-get install -y udev uuid-runtime usbutils byobu
ADD JLink.deb .
RUN /lib/systemd/systemd-udevd --daemon && apt-get install -y ./JLink.deb
