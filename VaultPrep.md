# Managing secrets

While there are many different approaches to securing sensitive information for use with ansible, the following steps show the approach used for this repository.

## Prepare for automatic run

- Create a location in home path to store vault secrets:

`mkdir ~/.mysec; chmod 700 ~/.mysec`

- Add a secret for the current project vault:

`echo mynewpassword > ~/.mysec/reponame; chmod 600 ~/.mysec/reponame`

- Create an ansible vault file containing sensitive information (eg: ./group_vars/private.yml):

```bash
# Example sensitive data
#./group_vars/private.yml
vault_id:
  first: Jeff
  last: Kelly
  email: jeff.kelly@email.com
  
vault_sshkeyname: "my_special_key"

```

- Encrypt sensitive info file:

`ansible-vault encrypt ./group_vars/private.yml --vault-id `