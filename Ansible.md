# Ansible Learning Notes

## 1. Introduction
- **What is Ansible?** 
  - Ansible is an open-source automation tool used for IT tasks such as configuration management, application deployment, and intraservice orchestration
  - it is agentless, meaning it doesn't require you to install extra software on the systems you're managing; it simply connects via SSH or WinRM.
- **Why use Ansible?**
  - Human-Readable (YAML): You don't need to be a Python pro. If you can read a grocery list, you can read an Ansible Playbook.
  - No Agents: As we discussed, not having to install software on your 500 servers saves massive amounts of time and memory.
  - Idempotency (The "Make it So" Rule): This is a fancy word for a simple concept. If you run an Ansible script twice, it won't break things the second time. It checks the current state: if the file is already there, it does nothing. If it’s missing, it creates it.
- **Architecture**
  - Control Node vs Managed Nodes
  - Inventory
  - Modules
  - Playbooks

## 2. key Concepts
### Inventory
- Definition:
- Static vs Dynamic Inventory:
- Example `hosts` file:
  ```ini
  [webservers]
  web1.example.com
  web2.example.com

  [dbservers]
  db1.example.com
  ```

### Modules
- What are modules?
- Common modules (e.g., `apt`, `yum`, `copy`, `service`, `user`, `ping`)

### Ad-Hoc Commands
- Syntax: `ansible [pattern] -m [module] -a "[arguments]"`
- Examples:
  ```bash
  ansible all -m ping
  ansible webservers -m service -a "name=httpd state=started"
  ```

### Playbooks
- Structure (YAML)
- Keywords (`hosts`, `tasks`, `vars`, `handlers`)
- Example Structure:
  ```yaml
  ---
  - name: Install Apache
    hosts: webservers
    become: yes
    tasks:
      - name: Install httpd package
        yum:
          name: httpd
          state: present
  ```

### Variables
- Defining variables (Playbooks, Inventory, Command line)
- Variable precedence

## 3. Installation & Setup
- **Prerequisites**: [Python, SSH, etc.]
- **Installation Command**:
  ```bash
  # Ubuntu/Debian
  sudo apt update
  sudo apt install ansible

  # RHEL/CentOS
  sudo yum install ansible
  ```
- **Configuration** (`ansible.cfg`)

## 4. Advanced Topics
### Roles
- Directory structure (`tasks`, `handlers`, `vars`, `files`, `templates`, `meta`)
- Creating a role: `ansible-galaxy init <role_name>`

### Handlers
- Triggering actions upon change (e.g., restarting services)

### Templates (Jinja2)
- Using variables in config files
- Loops and Conditionals

### Vault
- Encrypting sensitive data
- Commands: `ansible-vault create`, `ansible-vault edit`, `ansible-vault view`

## 5. Cheat Sheet / Common Commands
| Command | Description |
|Args|Args|
|---|---|
| `ansible --version` | Check Ansible version |
| `ansible-playbook site.yml` | Run a playbook |
| `ansible-galaxy list` | List installed roles |
| `ansible-doc -l` | List available modules |
| `ansible-doc [module]` | Show documentation for a module |

## 6. Practical Eamples / Labs
- **Lab 1: Web Server Setup**
  - [Link to code or brief notes]
- **Lab 2: User Management**
  - [Link to code or brief notes]

## 7. Resources & References
- [Official Documentation](https://docs.ansible.com/)
- [Ansible Galaxy](https://galaxy.ansible.com/)
- [Other useful links]

