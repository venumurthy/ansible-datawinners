ansible-datawinners
===================

Setup Datawinners using Ansible



Better have a VM created with a fresh install of Ubuntu 12.04
Setup the hostname to "dwdev"

    sudo sed -i 's/ubuntu/dwdev/g' /etc/hosts
    sudo sed -i 's/ubuntu/dwdev/g' /etc/hostname

Run the following Commands on the terminal if you have already downloaded the Oracle Java 7:-

    sudo apt-get update && \
    sudo apt-get -y install git-core && \
    sudo apt-get -y install alien && \
    sudo apt-get -y install python-software-properties && \
    sudo add-apt-repository -y ppa:rquillo/ansible && \
    sudo apt-get update && \
    sudo apt-get -y install ansible && \
    sudo alien -i --scripts jdk-7u67-linux-x64.rpm && \
    ((cd ansible-datawinners/ && git pull ) || (git clone https://github.com/mangroveorg/ansible-datawinners.git &&
    cd ansible-datawinners/)) && \
    ansible-playbook dev.yml --sudo -K
    
    
If you do not have java already downloaded then you can run the below script but you will need to be hooked onto your screen for a few minutes to accept the java install agreement. (Defaults are decline, be alert to select correctly)
    
    
    sudo apt-get update && \
    sudo apt-get -y install git-core && \
    sudo apt-get -y install python-software-properties && \
    sudo add-apt-repository -y ppa:webupd8team/java && \
    sudo add-apt-repository -y ppa:rquillo/ansible && \
    sudo apt-get update && \
    sudo apt-get -y install ansible && \
    sudo apt-get install -y oracle-java7-installer && \
    ((cd ansible-datawinners/ && git pull) || (git clone https://github.com/venumurthy/ansible-datawinners.git)) && \
    cd ansible-datawinners/ && \
    ansible-playbook dev.yml --sudo -K

This can take a few hours, upon all going well, you shoudl be able to get valid reponse from curl localhost:5984



