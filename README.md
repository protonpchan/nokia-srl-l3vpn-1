### How to run ansible-runbook as a docker container
```
alias ansible-playbook='docker run --rm -it \
  -v $(pwd):/ansible \
  -v ~/.ssh:/root/.ssh \
  -v /etc/hosts:/etc/hosts \
  ghcr.io/nokia/srlinux-ansible-collection/2.15.5/py3.11:v0.3.0 \
  ansible-playbook -i clab-l3evpn/ansible-inventory.yml $@'
```