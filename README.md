# ansible-rpi

Ansible resources for setting up my raspberry pi.

## Steps taken (to be removed)

To create role structure

```
ansible-galaxy init rpitv
```

To add `ansible.posix` collection

```
ansible-galaxy collection install ansible.posix
```

### Initial SSH configuration

Initially SSH pubkey authentication is disabled.

Run playbook with:


```
ansible-playbook site.yaml -b -i hosts --ask-pass
```
