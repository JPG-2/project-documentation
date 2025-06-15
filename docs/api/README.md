# API

Aqui você verá as principais tecnologias utilziadas na API, bem como um explicativo de como foi implementado. Para poder iniciar com o desenvolvimento desta API, veja a página [Getting Started](api/getting-started.md). E antes de fazer qualquer contribuição com o projeto, veja a página [Contributing](api/contributing.md).

---

## Tecnologias utilizada

### Principais Libs

- FastAPI
- Beanie - ODM
- Pydantic
- PyJWT - Geração de token JWT
- bcrypt

### Integrações

A API roda em cima de uma aplicação **FastAPI**. Os dados são armazenados em um banco de dados MongoDB, através de uma ODM (Object Document Model). As ODMs são criadas a partir da biblioteca **Beanie**, e permite manipular os dados dos documentos, e organizar as collections. Tanto FastAPI quanto Beanie utilizam Pydantic como base, o que permite uma integração sólida entre essas libs. Para a geração de tokens JWT, a biblioteca utilizada é a **PyJWT**,o qual é muito compatível com FastAPI. Pare encriptar os dados, está sendo utilizado a lib **bcrypt**.

---

## Sincronização de dados

O cliente envia os dados via requisição HTTP/HTTPS. Toda vez que o progresso do jogador for salvo, todos os dados do usuário serão atualizados. Os dados que poderão ser atualizados são:

- Progresso do jogador
- Achievements
- Badges

Como o objetivo da API é apenas demonstrar status sobre os usuários/jogadores, ela não syncroniza os dados de progresso entre clientes (apesar de salvar alguns dados de progresso), e sim apenas salva os dados gerais de estatísticas de desempenho dos jogadores.

---

## Segurança e Autenticação

O método de autenticação é baseado em JWT, onde o usuário informa o user e a senha, e a API retorna um token de autenticação JWT. Ao criar um usuário, os dados de registro são salvos no banco de dados. A senha de acesso é encriptada com a lib **bcrypt** para aumentar a segurança.