# Primeiro Pull Request

Este guia explica, de forma simples, como criar e enviar um pull request usando **fork** no GitHub.

## 1. Git e GitHub

Antes de começar, vale entender o papel de cada ferramenta:

- **Git** e a ferramenta que registra as mudancas no codigo.
- **GitHub** e o site onde o repositorio fica hospedado.

Voce vai usar os dois durante o processo.

## 2. Escolha uma issue

O primeiro passo e escolher em que voce vai trabalhar.

Se o projeto usa **issues**, procure uma tarefa aberta e avise nos comentarios que voce vai cuidar dela. Isso evita trabalho duplicado.

Se a sua ideia ainda nao virou uma issue, normalmente voce pode criar uma antes de comecar.

## 3. Faça um fork do repositorio

Depois de escolher a issue, abra o repositorio original no GitHub e clique em **Fork**.

O fork e uma copia do repositorio na sua conta. E nele que voce vai enviar suas alteracoes.

No fim desse processo, voce tera uma URL parecida com esta:

```text
https://github.com/seu-usuario/nome-do-repositorio
```

Neste guia, vamos chamar essa URL de `URL_DO_SEU_FORK`.

## 4. Clone o seu fork

Agora voce precisa baixar o seu fork para o computador.

No terminal, rode:

```bash
git clone URL_DO_SEU_FORK
```

Exemplo:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

Depois entre na pasta criada:

```bash
cd nome-do-repositorio
```

## 5. Faça as alteracoes

Com o repositorio na sua maquina, faca as mudancas necessarias para resolver a issue.

Pode ser codigo, documentacao, correcao de texto, testes ou qualquer outro conteudo relacionado ao que voce escolheu.

Quando terminar, confira o que foi alterado:

```bash
git status
```

## 6. Salve suas mudancas com commit

Agora voce vai registrar suas alteracoes.

Primeiro, adicione os arquivos modificados:

```bash
git add .
```

Depois crie um commit com uma mensagem clara:

```bash
git commit -m "Adiciona documentacao para primeiro pull request"
```

Essa mensagem deve resumir bem o que voce fez.

## 7. Envie as mudancas para o seu fork

Depois do commit, envie as alteracoes para o repositorio remoto do seu fork:

```bash
git push origin master
```

Se o projeto usar `main` em vez de `master`, use:

```bash
git push origin main
```

Se voce estiver trabalhando em outra branch, substitua pelo nome dela.

## 8. Crie o pull request

Com as mudancas ja enviadas para o seu fork, volte ao GitHub.

Abra a pagina do seu fork e clique em **New pull request** ou **Compare & pull request**.

Depois:

1. Confira se o destino e o repositorio original.
2. Confira se a origem e o seu fork.
3. Escreva um titulo claro.
4. Explique o que foi alterado.
5. Clique em **Create pull request**.

Pronto. Agora sua contribuicao foi enviada para revisao.

## 9. Aguarde a revisao

Depois que a pull request for aberta, alguem da equipe pode:

- aprovar a mudanca;
- pedir ajustes;
- comentar pontos para melhoria.

Se pedirem mudancas, basta corrigir no seu repositorio local, fazer novo `commit` e rodar `git push` novamente. A mesma pull request sera atualizada automaticamente.

## Resumo rapido

```bash
git clone URL_DO_SEU_FORK
cd nome-do-repositorio
# faz as alteracoes
git add .
git commit -m "Describe sua alteracao"
git push origin master
```

Depois, abra o GitHub e crie a pull request a partir do seu fork.

## Dicas

- Seja claro nas mensagens de commit.
- Revise seus arquivos antes de enviar.
- Se tiver duvida com Git ou GitHub, peca ajuda.
- Se alterar algo importante, veja se a documentacao tambem precisa ser atualizada.
- Para conteudo textual, prefira arquivos `.md`.
