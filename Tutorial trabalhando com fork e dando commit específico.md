# Trabalhando com uma fork do BIPES e contribuindo com o BIPES/BIPES (master)

Primeiramente, é necessário incluir  o source do BIPES/BIPES como upstream

``` 
git remote add upstream git@github.com:BIPES/BIPES.git
```

Então se pode listar as *branches* dispníveis

```
git fetch upstream
```

E para importar do BIPES/BIPES (master) (Fetch upstream)

```
git fetch upstream master
```

Após isso poderá dar conflitos e não dar merge automático, então uma ferramente de resolução de conflitos como o `meld` é utilizada.

```
git mergetool 
```

Que irá percorrer todos os documentos conflitantes para que se possa chegar em uma versão sem conflitos.



# Contribuindo com o BIPES/BIPES (master) com commits específicos

Atualizar o código tando do master quando upstream

```
git fetch --all
```

Criação da branch que irá receber somente os commmits desejados, cópia do `BIPES/BIPES`

```
git checkout -b BIPES-blocos-pluv upstream/master
```

Selecionar os commits desejados do `pete-br/BIPES`.

```
git cherry-pick CODIGO_AQUI 
```

Então envia para o `remote`.

```
git push -u origin BIPES-blocos-pluv
```

Depois disso basta abrir pull request da branch para o target, como `BIPES/BIPES`


