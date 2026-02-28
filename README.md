# ansible-personal-playbook

Playbook pessoal criado para automatizar a instalação e configuração de um Ubuntu após uma instalação limpa (fresh install).

## Descrição

Este projeto utiliza o [Ansible](https://www.ansible.com/) para automatizar a configuração do ambiente de desenvolvimento e uso pessoal no Ubuntu. Com um único comando, é possível instalar pacotes, configurar ferramentas e personalizar o sistema operacional de forma reproduzível.

## Pré-requisitos

- Ubuntu (versão 20.04 ou superior)
- Acesso à internet
- Privilégios de superusuário (sudo)

## Instalação do Ansible

Antes de executar o playbook, é necessário instalar o Ansible na máquina. Execute os comandos abaixo no terminal:

```bash
sudo apt update
sudo apt install -y software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```

Verifique se a instalação foi concluída com sucesso:

```bash
ansible --version
```

## Como executar o playbook

1. Clone este repositório:

```bash
git clone https://github.com/andredss99/ansible-personal-playbook.git
cd ansible-personal-playbook
```

2. Execute o playbook com o comando abaixo:

```bash
ansible-playbook playbook.yml --ask-become-pass
```

O parâmetro `--ask-become-pass` solicitará a senha do `sudo` para executar as tarefas que requerem privilégios de superusuário.

## O que este playbook configura

- Atualização do sistema operacional
- Instalação de pacotes e ferramentas de desenvolvimento
- Configuração de aplicativos pessoais

## Licença

Este projeto é de uso pessoal e não possui uma licença formal.
