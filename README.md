# ansible-playbook-aws

## Requirements
- ansible >= 2.3 (`pip install git+git://github.com/ansible/ansible.git@stable-2.3`)

## Setup

### Set org_id
Keep it lowercase.
- `./run`

```yml
---

# SSH
# Min Length: 14, 1 Uppercase, 1 Lowercase, 1 Number, 1 Special Char
ssh_default_password: 'P4ssw0rd!01234'
```

3. Encrypt secrets. `ansible-vault encrypt group_vars/all/secrets.yml --vault-password-file ~/.vault_password_{{ org_id }}`

## Run
`./run`

## 2. Bastion Host
- [x] Deploy EC2 instance
- [x] Setup bastion host
- [x] Setup Security Groups (SSH)
- [x] role to add public keys to servers
- [-] Docs for google-authenticator
- [-] Docs for multi-plexing through bastion and setting up OTP

## 3. Servers
- [x] Security groups
- [x] deploy Web Server + LB
- [x] deploy DB
- [x] harden Web Server
- [x] docker Web Server
- [ ] create users & tables DB
