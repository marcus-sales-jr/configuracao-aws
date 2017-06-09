Configurando acesso ao AWS Code Commit
---
Observação: Essa configuração funciona apenas para usuários Mac/Linux.

```
cd $HOME/.ssh
ssh-keygen
[here just create the name codecommit_rsa and leave all fields blank *just click enter*]
cat codecommit_rsa.pub
```

Agora precisamos inserir o nosso codecommit_rsa.pub no IAM.

```
touch config
chmod 600 config
```

```
nano config

Host git-codecommit.*.amazonaws.com
  User [YOUR_SSH_KEY_ID_FROM_IAM]
  IdentityFile ~/.ssh/codecommit_rsa
```

Agora vamos testar para verificar se ele funciona.

```
ssh git-codecommit.us-east-1.amazonaws.com
```

Você deveria ver.
---
You have successfully authenticated over SSH. You can use Git to interact with AWS CodeCommit. Interactive shells are not supported.Connection to git-codecommit.us-east-1.amazonaws.com closed by remote host.
