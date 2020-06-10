Playbook for production hosts
=============================

Install host dependencies [for MacOs only]
------------------------------------------
```bash
brew install gnu-tar
```
Install ansible
---------------
```
brew install ansible
```

Update dependency roles
-----------------------
```bash
cd java-application-monitoring-and-troubleshooting/iaac
ansible-galaxy install -r requirements.yml
```

Reset ssh keys [if target host've changed]
------------------------------------------
```bash
ssh-keygen -R {{ ansible_ssh_host }}
```

Smoke test Ansible connections
------------------------------
```bash
ansible -i inventories/production -m shell -a 'uname -a' all
```

Dry run [if IaaC have changed]
------------------------------
```bash
ansible-playbook site.yml -i inventories/production --check
```

Run playbook against docker test environment hosts inventory
------------------------------------------------------------
```bash
export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES #for MacOSX
ansible-playbook site.yml -i inventories/production
```
