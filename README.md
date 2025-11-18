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

| Comando              | Objetivo                                  | Descrição                                                                                                         |
| -------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `git status`         | Verificar o status                        | Mostra as alterações no diretório de trabalho e na área de staging (a área de preparação)                         |
| `git init`           | Iniciar repositório                       | Inicia um novo repositório em um diretório                                                                        |
| `git branch -M main` | Altera nome da branch principal para main | Para garantir a compatibilidade no futuro é recomendado atualizar o nome da branch principal, de master para main |

|
