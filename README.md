# CCE Search Ansible Setup

# Frontend Server (cce.ebookfoundation.org)

### Pre-requisites
1. Install `ansible` on your local machine
2. Ensure you have obtained the SSH key for the server 
3. Ensure Python 3.7 and pip3 are installed on the server you wish to deploy to

## Complete Playbooks

### Updating and redeploying

Once new changes have been added to the master branch of the [frontend repo](https://github.com/EbookFoundation/cce-search-prototype), run the `update-frontend-prod` playbook:
```
$ ansible-playbook -i hosts update-frontend-prod.yml --key-file="/path/to/key/on/your/machine"
```

## In-progress Playbooks

### Initial bootstrapping and deployment 

To deploy, run the `setup-frontend-prod` playbook from within the directory containing this repository:
```
$ ansible-playbook -i hosts setup-frontend-prod.yml --key-file="/path/to/key/on/your/machine"
```  

### Manually renewing HTTPS cert
If Certbot does not automatically renew the HTTPS certificate, run the `refresh-frontend-cert` playbook:
```
$ ansible-playbook -i hosts refresh-frontend-cert.yml --key-file="/path/to/key/on/your/machine"
```

### TODO
1. Complete todos from setup-frontend-prod.yml
2. Complete refresh-frontend-cert.yml
3. Automate installation of Python 3.7 and pip3
4. Setup Ansible Vault to handle keys