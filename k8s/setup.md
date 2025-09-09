
### Generate ssh key
```bash
ssh-keygen -t rsa -b 4096 -m PEM -f ~/.ssh/ansible
```
### Create config secret

```bash
 kubectl -n automation create secret generic semaphore-config --from-file config.json
```

### Create ssh secret

```bash
kubectl -n automation create secret generic semaphore-ssh --from-file ~/.ssh/ansible
```

### Create admin secret
```bash
kubectl apply -f secrets.yaml
```
