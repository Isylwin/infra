# infra

# Prerequisites
- Python3
- Git

`sudo apt install python3 git`

# Run

Run once to install ansible:
`sudo ./bootstrap_ubuntu.sh`

Run once to install dependencies:
`ansible-galaxy install -r requirements.yml`

Run idempotently:
`ansible-playbook playbook.yml -e '@vars.vault.yml' --vault-password-file=vault.txt`

See (Setup Vault)[Setup Vault]

Alternatively you could add passwordless sudo to your current user and just run:
`ansible-playbook playbook.yml`

## Setup vault

Create:
`ansible-vault create vars.vault.yml`

Edit:
`ansible-vault edit vars.vault.yml`
`ansible-vault edit vars.vault.yml --vault-password-file=vault.txt`

If desired, you could put the password for the vault in plaintext in `vault.txt`
