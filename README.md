# ansible-rpi

Ansible resources for setting up my raspberry pi.

## Commands

This example playbook performs the following tasks:

- Uploads
- disable password authentication

```bash
ansible-playbook install-grafana-kiosk -i hosts --ask-pass
```

## Steps taken (to be removed)

To create role structure

```
ansible-galaxy init rpitv
```

To add `ansible.posix` collection

```
ansible-galaxy collection install ansible.posix
ansible-galaxy collection install community.general
```

### Initial SSH configuration

Initially SSH pubkey authentication is disabled.

Run playbook with:


```
ansible-playbook site.yaml -b -i hosts --ask-pass
```
