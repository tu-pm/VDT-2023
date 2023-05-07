## Ansible hands-on lab

### Install ansible

- Install virtualenv
  ```
  sudo apt install python3-virtualenv
  ```

- Activate virtualenv
  ```
  virtualenv venv && source venv/bin/activate
  ```

- Install ansible inside virtualenv
  ```
  pip install ansible
  ```

- Test ansible installation:
  ```
  ansible --version
  ```

### How to use

This repos contain a playbook to setup and hardening a typical Ubuntu server in three different styles:
1. Using shell commands
2. Using modules
3. Factoring tasks into roles

To execute each playbook, cd to the corresponding directory and run this command:

```
ansible-playbook -i inventory.yaml setup.yaml
```
