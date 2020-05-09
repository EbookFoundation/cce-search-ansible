# CCE Search Ansible Setup

### Pre-requisites
1. Install `ansible` on your local machine
2. Ensure you have obtained the SSH key for the EC2 instances
3. Provision EC2 instances as needed

## Frontend Server (cce.ebookfoundation.org)

For information on how to provision the EC2 instance, see [CCE-Frontend-System-Information-and-Provisioning-Guide.md](CCE-Frontend-System-Information-and-Provisioning-Guide.md)

### Updating and redeploying

Once new changes have been added to the master branch of the [frontend repo](https://github.com/EbookFoundation/cce-search-prototype), run the `update-frontend-prod` playbook:
```
$ ansible-playbook -i hosts update-frontend-prod.yml --key-file="/path/to/key/on/your/machine"
```

## Backend Server (ec2-18-217-39-134.us-east-2.compute.amazonaws.com)