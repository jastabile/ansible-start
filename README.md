# Test connection
```
ansible google -m ping -i inventory.yaml
```

# Test playbook
```
ansible-playbook -i inventory.yaml playbook.yaml

# increasing the verbosity
ansible-playbook cloudflare.yaml -vvv

# with secrets file
ansible-playbook -i inventory.yaml -e @secrets_file.enc --ask-vault-pass cloudflare.yaml
```


# Encrypt secrets
```
ansible-vault encrypt secrets_file.enc
```