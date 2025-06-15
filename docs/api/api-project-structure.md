# Estrutura do Projeto

---

## Módulos Principais

### `controllers/`

Responsável pelos controladores e endpoints da API.

- `auth.py` - Define as rotas de login e registro.
- `npcs` - Controlador responsável por definir os endpoits da API de NPCs.
- `users.py` - Controlador responsável por definir os endpoints da API de usuários.

### `database/`

Responsável por efetuar a conexão com o banco de dados.

### `services/`

Responsável por conter as regras de negócios da aplicação.

- `users.py` - Lógica de negócios de usuário.
- `npcs.py` - Lógica de negócios de NPCs.
- `roles.py` - Lógica de negócios dos cargos de usuários.

### `models/`

Modelos que representam os dados.

- `character.py` - Modelo que representa um personagem.
- `npc.py` - Modelo que representa um NPC.
- `progress.` - Modelo que representa o progresso de um usuário.
- `user.py` - Modelo que representa um usuário.

### `dto/`

Data Transfer Objects - validação e tipagem de entrada/saída.

### `middleware/`

Middlewares customizados.

- `authentication` - Responsável por realizar a autenticação do usuário.

### `types/`

Tipagens e interfaces reutilizáveis.

- `role_names.py` - Enumerator que contém as definições de cargos de usuário.