# Contribuindo

Você pode contribuir com o projeto de diversas formas: adicionando uma feature, corrigindo um bug, refatorando código... Mas como você pode fazer isso? Basta seguir esta página da Wiki.

- [Como contribuir?](#como-contribuir)
  - [Fazendo fork e clonando](#fazendo-fork-e-clonando)
  - [Fazendo alterações](#fazendo-alterações)
- [Padrões e convenções](#padrões-e-convenções)
  - [Workflow](#workflow)
  - [Commits](#commits)
  - [Branches](#branches)

---

## Como contribuir?

### Fazendo fork e clonando
Para contribuir você deve fazer um fork do [repositório do projeto](#). Depois de fazer o fork, basta clonar com `git`.

<!-- tabs:start -->

#### **HTTP**

Utilizando HTTP para clonar o repositório.

```bash
git clone https://github.com/seu-usuario/seu-fork.git
cd seu-fork
```

#### **SSH**

Utilizando SSH para clonar o repositório.

```
git clone git@github.com:seu-user/seu-fork.git
cd seu-fork
```

<!-- tabs:end -->

> [!NOTE]
> Os links para clonar o repositório, tanto `SSH` quanto `HTTP`, podem ser adquiridos clicando no botão verde escrito `Code` no repositório do seu fork.

### Fazendo alterações

Você pode realizar altearação, adicionando features, resolvendo bugs, refatorando código, entre outros. Para fazer alterações no projeto, sempre crie uma branch nova. Nunca faça alterações diretamente na branch `main` ou `develop`.

Para criar uma branch, basta utilizar o seguinte comando:

```bash
git checkout -b nome-da-branch # Cria a branch e seleciona ela automaticamente
# ou
git branch nome-da-branch
git checkout nome-da-branch
```

Depois de fazer commit das alterações, você pode publicar sua branch.

```bash
git push orign nome-da-branch
```

Assim a sua branch vai ser criada no repositório remoto, possibilitando que você faça PR (Pull Request).

---

## Padrões e convenções

Os padrões aqui definidos, devem ser seguidos (até rimou).

### Workflow

Nesse projeto será utilizado o [Gitflow](https://github.com/JuniorLima22/padroes-e-nomenclaturas-no-git?tab=readme-ov-file#gitflow), que consiste nas seguintes branches:

- `main`: A branch principal, a qual contém as versões finais produzidas.
- `develop`: Branch de desenvolvimento.
- `feat`: Branch de desenvolvimento de feature.
- `fix`: Branch de hotfix.

O processo consiste em realizar um fork da branch `main` para `develop`. Para adicionar features, deve-se fazer fork (ou criar uma nova) da branch develop para uma branch `feat`. Depois de finalizar a nova feature, publicar a branch de feature e abrir PR para a branch `develop`.

> [!ATTENTION]
> Antes de publicar a branch de feature, atualize a branch `develop` local, e faça merge na sua branch de feature. Caso tenha algum conflito, resolva localmente. Caso seja aberta PR, e contenha algum conflito, a mesma será negada.

### Commits

Para os commits iremos aplicar [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/). Que consiste em adicionar um prefixo aos commits. Seriam esses:

- `fix`: Ao resolver alguma falha ou bug.
- `feat`: Ao adicionar uma nova funcionalidade.
- `refactor`: Ao reestruturar códigos, mas sem mudar/adicionar funcionalidade.
- `docs`: Ao alterar documentação.

Os commits deve ser feitos com mensagens curtas, claras, e objetivas. Tente sempre respeitar o limite de 50 caracteres, ultrapasse esse limite apenas quando necessário.

#### Exemplo

Vamos supor que eu adicionei a movimentação do player, e agora eu quero fazer um cmmit com essas alterações. Esse padrão eu deveria seguir:

```bash
git commit -m "feat:add player moviment"
```

Ficou bem claro sobre o que se trata esse commit. Porém, as vezes pode ser necessário adicionar uma descrição para melhorar o entendimento.

```bash
git commit -m "feat:add player moviment" -m "Create player movimentation script"
```

Agora meu commit tem um título (`feat:add player moviment`) e uma descrição (`Create player movimentation script`).

### Branches

As branches devem ser nomedas levando em conta o mesmo conceito de Conventional Commits. Utilize nomes curtos e descritivos, contendo um prefixo baseado na alteração. Por exemplo:

```bash
git checkout -b feat/add-player-moviment
```

Dessa forma, quando os manteiners forem verificar a PR, fica bem claro do que aquela branch se refere.