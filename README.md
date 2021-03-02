# Luci Credential Store


# problem 
- dev secrets are tribal

# solutions
## Ansible Vault
- pros
    - source control with github
- cons
    - potential knowledge gap 
    - encrypted with one key (creates issue when somebody leaves, or for various scopes)

## Hashicorp Vault
- pros
    - way better than tribal knowledge
    - source control with github
- cons
    - cost of running a server
    - potential knowledge gap x2 
    - encrypted with one key (creates issue when somebody leaves, or for various scopes)

aws ssm get-parameter --with-decryption --name myParameter | set-password






# the boring fallback solution
## AWS parameter store just works (tm)
- pros
    - use existing Access control (roles and stuff)
    - keeps history (and blame)
- cons
    - not in github (more commonly known)