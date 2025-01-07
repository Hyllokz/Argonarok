
# Argonarok

A handmade classic MMORPG server


## Documentação

[Arquivo de sugestões](https://docs.google.com/document/d/1_G3Tp0AwD97i4ozIHX2gTTzPvQJ5SrKtZo-SMoI5Vzg/edit?tab=t.0)

## Instalando o Git e clonando o repositório
• Baixe e instale o [Git](https://git-scm.com/downloads)

• Abra o `cmd` e digite `git --version` para se certificar que o Git foi instalado, em seguida feche o cmd

• Em seu PC, navegue até uma pasta de sua preferência para baixar o código-fonte do servidor, em seguida, clique com o botão direito em uma área limpa da pasta e vá até a opção `Abrir Prompt de Comando aqui/Abrir PowerShell`

• Com o terminal aberto, digite `git clone https://github.com/Hyllokz/Argonarok` e pressione Enter — esse procedimento irá baixar os arquivos na pasta escolhida

• Iremos editar diversos tipos de arquivo, para isso, recomendo a instalação do [Notepad++](https://notepad-plus-plus.org/)

## Conhecendo os diretórios e arquivos

• Dentro da pasta do código-fonte, temos vários diretórios e arquivos que iremos utilizar para as edições, sendo eles:

### Banco de Dados
`db\re` - Banco de dados, onde ficam os arquivos contendo as informações sobre itens, mobs, skills, árvore de skills, entre outros. A linguagem aqui é `yaml`

### O arquivo que mais utilizaremos nessa pasta é `skill_db.yml`
Ele é contém as informações de cooldown, requisitos de item para skill, custos de HP/SP/Zeny
###
### Código-fonte
`src\map` - Local onde ficam os arquivos contendo o código-fonte, aqui teremos as fórmulas. A linguagem aqui é `C++`

### Arquivos e suas funções

• battle.cpp - um dos principais arquivos, contém fórmulas de skill

• skill.cpp - outro arquivo importante contendo fórmulas

• skill.hpp - arquivo de referência para pegar nome interno das skills

• status.cpp - arquivo contendo todos os buffs/debuffs/mudanças de status, aqui os prefixos começam com `SC_`, que significa `status_change`

• pc.cpp - arquivo contendo outras fórmulas

### Como saber qual arquivo editar?
O Notepad++ tem uma função de busca de termos em todos arquivos de determinado diretório, isso ajuda a encontrar todas as incidências de certa skill nos arquivos.
Para isso, utilize o atalho `Ctrl+F`, na aba `Localizar nos arquivos`, insira o termo desejado na caixa de texto `Localizar:` e escolha a pasta `Argonarok\src\map` na opção `Pasta:`

### Qual termo devo pesquisar?
Não existe fórmula mágica, mas vamos ver dois exemplos que podem ajudar:

• Exemplo 1: modificar a skill `Magnum Break` de `Swordsman`
    
Pesquise o nome da skill no [RateMyServer](https://ratemyserver.net/), ele irá retornar o **Name**, **AegisName** e **ID**.

`Sendo eles, respectivamente: Magnum Break, SM_MAGNUM, 7;`

O que nos interessa é quase sempre o **AegisName**, `SM_MAGNUM`

Tendo essa informação, use o `Ctrl+F` para localizar o termo na pasta `src\map` e analise as incidências.
###
• Exemplo 2: modificar a skill `Endure` de `Swordsman`
    
Pesquise o nome da skill no [RateMyServer](https://ratemyserver.net/), ele irá retornar o **Name**, **AegisName** e **ID**.

`Sendo eles, respectivamente: Endure, SM_ENDURE, 8;`

O que nos interessa é quase sempre o **AegisName**, `SM_ENDURE`
Porém, note que `SM_ENDURE` é um buff que provoca uma mudança de status, então devemos considerar mudar o prefixo da busca para `SC_ENDURE`, já que se trata de um `status_change`
Tendo essa informação, vá até o arquivo `src\map\status.cpp` e localize as incidências de `SC_ENDURE`
###

# Boas práticas de programação

Boas práticas de programação são um conjunto de convenções que ajudam a tornar o código de computador mais legível e eficiente, facilitando a manutenção e a colaboração entre programadores. 

Algumas boas práticas de programação são:

    Escrever código limpo e legível: O código deve ser compreensível por outros desenvolvedores e por você mesmo no futuro. 
    Não apagar conteúdo: Ao realizar uma modificação, comente o trecho do código original, para mantermos uma referência
    Identificar sua modificação: Ao início de seu código, faça um comentário dizendo seu nome e o que o trecho abaixo deverá fazer

# Utilizando o Git para baixar e enviar as modificações

### Sempre antes de iniciar modificações no código, é uma boa prática realizar um `git pull`

Para baixar atualizações do Git, pode usar o comando git pull: 

    Abra o terminal ou Prompt de Comandos e navegue até à pasta do projeto
    Use o comando git pull 

Para enviar atualizações do Git, pode seguir os seguintes passos: 

    Garantir que as alterações no código estão salvas no ambiente de desenvolvimento local
    Abrir o terminal ou Prompt de Comandos e navegar até à pasta do projeto
    Executar os seguintes comandos do Git:
        git add . Adiciona todas as alterações feitas no projeto para a área de preparação do Git
        git commit -m "mensagem de commit": Cria um novo commit com todas as alterações que adicionou à área de preparação
        git push: Envia todos os novos commits para o GitHub
## Autores

- [@Hyllokz](https://github.com/Hyllokz)


## FAQ

#### What is Argonarok?

A highly customized classic MMORPG server, mixing original and legacy content

#### For whom Argonarok is?

Argonarok was designed for everybody who likes a classic style MMORPG gameplay experience, classes based, level and skill progression

![Logo](https://i.imgur.com/08n24cg.png)


## 🔗 Links
[![portfolio](https://i.imgur.com/RQKbdq3.png)](https://argonarok.fun/)Download it now!

