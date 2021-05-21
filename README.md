# dot

Meus arquivos de configurações, carinhosamente chamados de `dotfiles`

## Como

Cria um repo bare em minha `home` 
```
  git init --bare $HOME/.dot
 ```
 
Adiciono um alias no arquivo de configuração do shell

```
alias config='/usr/bin/git --git-dir=$HOME/.dot/ --work-tree=$HOME'

```

Digo que para esse repositório não é para mostrar arquivos não trackedos.
```
config config status.showUntrackedFiles no
```

Feio isso é só seguir o fluxo, como qualquer outro projeto git.
```
config status
config add .vimrc
config commit -m "feat: adiciona configurações do vim"
config push

```

## Referências
- https://wiki.archlinux.org/title/Dotfiles
- https://news.ycombinator.com/item?id=11070797
- https://wiki.archlinux.org/title/Git#Filtering_confidential_information
