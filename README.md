# Ansible Playbook: aws-proxy

Playbook which creates and configures proxy server in AWS.

It was tested for Amazon Linux 2, but might work for other RHEL based distros
as well.

Originally created by [@dahorak](https://github.com/dahorak)!


# Prerequisites
TODO: document configuration, credentials and required packages

Review `configuration.yml` file and fill/update required options.

Install required collections via ansible-galaxy:
```
ansible-galaxy collection install -r required-collections.yml
```

# Deploy EC2 instance and install and configure proxy server
```
ansible-playbook playbook.yml -e "_action=create"
```

# Install and configure proxy server on existing VM

Create ansible inventory file with `proxy_server` group containing the VM.

```
ansible-playbook playbook.yml -i inventory.yml
```

# Destroy EC2 instance and related resources (created by this playbook)
```
ansible-playbook playbook.yml -e "_action=destroy"
```
