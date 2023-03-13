# Assinatura de commit

### Instalação linux
````sh
sudo apt install gnupg
````
---

### Listar chaves
````sh
gpg --list-secret-keys --keyid-format LONG
````

### Gerar chave
````sh
gpg --full-generate-key
````

### Exportar chave
````sh
gpg --armor --export <chave>
````

---

````sh
export GPG_TTY=$(tty)
````

## Configuração GIT

#### Utilizar essa chave na hora de assinar
````sh
git config --global user.signingKey <chave>
````

#### Assinar por padrão todos os commits
````sh
git config --global commit.gpgSign true
````

#### Assinar por padrão todas tags
````sh
git config --global tag.gpgSign true
````