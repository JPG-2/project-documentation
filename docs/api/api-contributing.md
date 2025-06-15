# Contributing

Para poder contribuir com o projeto, siga as orientações abaixo sobre o projeto.

---

## Onde posso ajudar?

Você pode contribuir de várias formas:

- Corrigindo bugs
- Sugerindo melhorias
- Criando novas features
- Melhorando a documentação
- Refatorando código

## Estrutura básica

- `api/controllers/` → define as rotas da API
- `api/services/` → lógica de negócio
- `api/models/` → entidades/dados
- `api/dto/` → validação dos dados
- Veja mais [aqui](api/api-project-structure.md)

## Como contribuir de fato

- Faça um fork do projeto
- Crie uma nova branch com um nome descritivo
```bash
git checkout -b feat/add-new-feature
```
- Faça suas alterações
- Confirme com mensagens claras
```bash
git commit -m "feat: add new login feature with OTP"
```
- Envie para o seu fork
```bash
git push origin feat/add-new-feature
```
- Abra um pull request para a branch `main`

## Regras de código

- Não utilizar wildcard em imports
```py
from library import *
```
- Nomes de funções e variáveis devem ser claros
- Evitar comentários inúteis ou código morto

## Revisão de PR

Seu Pull Request será revisado. Durante a revisão, podemos:

- Sugerir melhorias
- Pedir ajustes