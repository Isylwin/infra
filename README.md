# infra

# Prerequisites
- Python3
- Git

`sudo apt install python3 git`

# Run

Run once to install ansible:
`sudo ./bootstrap_ubuntu.sh`

Run idempotently:
`ansible-playbook playbook.yml --ask-become-pass`

