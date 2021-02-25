# ansible-playbook-grafana-kiosk

I use this playbook to set up a Grafana Kiosk on a Headless Raspberry Pi.

This playbook performs the following tasks:

- Uploads **my** ssh keys to the host (:warning: don't blindly copy this to your machines :smile_cat:)
- Disables password authentication on the host
- Runs [ansible-role-grafana-kiosk](https://github.com/sladkoff/ansible-role-grafana-kiosk):
  - Installs graphical environment (openbox + chromium)
  - Installs [grafana-kiosk](https://github.com/grafana/grafana-kiosk)
  - Autostarts grafana-kiosk on login

## Play :play_or_pause_button: 

```bash
# First run must include --ask-pass
ansible-playbook install-grafana-kiosk -i hosts.yaml --ask-pass
# Consecutive runs
ansible-playbook install-grafana-kiosk -i hosts.yaml
```

