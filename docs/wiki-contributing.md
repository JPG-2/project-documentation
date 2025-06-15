# Contribuindo com a Wiki

Para contribuir com a Wiki, deixando ela mais atualizada e útil, basta seguir as orientações abaixo.

---

## O que posso contribuir?

Você pode ajudar com:

- Melhorias em páginas já existentes
- Correções ortográficas ou gramaticais
- Explicações mais claras e exemplos práticos
- Criação de novas seções (como guias, tutoriais ou explicações de conceitos)
- Atualizações que acompanham mudanças no código

---

## Organizaçao do diretório da Wiki

As páginas são arquivos .md (Markdown) organizados por tema.

Exemplos:

- `docs/api/project-structure.md`
- `docs/api/api-contributing.md`
- `docs/wiki-contributing.md` (esta página!)

---

# Como editar ou adicionar conteúdo

- Clone o projeto (se ainda não fez):

```bash
git clone https://github.com/seu-usuario/seu-repo.git
```

- Crie uma branch para sua contribuição:

```bash
git checkout -b docs/explicacao-de-auth
```

- Edite ou crie um arquivo `.md` dentro da pasta `docs/`.

- Visualize localmente (opcional, mas recomendado):

Instale o Docsify globalmente (se ainda não tiver):

```bash
npm install -g docsify-cli
```

Rode localmente:

```bash
docsify serve docs
```

- Faça o commit com uma mensagem clara:

```bash
git commit -m "docs: adiciona explicação sobre autenticação JWT"
```

- Abra um Pull Request com sua contribuição.

---

## Boas práticas

- Use títulos e subtítulos (`#`, `##`, `###`) para organizar
- Prefira listas, tabelas e exemplos de código ao invés de blocos gigantes de texto
- Sempre que possível, adicione exemplos de uso
- Mantenha o mesmo estilo e tom das outras páginas

Para ver mais sobre a sintaxe do Markdown, acesse esse [guia](https://markdown.net.br/sintaxe-basica/).

---

## Organização dos arquivos

Organize os arquivos com nomes claros e em diretórios que corresponde ao tema abordado em seu conteúdo. Por exemplo:

|Diretório|Função                                   |
|---      |---                                      |
|`api/`   |Arquivos relacionado com o projeto da API|

Ao criar uma nova página, é necessário adicionar um link para a mesma no arquivo `_sidebar.md` e `navbar.md`.