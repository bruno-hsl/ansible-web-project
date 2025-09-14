🚀 Ansible Web Project

Um projeto de automação de infraestrutura com Ansible, que provisiona servidores Linux de forma rápida, padronizada e segura. Ideal para aprendizado, demonstração de habilidades ou ambientes de teste.

✨ O que este projeto faz

O playbook executa as seguintes tarefas:

🛠 Atualização do sistema – mantém os pacotes sempre atualizados

🌐 Instalação e configuração do Nginx – servidor web pronto para uso

🔥 Configuração de firewall – abre portas essenciais: 22, 80, 443

👤 Gerenciamento de usuários – criação de contas e definição de permissões

📄 Provisionamento de páginas HTML dinâmicas – usando Jinja2

O objetivo é criar uma infraestrutura automatizada, segura e replicável.

📋 Pré-requisitos

Antes de rodar o playbook, verifique se você tem:

Servidores Linux (Debian/CentOS) com SSH ativo

Ansible instalado na máquina local

Acesso root ou sudo nos servidores remotos

Git instalado (para versionamento e controle do projeto)

🗂 Estrutura do Projeto

ansible-web-project/
│
├── hosts
├── playbooks/
│   └── site.yml
├── roles/
│   ├── webserver/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── handlers/
│   │   │   └── main.yml
│   │   └── templates/
│   │       └── index.html.j2
│   ├── firewall/
│   │   └── tasks/main.yml
│   └── users/
│       └── tasks/main.yml
└── README.md


🏗 Detalhes das Roles
webserver/ 🌐

tasks/main.yml → Instala e configura o Nginx

handlers/main.yml → Reinicia serviços quando necessário

templates/index.html.j2 → Template HTML dinâmico

firewall/ 🔥

tasks/main.yml → Configura regras de firewall e abre portas essenciais

users/ 👤

tasks/main.yml → Cria usuários, define senhas e permissões
