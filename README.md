
## Run playbook
```bash
ansible-playbook dev_env_setup.yml --ask-become-pass
```

On `BECOME password:` provide root password

# Additional setup steps
## Set up SSH signing key
GitHub documentation on [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux#generating-a-new-ssh-key)
GitHub documentation on [Adding a new SSH key to your account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=cli#adding-a-new-ssh-key-to-your-account)
```bash
ssh-keygen -t ed25519 -C ""
gh ssh-key add ~/.ssh/id_ed25519.pub --type signing --title ""
git config --global user.signingkey ~/.ssh/id_ed25519.pub
```

## Set up git user
```bash
git config --global user.name ""
git config --global user.email ""
```