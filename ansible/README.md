# GitOps workflow for kubernetes cluster

![](https://i.imgur.com/9tvyWMp.png)

Leverage [Flux](https://github.com/fluxcd/flux) to automate cluster state using code residing in this repo

## Setup

See [setup/README.md](setup/README.md) for more details.

## Workloads (by namespace)

* [cert-manager](cert-manager/)
* [default](default/)
* [flux](flux/)
* [kube-system](kube-system/)
* [longhorn-system](longhorn-system/)
* [logs](logs/)
* [monitoring](monitoring/)
* [system-upgrade](system-upgrade/)

## Ansible Sets To Install

Note: Do not use the `--check` option in Ansible, it will fail on the K3S install
Note: Must `sudo chmod a+w /usr/local/bin` for some reason still. Fails on downloading k3s binary if I dont do this

1. Install ansible
   ```
   sudo apt-get install ansible
   ```
2. Create a Github SSH pesonal access token. Follow directions located at [Github](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)
   Paste the key into `nano ~/.secret/github_access_token`
3. Clone github repo to home directory
   ```
   cd ~
   git clone https://github.com/dcplaya/k8s-gitops
   ```
4. Install Ansible Galaxy requirements (Want to add ZSH stuff here once I get this working as is)

   ```
   cd ~/k8s-gitops/ansible
   ansible-galaxy install -r requirements.yml
   ```
5. Set up Ansible vault (applies to only inital installs)
   ```
   ansible-vault encrypt ~/k8s-gitops/ansible/group_vars/vault/encrypted-vault.yml
   ```
   Note: I am not sure what the recovery/root token are for yet.

6. ## To enable SSH key prompt only once (Seems to not survive a reboot?)
   ```
   ssh-agent $SHELL
   ssh-add /home/$USER/.ssh/id_rsa
   ```

7. Run ansible main.yml (-K option is for BECOME password on remote server)
   Note: Must be in ansible directory for ansible to automatically pick up the hosts.yml file
   ```
   cd ~/k8s-gitops/ansible/
   ansible-playbook main.yml -K --private-key=~/.ssh/id_rsa
   ```

   Or, if you do not have SSH keys, a lowercase -k option to set SSH password
   ```
   cd ~/k8s-gitops/ansible/
   ansible-playbook main.yml -k -K
   ```

7. Install for ceph
  `sudo apt-get install -y lvm2`


## To enable SSH key prompt only once (Seems to not survive a reboot?)

1. `ssh-agent $SHELL`
2. `ssh-add /home/$USER/.ssh/id_rsa`
