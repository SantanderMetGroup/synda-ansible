# synda-ansible

Ansible playbook to populate conda environments that will be used for synda downloads at Santander Met Group.

```bash
ansible-galaxy install -r requirements.yml

# You might save the variables in a `vars_files`
# `name` defaults to `dataset|basename`
ansible-playbook main.yml -e name="condaEnvName" -e dataset="/path/to/zfs/mountpoint" -e openid="OPENID" -e password="PASSWORD"
```

A new conda environment has been created for you. Synda is available in the environment and configured to download and create the database in the ZFS dataset.
For info about defaults for the conda environment see https://github.com/uchida/ansible-miniconda-role
