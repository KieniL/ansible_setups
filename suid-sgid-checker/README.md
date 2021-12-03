SUID-SGID-Checker
=========

This role was created with 
<code>
molecule init role suid-sgid-checker -d docker
</code>

And then:
<code>
rm -rf suid-sgid-checker/meta/
</code>
------------

It is run with molecule.

# Prerequisites
sudo apt install python3-pip

# Installation

We need ansible, molecule and docker

## ansible
sudo apt update && sudo apt install software-properties-common && sudo add-apt-repository --yes --update ppa:ansible/ansible && sudo apt install ansible

## molecule
pip3 install molecule

Add molecule to path
vi ~/.bashrc
PATH=$PATH:/home/lukas/.local/bin

:wq

source ~/.bashrc

## Docker
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update && sudo apt-get install docker-ce docker-ce-cli containerd.io


pip3 install git+https://github.com/ansible-community/molecule-docker.git

Check with:
<code>
molecule drivers
</code>

sudo usermod -aG docker $USER

## linters
sudo apt-get install yamllint ansible-lint flake8
# Usage

molecule init role suid-sgid-checker -d docker




# Testing
You can run <code>molecule test</code>


Otherwise on a push to github it will run molecule also against multiple images