FROM ubuntu:24.04

ENV IMAGE_NAME=MikanOS

RUN apt-get update && \
    apt-get install -y \
    vim \
    build-essential \
    python3 \
    git \
    okteta \
    tmux \
    dosfstools \
    sudo \
    ansible

RUN groupadd -g 2000 vscode && \
    useradd -m -s /bin/bash -u 2000 -g 2000 vscode && \
    echo "vscode:password" | chpasswd && \
    echo "vscode ALL=(ALL:ALL) NOPASSWD: ALL" >> /etc/sudoers

USER vscode:vscode

# https://github.com/uchan-nos/mikanos-build
RUN cd $HOME; \
    git clone https://github.com/uchan-nos/mikanos-build.git osbook; \
    cd $HOME/osbook/devenv; \
    # Ubuntu24.04 の Python3.12 から python3-distutils は deprecated
    sed -i 's/python3-distutils/python3-setuptools/' ansible_provision.yml; \
    ansible-playbook -K -i ansible_inventory ansible_provision.yml  --extra-vars "ansible_become_pass=password"

CMD ["/bin/bash"]
