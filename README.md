Ansible Web Project

Este projeto demonstra o uso do Ansible para automatizar o provisionamento e configuração de servidores Linux. O playbook realiza tarefas essenciais de infraestrutura, como:

Atualização de pacotes do sistema

Instalação e configuração do servidor web Nginx

Configuração de firewall para portas essenciais (22, 80, 443)

Criação de usuários e definição de permissões

Provisionamento de páginas HTML dinâmicas usando Jinja2

O objetivo é criar uma infraestrutura padronizada e segura, totalmente automatizada, ideal para aprendizado, testes e demonstração de habilidades em Ansible.

Pré-requisitos

Antes de executar o playbook, verifique se você possui:

Servidores Linux (Debian/CentOS) com SSH ativo

Ansible instalado na máquina local

Acesso root ou sudo nos servidores remotos

Git instalado (para versionamento e controle do projeto)

Estrutura do Projeto
ansible-web-project/
│
├── hosts                   # Inventário de servidores
├── playbooks/
│   └── site.yml            # Playbook principal
├── roles/                  # Diretório de roles
│   ├── webserver/
│   │   ├── tasks/
│   │   │   └── main.yml   # Tarefas do webserver
│   │   ├── handlers/
│   │   │   └── main.yml   # Ações notificadas, como reiniciar serviços
│   │   └── templates/
│   │       └── index.html.j2 # Template Jinja2 para páginas web
│   ├── firewall/
│   │   └── tasks/main.yml # Configurações de firewall
│   └── users/
│       └── tasks/main.yml # Criação de usuários e permissões
└── README.md

Detalhes das Roles
webserver/

Responsável por instalar e configurar o servidor web.

tasks/main.yml → Instalação e configuração do Nginx

handlers/main.yml → Tarefas executadas sob notificação (ex: reiniciar o serviço web)

templates/index.html.j2 → Página HTML dinâmica renderizada pelo Ansible

firewall/

Gerencia a configuração do firewall.

tasks/main.yml → Abre portas específicas (22, 80, 443) e aplica regras de segurança

users/

Administra contas de usuários.

tasks/main.yml → Criação de usuários, definição de senhas e permissões

