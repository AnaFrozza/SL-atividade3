# Git Assignment

## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo


1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
  - git branch: mostra todas as branches do repositorio
  - git checkout feature-foo: indo para a branch feature-foo
  - git log --decorate: mostra o historico dos ultimos commits com autor e data 

```

2. Tente usar `git log --graph --all`. O que acontece?
```
  - git log --graph --all: mostra os commits das banches e sua representação grafica 
  de como estão em relação ao ramo principal 

```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
  - O arquivo A.java possui a classe A, na master essa classe não possui o metodo foo
  - O arquivo B.java esta vazio, na master ele possui a classe B

```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
  - git checkout master
  - git merge feature-foo
  
  OBS.: não ocorreu conflito

```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
  - git checkout -b math

```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
  - git status
  - git commit -a -m "commit das mudancas no arquivo B"

```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
  - git merge math
  
  Ocorreu conflito na mesclagem no arquivo B.java

```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
  - git reset --merge

```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
  - Quando existe conflito fica "marcado" no arquivo, oque esta dentro de HEAD, é o código que esta na 
  branch master, e o que esta abaixo de ======= é o código que está sendo inserido da brach math:
  
    <<<<<<< HEAD

	    System.out.println("Hello World")
    =======
	
	    System.out.println("I know math, look:")
	    System.out.println(2+2)
    >>>>>>> math
  
  - Para remover o conflito, basta apagar oque você não quer que pertença a branch bem como as marcações 
  que dizem oque é de cada branch, como o enunciado pede para deixar todas as funções, então só removeremos 
  as marcações:
  
    System.out.println("Hello World")
    System.out.println("I know math, look:")
    System.out.println(2+2)

```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
  - git commit -a -m "arrumando conflito do merge no arquivo B"

```



