ansible-datawinners
===================

Setup Datawinners using Ansible

Better have a VM created with a fresh install of Ubuntu 12.04

Run the following Commands on the terminal:-

    sudo apt-get update && sudo apt-get -y install git-core && \
    sudo apt-get -y install python-software-properties && \
    sudo add-apt-repository -y ppa:webupd8team/java && \
    sudo add-apt-repository -y ppa:rquillo/ansible && \
    sudo apt-get update && \
    sudo apt-get -y install ansible && \
    sudo apt-get install -y oracle-java7-installer && \
    ((cd ansible-datawinners/ && git pull) || (git clone https://github.com/venumurthy/ansible-datawinners.git)) && \
    cd ansible-datawinners/ && ansible-playbook dev.yml --sudo -K

