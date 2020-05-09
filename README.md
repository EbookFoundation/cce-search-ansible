# CCE Search Ansible Setup

## Frontend Server (cce.ebookfoundation.org)

### Pre-requisites
1. Install `ansible` on your local machine
2. Ensure you have obtained the SSH key for the server 
3. Complete server setup if not already complete (see CCE-Frontend-System-Information-and-Provisioning-Guide.pdf)

### Updating and redeploying

Once new changes have been added to the master branch of the [frontend repo](https://github.com/EbookFoundation/cce-search-prototype), run the `update-frontend-prod` playbook:
```
$ ansible-playbook -i hosts update-frontend-prod.yml --key-file="/path/to/key/on/your/machine"
```