# JPG2 Project

- [Visão Geral](#visão-geral)
- [Requisitos Funcionais](#requisitos-funcionais)
- [Requisitos Não Funcionais](#TODO)
- [Escopo](#TODO)
- [Arquitetura e Design](#TODO)
- [Decisões Técnicas](#TODO)

---

## Visão Geral do Projeto

O JPG2 Project é um jogo educativo desenvolvido para complementar o ensino da disciplina de Direito em uma turma universitária. O projeto surgiu a partir de uma pesquisa conduzida com os alunos e a professora responsável pela matéria, que revelou diversas dificuldades enfrentadas no processo de aprendizagem, especialmente relacionadas ao excesso de termos técnicos, linguagem densa e ausência de exemplos práticos durante as aulas.

Entre os principais desafios identificados pelos alunos estão a velocidade com que o conteúdo é apresentado, a baixa clareza na explicação de conceitos e a dificuldade em acompanhar os temas teóricos sem contextualizações práticas. Com base nesses pontos, o projeto tem como objetivo principal transformar o aprendizado jurídico em uma experiência mais acessível, interativa e envolvente, por meio da simulação de situações reais dentro da mecânica do jogo.

Para isso, o JPG2 Project será desenvolvido utilizando o motor Godot e contará com narrativas interativas, desafios práticos baseados em estudos de caso e uma linguagem acessível. Os conceitos jurídicos serão apresentados dentro de contextos compreensíveis, buscando aliar teoria à prática de maneira fluida e lúdica. O jogo também se propõe a ser uma ferramenta de apoio para os professores, promovendo a discussão e a consolidação do conteúdo em sala de aula.

Além disso, está em análise a implementação de uma API complementar para coleta de dados de desempenho dos usuários, com o intuito de oferecer métricas que auxiliem na avaliação da eficácia do aprendizado por meio da plataforma.

O JPG2 Project, portanto, não busca substituir o ensino tradicional, mas sim ampliá-lo, oferecendo uma alternativa pedagógica criativa que dialogue com as reais necessidades dos alunos e contribua para uma formação mais sólida e engajada.

## Requisitos funcionais

> [!NOTE]
> **\*** Funcionalidades que podem ser impementadas caso a API de desempenho seja acrecentada ao escopo do projeto.

- O jogador deve criar uma conta, onde os dados de progressão e desempenho serão coletadas e armazenadas em um banco de dados. *
- O jogador deve criar um personagem, o qual também servirá como registro de salvamento dos dados de forma local (e possívelmente em nuvem *).
- O jogo deve fornecer feedbacks positivos, negativos, ou em casos específicos, justificativas, com base nas ações e decisões do jogador.
- O jogo terá pontos de salvamento automáticos.
- O jogo deve registrar o desempenho do jogador (acertos, erros, tempo de gameplay).
- O jogo deve registrar as conquistas realizadas pelo jogador, e dar feedback para o mesmo ao desbloqueá-las.
- A API deve receber dados sobre o progresso do jogador. *
- A API deve receber dados de conquistas do jogador. *
- O jogo deve funcionar com mouse e teclado.
- O jogo deve ter controles que o torna compatível com mobile.
- O jogo deve permitir o jogador pausar a gameplay e sair a qualquer momento.
- O jogo deve se manter 100% funcional, mesmo offline.
- O jogo deve permitir o ajuste de volume de SFX.
- É necessário que o jogador esteja autenticado para poder enviar dados para a API.
- O jogador deve poder se movimentar para a esquerda e para a direita, quando estiver em modo de caminhada livre.
- O jogador deve conseguir manipular documentos, utilizando *drag and drop*, quando estiver em modo de resolução de caso. 
- O jogador deve conseguir dialogar com os NPCs.

## Requisitos Não Funcionais

- O jogador deve ter acesso à conteúdos da matéria através da biblioteca em jogo.
- O jogador deve ser exposto a situações que exigem tomadas de decisões, que tenha relação com a matéria/conteúdo.
- Os conceitos apresentados devem ser contextualizado através de exemplos ou situações práticas.
- O jogo deve conter um breve tutorial introdutório.
- O jogo deve conter tarefas a serem realizados pelo jogador, de forma coerente com a matéria.
- O desenvolvimento do jogo deve ser baseado em componentização.
- O jogo deve ser compatível com o browser no PC (Chrome, Opera, Brave, Firefox...).
- O jogo deve ser compatível com Android.

## Escopo

### Incluso

- Desenvolvimento de um jogo educativo focado no ensino de Direito para alunos universitários.
- Implementação de 3 fases, sendo elas: estagiário, advogado e juiz. Nas fases de advogado e juiz, serão divididos 6 casos entre eles.
- Implementação de tarefas relacionadas com estágio na área.
- Feedback imediato ao jogador, explicando ações positivas e negativas com base nos conceitos trabalhados.
- Condeúdo disponível para estudo em uma biblioteca dentro do jogo. Essa biblioteca contém explicações de termos juridicos e conceitos da diciplina.
- Sistema de salvamento automático de progresso.
- Diálogo com NPCs.
- Sistema de confiança baseado nas ações e decisões do jogador.

### Fora do Escopo (na fase atual)

- API de métricas de desempenho e progressão dos alunos.

## Visão Geral do Sistema

Este é um jogo educativo voltado para estudantes de Direito, com foco na disciplina de Fundamentos e Aplicação do Direito. A proposta é transformar conceitos jurídicos abstratos em experiências práticas e interativas, utilizando casos reais como base. Mediante decisões complexas e dilemas morais, o jogador é desafiado a aplicar o conhecimento aprendido em sala de aula. A jogabilidade é inspirada em Papers Please (jogo), misturando análise crítica, interpretação legal e tomada de decisão sob pressão, tudo em um ambiente envolvente que simula o cotidiano jurídico.

### Plataforma Alvo

- PC e Mobile.

### Requisitos Mínimos de Hardware

- **PC**: Compatibilidade com browser (Chrome, Opera, Brave, Firefox...).

## Arquitetura do Sistema

### Módulos Principais

- **Motor Gráfico**: Godot.
- **Física**: Godot Physics 2D.

## Tecnologias Utilizadas

- **Linguagem de Programação**: GDScript/C#/C++.
- **Ferramentas de Desenvolvimento**: Git, GitHub, ClickUp, Visual Studio Code/Codium, Aseprite.

## Fluxo de Trabalho

- **Versionamento**: Git com repositório no GitHub.
- **CI**: GitHub Actions para CI/CD.

## Desafios Técnicos

### Problemas Conhecidos

- Grande quantidade de elementos visuais (sprites/texturas/objetos) em cena podem impactar o desempenho do browser.

### Propostas de Soluções

- Renderizar apenas os elementos visuais que estão sendo captados pela câmera do jogador. Os demais elementos podem permanecer ocultos.

## Integração de Assets

- **Formato de Arquivos**: PNG, APNG, MP3, WAV.
- **Ferramentas de Autores**: Aseprite, Audacity, BeepBox.