# Docker Kill Last Container Shortcut

Add the following snippet to your .zshrc or .bashrc and then restart your terminal.

```
dk() {    
  IMAGE=$(docker ps | grep '[a-z0-9]' | grep -m 1 '^\w'  )    
  echo `docker kill ${IMAGE%% *}`    
  echo 'docker container above is now dead'    
}    
```

type <code>dk</code> in your command line and it will kill the last started docker container.
