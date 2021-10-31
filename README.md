# create_projetc_ansible

```bash
$ tree template_ansible

template_ansible
├── hosts
├── main.yml
├── README.md
└── roles
    └── name_role
        ├── defaults
        │   └── main.yml
        ├── files
        │   └── main.yml
        ├── handlers
        │   └── main.yml
        ├── meta
        │   └── main.yml
        ├── README.md
        ├── tasks
        │   └── main.yml
        ├── templates
        │   └── main.yml
        └── vars
            └── main.yml

9 directories, 11 files

```

### main.yml
### hosts
### roles
### name_role
### defaults

No diretório ``defaults`` é onde estará o valor padrão de todas as variáveis que não seja realmente necessária ser setada por quem está consumindo a role. 

### files
### handlers

No diretório ``handlers`` será usada a configuração dos handlers que ao ser chamado em uma task, será executado conforme sua configuração.

**Docs:** [handlers](https://docs.ansible.com/ansible/latest/user_guide/playbooks_handlers.html)

### meta
### templates
### vars

No diretório ``vars`` é usado para configurar variáveis que serão usadas para organização do que foi implementado na role e evitar repetição dentro do código, o conteúdo dessa pasta não deve ser alterado pelo usuário da role ao baixar a role para uso via playbook.

## ansible-galaxy

Se não quiser criar toda essa estrutura na mão pode usar o ansible-galaxy.

```bash
$ mkdir -vp project_ansible_galaxy/roles
mkdir: foi criado o diretório 'project_ansible_galaxy'
mkdir: foi criado o diretório 'project_ansible_galaxy/roles'
```

```bash
$ cd project_ansible_galaxy/roles

$ ansible-galaxy init apache_vhost
- Role apache_vhost was created successfully
```


```bash
tree .
.
└── apache_vhost
    ├── defaults
    │   └── main.yml
    ├── handlers
    │   └── main.yml
    ├── meta
    │   └── main.yml
    ├── README.md
    ├── tasks
    │   └── main.yml
    ├── tests
    │   ├── inventory
    │   └── test.yml
    └── vars
        └── main.yml

7 directories, 8 files

```
**Source based:** [gomex.me](https://gomex.me/2021/01/18/como-organizar-as-roles-e-playbooks-do-ansible/)
