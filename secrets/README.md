# System Secrets

This handles the automatic upgrade creation of secrets? Still trying to figure out how it works. This page will eventually have steps to Setup

1. Install kubeseal and yq
  ```
  wget https://github.com/bitnami-labs/sealed-secrets/releases/download/v0.12.4/kubeseal-linux-amd64 -O kubeseal
  sudo install -m 755 kubeseal /usr/local/bin/kubeseal

  sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CC86BB64
  sudo add-apt-repository ppa:rmescandon/yq
  sudo apt update
  sudo apt install yq -y
  ```
2. Put all secrets into .secrets.env file, use the sample as an example

3. Grab pub-cert

4. Run ``./secrets.sh`
    - This will create a file `zz_generated_secrets.yaml` in the cluster folder. This file is encrypted and can be uploaded to github
