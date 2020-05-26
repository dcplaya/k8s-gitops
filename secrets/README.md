# System Secrets

This handles the automatic upgrade creation of secrets? Still trying to figure out how it works. This page will eventually have steps to Setup


1. Put all secrets into .secrets.env file, use the sample as an example
2. Source the secrets file (This is in the script but doesnt work for some reason)
  `. /home/$USER/k8s-gitops/secrets/.secrets.env`
3. Run ./secrets.sh
    - This will create a file `zz_generated_secrets.yaml` in the cluster folder. This file is encrypted and can be uploaded to github
