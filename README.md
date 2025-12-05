# Resumos Git e Github

Repositório para armazenar resumos sobre Git e Github do curso Versionamento de Código com Git e Github da
[DIO - Digital Innovation One](https://www.dio.me/)

## 📑 Documentação

- [Documentação Git](https://git-scm.com/docs/git/pt_BR)
- [Documentação Github](https://docs.github.com/pt)
- [Documentação Markdown](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## 💻 Resumos das aulas

### Aula 1 - Configurando o Git

Se for usar o git pela primeira vez, primeiro deverá configura-lo, estabelecendo seu nome de usuário e endereço de email, já que esta informação será usada de maneira inalterável nos “commits” que enviar.

| Comando                                           | Objetivo            | Descrição                                            |
| ------------------------------------------------- | ------------------- | ---------------------------------------------------- |
| `git config --global user.name "Nome do usuário"` | Configurar username | Configura o nome de usuário, nesse caso, globalmente |
| `git config --global user.email "seu@email.com"`  | Configurar email    | Configura e-mail, nesse caso, como variável global   |

Será usado como a "assinatura" de todos os commits.

### Aula 2 - Gravando alterações no repositório local

| Comando                                                        | Objetivo                        | Descrição                                                                                 |
| -------------------------------------------------------------- | ------------------------------- | ----------------------------------------------------------------------------------------- |
| `git status`                                                   | Verificar o status              | Mostra as alterações no diretório de trabalho e na área de staging (a área de preparação) |
| `git init`                                                     | Iniciar repositório             | Inicia um novo repositório em um diretório                                                |
| `git add nome_do_arquivo`                                      | Adicionar arquivo para rastrear | Adiciona apenas o arquivo mencionado ao rastreio do Git                                   |
| `git add .`                                                    | Adicionar arquivo para rastrear | Adiciona todos os arquivos ao rastreio do Git                                             |
| `git commit -m "Mensagem descritiva do commit"`                | Confirmar os arquivos           | Confirma os arquivos rastreados com um breve nome que descreva as alterações feitas       |
| `git log`                                                      | Exibir commits                  | Exibe histórico de commits                                                                |
| `git reflog`                                                   | Exibir alterações feitas        | Exibe histórico de alterações feitas no repositório local                                 |
| `git clone [url]`                                              | Clonar repositório              | Clona um repositório existente                                                            |
| `git remote`                                                   | Exibir repositório remoto       | Exibe o diretório remoto                                                                  |
| `git pull`                                                     | Baixar conteúdo remoto          | Baixa o conteúdo do repositório remoto, atualizando automaticamente o repositório local.  |
| `git push`                                                     | Enviar conteúdo local           | Envia o conteúdo do repositório local, atualizando automaticamente o repositório remoto.  |
| `git remote add origem https://github.com/username/origem.git` | Adicionar repositório remoto    | Adiciona um repositório remoto ao repositório local                                       |

### Aula 3 - Desfazendo alterações no repositório local

É importante desfazer as alterações localmente ao invés de forçar o commit com algum erro pois isso pode gerar problemas ao trabalhar em conjunto.

| Comando                            | Objetivo                           | Descrição                                                                                                           |
| ---------------------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `rm -rf .git`                      | Remover versionamento de uma pasta | Remove o versionamento caso tenha dado git init na pasta errada                                                     |
| `git rm arquivo1.txt`              | Remover arquivo                    | Remove arquivos do seu diretório de trabalho e prepara a remoção para o próximo commit                              |
| `git reset diretorio/arquivo1.txt` | Remover arquivo                    | Remove arquivos do seu diretório                                                                                    |
| `git restore arquivo1.txt`         | Restaurar arquivo                  | Restaura o arquivo para o ultimo commit                                                                             |
| `git commit --amend -m"mensagem"`  | Renomear último commit             | Possibilita editar a mensagem escrita no último commit                                                              |
| `git reset --soft hash-do-commit`  | Desfazer último commit             | Desfaz o commit informado mantendo os arquivos dos commits posteriores na área de preparação                        |
| `git reset --mixed hash-do-commit` | Desfazer último commit             | Desfaz o commit informado mantendo os arquivos dos commits posteriores na área de trabalho, não restreados pelo git |
| `git reset --hard hash-do-commit`  | Desfazer último commit             | Desfaz o commit informado apagando os arquivos dos commits posteriores                                              |

### Aula 4 - Enviando e baixando alterações no repositório remoto

| Comando                                                             | Objetivo                                     | Descrição                                                                 |
| ------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------------- |
| `git remote add origin URL-repositorio-github` `git branch -M main` | Conectar ao repositório remoto               | Conecta o repositório local com o repositório remoto                      |
| `git push -u origin main`                                           | Enviar alterações para o repositório remoto6 | Envia as informações do repositório local para o repositório remoto       |
| `git pull`                                                          | Pegar alterações do repositório remoto       | Puxa as alterações do repositório remoto e mescla com o repositório local |

### Aula 5 - Trabalhando com Branches - Criando, mesclando, deletando e tratando conflitos

Branch -> Ramificação do projeto

- É um ponteiro móvel para um commit no histórico do repositório;
- Quando é criado uma nova Branch a partir de outra existente, a nova se inicia apontando para o mesmo commit da Branch que estava quando foi criada.

| Comando                      | Objetivo               | Descrição                             |
| ---------------------------- | ---------------------- | ------------------------------------- |
| `git checkout -b nomeBranch` | Criar nova Branch      | Cria e troca para a nova Branch       |
| `git checkout nomeBranch`    | Trocar de Branch       | Troca a Branch atual para a informada |
| `git branch -v`              | Listar últimos commits | Lista o último commit de cada Branch  |
