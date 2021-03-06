# Contribuição

### Política de Branches

| Data       | Versão | Descrição                                           | Autor              |
| ---------- | ------ | --------------------------------------------------- | ------------------ |
| 13/03/2021 | 1.0    | Criação do documento                                |    Felipe Campos   |
| 23/03/2021 | 1.1    | Adicionando politica de pull request                |    Lucas Machado   |


#### *main*

A branch *main* é a branch de produção, onde ficará a versão estável do projeto. Ela estará bloqueada para commits e para pushs.

#### *devel*

A branch *devel* é a branch de desenvolvimento, onde o trabalho das outras branchs será unificado e onde será criada uma versão estável para mesclar com a *main*.
Assim como a *main* ela está bloqueada para commits e pushs.

#### Nome das Branches  

As branchs de desenvolvimento de features serão criadas a partir da branch *devel* com a nomenclatura padrão `x_nome_da_issue`, onde o `x` representa o código de rastreio da issue.

### Política de Commits

Os commits devem ser feitos em português com aprimeira letra maiuscula usando o parâmetro `-s` para indicar sua assinatura no commit.

```
git commit -s
```

A issue em questão deve ser citada no commit, para isso, basta adicionar `#<numero_da_issue>`.

```
 #5 Fazendo guia de contribuição
```

**Por padrão, o caracter `#` define uma linha de comentário no arquivo da mensagem do commit. Para resolver este problema, use o commando:**

```
git config --local core.commentChar '!'
```

Igualmente, para commits em dupla deve ser usado o comando `-s` , e deve ser adicionado a assinatura da sua dupla.

```
git commit -s
```

Comentário do commit:

```
#5 Fazendo guia de contribuição

Signed-off-by: John Winston Ono Lennon <jwolennon@gmail.com>
Signed-off-by: James Paul McCartney <jpaulm@gmail.com>
```

Para que ambos envolvidos no commit sejam incluidos como contribuintes no gráfico de commits do GitHub, basta incluir a instrução `Co-authored-by:` na mensagem:

```
#5 Fazendo guia de contribuição

Signed-off-by: John Winston Ono Lennon <jwolennon@gmail.com>
Signed-off-by: James Paul McCartney <jpaulm@gmail.com>

Co-authored-by: John Winston Ono Lennon <jwolennon@gmail.com>
Co-authored-by: James Paul McCartney <jpaulm@gmail.com>

```

Para commits que encerram a resolução de uma issue, deve-se iniciar a mensagem do commit com `Fix #<numero_da_issue> <mensagem>`, para que a issue seja [encerrada automaticamente](https://help.github.com/articles/closing-issues-using-keywords/) quando mesclada na `main`.

Exemplo de comentário do commit:

```
Fix #5 Finalizando guia de contribuição do projeto
```

Para commits que incluem uma pequena mudança em uma issue que já teve sua resolução encerrada, deve-se iniciar a mensagem do commit com `HOTFIX #<numero_da_issue> <mensagem>`

Exemplo de comentário do commit:

```
HOTFIX #5 Atualizando guia de contribuição do projeto
```

### Política de Pull Request (PR)

- O titulo do pull request deve estar claro.

- O comentario deve estar claro

- O Pull Request deve referenciar a issue que esta relacionada.

- Utilize o [template](../../.github/PULL_REQUEST_TEMPLATE.md) para realizar o Pull Request