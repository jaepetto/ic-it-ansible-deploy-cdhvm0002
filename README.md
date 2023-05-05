# cdhvm0002.xaas.epfl.ch automated deployment

This repository contains the Ansible playbooks used to deploy the cdhvm0002.xaas.epfl.ch server.

This machine is used as a jump host to store data used by the IC Cluster. The NFS volume is mounted in order to allow pushing data to the cluster.

## Setup

### Python version

Make sure you are using the python version indicated into the `.tool-versions` file.

### Virtual environment

Create a virtual environment and install the required packages:

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Activate the virtual environment:

```bash
source venv/bin/activate
```

### Ansible dependencies

Install the required Ansible roles:

```bash
ansible-galaxy install -r requirements.yml
```

## Usage

### Deploy

Deploy the server:

```bash
ansible-playbook -i inventory/prod playbook.yml
```
