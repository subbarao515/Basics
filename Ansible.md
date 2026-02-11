# Ansible Learning Notes

## 1. Introduction
- **What is Ansible?** 
  - [Brief description: Open-source automation tool, agentless, etc.]
- **Why use Ansible?**
  - [Benefits: Simplicity, scalability, etc.]
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

---
*Created: [Date]*
*Last Updated: [Date]*
