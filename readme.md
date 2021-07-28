# Estatística Computacional

## Instalação do R Studio
### Pre Requisitos
  -  [Docker](https://docs.docker.com/engine/install)
### Criando o container
```sh
  docker run -d --name rstudio -v $HOME:/home/`whoami` -e PASSWORD=admin -p 80:8787 rocker/tidyverse
```

### Executando o container
```sh
  docker start rstudio
```

## Executar o R Studio
### Abra http://localhost no seu navegador
### Será solicitado usuário e senha:
```
  user: rstudio
  password: admin
```