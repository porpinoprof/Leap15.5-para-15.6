## Fazer Backup de Dados Importantes

Antes de qualquer atualização, faça um backup completo dos seus dados importantes.

## Atualizar Pacotes Existentes

Atualize todos os pacotes existentes para garantir que você esteja começando com a versão mais recente dos pacotes em uso.

Abra um terminal e execute:

```bash
sudo zypper ref
sudo zypper up
```

## Desabilitar Repositórios de Terceiros

Desabilite temporariamente repositórios de terceiros para evitar conflitos durante a atualização.

```bash
sudo zypper modifyrepo --all --disable
```
Adicionar Novos Repositórios

Adicione os repositórios necessários para a nova versão do openSUSE Leap. Para atualizar do Leap 15.5 para o 15.6, os comandos são os seguintes:
```bash
sudo zypper ar -f https://download.opensuse.org/distribution/leap/15.6/repo/oss/ repo-oss-15.6
sudo zypper ar -f https://download.opensuse.org/distribution/leap/15.6/repo/non-oss/ repo-non-oss-15.6
sudo zypper ar -f https://download.opensuse.org/update/leap/15.6/oss/ repo-update-oss-15.6
sudo zypper ar -f https://download.opensuse.org/update/leap/15.6/non-oss/ repo-update-non-oss-15.6
```
## Atualizar o Sistema para a Nova Versão

Execute a atualização para a nova versão com o comando zypper dist-upgrade.
```bash
sudo zypper ref
sudo zypper dist-upgrade
```

## Reativar Repositórios de Terceiros

Depois de completar a atualização, reative os repositórios de terceiros, se necessário. Certifique-se de que esses repositórios sejam compatíveis com a nova versão do openSUSE Leap.

```bash
sudo zypper modifyrepo --all --enable   
```

## Reiniciar o Sistema

Reinicie o sistema para concluir a atualização e aplicar todas as mudanças.
```bash
sudo reboot now
```


