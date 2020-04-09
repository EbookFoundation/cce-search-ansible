# CCE Search Ansible Setup

## Frontend Server (cce.ebookfoundation.org)

### Pre-requisites
1. Install `ansible` on your local machine
2. Ensure you have obtained the SSH key for the server 
3. Ensure Python 3.7 and pip3 are installed on the server you wish to deploy to

### Deploying
To deploy, run the `setup-frontend-prod` playbook from within the directory containing this repository:
```
$ ansible-playbook -i hosts setup-frontend-prod.yml --key-file="/path/to/key/on/your/machine"
```  

### TODO
1. Complete todos from setup-frontend-prod.yml
2. Complete refresh-frontend-cert.yml
2. Automate installation of Python 3.7 and pip3
3. Create playbook to renew HTTPS cert
4. Setup Ansible Vault to handle keys