# Estrutura do Projeto

## Organização das Pastas

| Pasta         | Descrição                                                            |
|---------------|----------------------------------------------------------------------|
| `/scenes`     | Contém todas as cenas do jogo (menus, fases, personagens, etc.).     |
| `/scripts`    | Scripts em GDScript, organizados por função.                         |
| `/assets`     | Recursos como sprites, sons, músicas e fontes.                       |
| `/ui`         | Elementos visuais da interface (HUDs, menus, botões).                |
| `/addons`     | Plugins adicionais instalados na Godot.                              |
| `/resources`  | Configurações personalizadas e recursos reutilizáveis.               |
| `/docs`       | Documentação interna do projeto.                                     |

---

## Padrões e Convenções

- **Scripts:** Nomeados no padrão `kebab-case.gd`. Cada script controla sua própria cena.
- **Cenas:** Hierarquia modular e clara. Evite cenas gigantes.
- **Assets:** Nomes descritivos (`player_idle.png`, `enemy_attack.wav`).

---

## Fluxo de Desenvolvimento

1. **Planejamento** (Design da fase/sistema).
2. **Criação de Cenas** (Estrutura visual).
3. **Desenvolvimento dos Scripts** (Comportamento e lógica).
4. **Testes Locais** (Dentro da Godot).
5. **Revisão em Equipe** (se aplicável).
6. **Commit no GitHub** (Commits pequenos e descritivos).

---

## Boas Práticas Internas

- Use composition ao máximo.
- Evitar “God Objects”. Exemplos:
  - Uma única cena ou script que controla o jogador, inimigos, fases, pontuação, sons, menus… tudo junto.
  - Um script gigante chamado GameManager.gd que se conecta diretamente a todos os elementos do jogo e gerencia suas ações.
- Reaproveitamento através do instanciamento de cenas.
- Separação entre lógica de jogo e lógica de UI.

---

## Materiais de Apoio

- **Conceitos**
  - [Filosofia e Design da Godot [Conceitos]](https://www.youtube.com/watch?v=eTBpKm_rY_w&t=43s)
  - [How You Can Easily Make Your Code Simpler in Godot 4](https://www.youtube.com/watch?v=74y6zWZfQKk&t=117s)
  - [Linguagens de programação suportadas pela Godot [Conceitos]](https://www.youtube.com/watch?v=x09ISzjw-UM)

- **Melhorar o editor de código**
  - [Godot: Como deixar seu código melhor [Tutorial em Português]](https://www.youtube.com/watch?v=Beg-_bV8VWk)