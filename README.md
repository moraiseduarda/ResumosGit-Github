# Resumos Git e Github

Repositório para armazenar resumos sobre Git e Github do curso Versionamento de Código com Git e Github da
[DIO - Digital Innovation One](https://www.dio.me/)

## 📑 Documentação

- [Documentação Git](https://git-scm.com/docs/git/pt_BR)
- [Documentação Github](https://docs.github.com/pt)
- [Documentação Markdown](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## 💻 Resumos das aulas

##### Aula 1 - Configurando o Git

Se for usar o git pela primeira vez, primeiro deverá configura-lo, estabelecendo seu nome de usuário e endereço de email, já que esta informação será usada de maneira inalterável nos “commits” que enviar.

| Comando                                            | Objetivo            | Descrição                                            |
| -------------------------------------------------- | ------------------- | ---------------------------------------------------- |
| ` git config --global user.name "Nome do usuário"` | Configurar username | Configura o nome de usuário, nesse caso, globalmente |
| `git config --global user.email "seu@email.com"`   | Configurar email    | Configura e-mail, nesse caso, como variável global   |

Será usado como a "assinatura" de todos os commits.

##### Aula 2 - Gravando alterações no repositório local

+++ Resumo branch

| Comando                                                        | Objetivo                        | Descrição                                                                                 |
| -------------------------------------------------------------- | ------------------------------- | ----------------------------------------------------------------------------------------- |
| `git status`                                                   | Verificar o status              | Mostra as alterações no diretório de trabalho e na área de staging (a área de preparação) |
| `git init`                                                     | Iniciar repositório             | Inicia um novo repositório em um diretório                                                |
| `git add nome_do_arquivo`                                      | Adicionar arquivo para rastrear | Adiciona apenas o arquivo mencionado ao rastreio do Git                                   |
| `git add .`                                                    | Adicionar arquivo para rastrear | Adiciona todos os arquivos ao rastreio do Git                                             |
| `git commit -m "Mensagem descritiva do commit"`                | Confirmar os arquivos           | Confirma os arquivos rastreados com um breve nome que descreva as alterações feitas       |
| `git log`                                                      | Exibir commits                  | Exibe histórico de commits                                                                |
| `git clone [url]`                                              | Clonar repositório              | Clona um repositório existente                                                            |
| `git remote`                                                   | Exibir repositório remoto       | Exibe o diretório remoto                                                                  |
| `git pull`                                                     | Baixar conteúdo remoto          | Baixa o conteúdo do repositório remoto, atualizando automaticamente o repositório local.  |
| `git push`                                                     | Enviar conteúdo local           | Envia o conteúdo do repositório local, atualizando automaticamente o repositório remoto.  |
| `git remote add origem https://github.com/username/origem.git` | Adicionar repositório remoto    | Adiciona um repositório remoto ao repositório local                                       |

##### Aula 3 - Desfazendo alterações no repositório local

| Comando               | Objetivo        | Descrição                                                                              |
| --------------------- | --------------- | -------------------------------------------------------------------------------------- |
| `git rm arquivo1.txt` | Remover arquivo | Remove arquivos do seu diretório de trabalho e prepara a remoção para o próximo commit |
