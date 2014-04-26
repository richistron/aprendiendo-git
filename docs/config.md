git config
==========

El comando **config** nos sirve para setear especificas configuraciones a git. Muy al estilo de los de 
[POSIX](http://en.wikipedia.org/wiki/POSIX), git usa dotfiles para manejar sus configuraciones locales sin afectar configuraciones del servidor u otros usuarios.

Como se si mi configuración existe
```
cat ~/.gitconfig
```

Configurando tu usuario
=======================


```
git config --global user.name "Ricardo Rivas G."
git config --global user.email "richistron@gmail.com"
```

Ejemplo de configuraciones avanzadas
====================================

[.gitconfig](.gitconfig)

```
[alias]
  c = commit
        aa = add .
  tool = mergetool 
  up = fetch --all --prune
        p = push
        m = merge
        st = status -s
        a = add -i
        d = diff --color --color-words --abbrev
  l = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --
  rt = reset HEAD --hard
  am = commit --amend
  rollback = reset HEAD~10 --hard
        ch = checkout
        b = branch
        find = rev-list -n 1 HEAD
        sub = submodule
        patch = format-patch -1
        r = reset
[color]
  ui = always
[core]
  excludesfile = ~/.gitignore
  attributesfile = ~/.gitattributes
[color "branch"]
  current = yellow reverse
  local = yellow
  remote = green
[color "diff"]
  meta = yellow bold
  frag = magenta bold
  old = red bold
  new = green bold
[color "status"]
  added = yellow
  changed = green
  untracked = cyan
[merge]
  log = true
  tool = vimdiff
[url "git@github.com:"]
  insteadOf = "gh:"
  pushInsteadOf = "github:"
  pushInsteadOf = "git://github.com/"
[url "git://github.com/"]
  insteadOf = "github:"
[url "git@gist.github.com:"]
  insteadOf = "gst:"
  pushInsteadOf = "gist:"
  pushInsteadOf = "git://gist.github.com/"
[url "git://gist.github.com/"]
  insteadOf = "gist:"

# Any GitHub repo with my username should be checked out r/w by default
# http://rentzsch.tumblr.com/post/564806957/public-but-hackable-git-submodules
[url "git@github.com:richistron/"]
  insteadOf = "git://github.com/richistron/"
[user]
  name = Ricardo Rivas G.
  email = richistron@gmail.com
[push]
  default = simple
```

