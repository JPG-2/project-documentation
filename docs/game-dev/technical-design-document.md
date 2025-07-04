# JPG2 Project

- [Visão Geral](#visão-geral)
- [Requisitos Funcionais](#requisitos-funcionais)
- [Requisitos Não Funcionais](#TODO)
- [Escopo](#TODO)
- [Arquitetura e Design](#TODO)
- [Decisões Técnicas](#TODO)

---

## Visão Geral

O JPG2 Project é um jogo educativo desenvolvido para complementar o ensino da disciplina de Direito em uma turma universitária. O projeto surgiu a partir de uma pesquisa conduzida com os alunos e a professora responsável pela matéria, que revelou diversas dificuldades enfrentadas no processo de aprendizagem, especialmente relacionadas ao excesso de termos técnicos, linguagem densa e ausência de exemplos práticos durante as aulas.

Entre os principais desafios identificados pelos alunos estão a velocidade com que o conteúdo é apresentado, a baixa clareza na explicação de conceitos e a dificuldade em acompanhar os temas teóricos sem contextualizações práticas. Com base nesses pontos, o projeto tem como objetivo principal transformar o aprendizado jurídico em uma experiência mais acessível, interativa e envolvente, por meio da simulação de situações reais dentro da mecânica do jogo.

Para isso, o JPG2 Project será desenvolvido utilizando o motor Godot e contará com narrativas interativas, desafios práticos baseados em estudos de caso e uma linguagem acessível. Os conceitos jurídicos serão apresentados dentro de contextos compreensíveis, buscando aliar teoria à prática de maneira fluida e lúdica. O jogo também se propõe a ser uma ferramenta de apoio para os professores, promovendo a discussão e a consolidação do conteúdo em sala de aula.

Além disso, está em análise a implementação de uma API complementar para coleta de dados de desempenho dos usuários, com o intuito de oferecer métricas que auxiliem na avaliação da eficácia do aprendizado por meio da plataforma.

O JPG2 Project, portanto, não busca substituir o ensino tradicional, mas sim ampliá-lo, oferecendo uma alternativa pedagógica criativa que dialogue com as reais necessidades dos alunos e contribua para uma formação mais sólida e engajada.

## Requisitos funcionais

> [!NOTE]
> **\*** - Funcionalidades que podem ser impementadas caso a API de desempenho seja acrecentada ao escopo do projeto.

### Gameplay e Progressão

- O jogador deve criar uma conta, onde os dados de progressão e desempenho serão coletadas e armazenadas em um banco de dados *
- O jogador deve criar um personagem, o qual também servirá como registro de salvamento dos dados de forma local (e possívelmente em nuvem *).
- O jogo deve fornecer feedbacks para positivos, negativos, ou em casos específicos, justificativas, com base nas ações e decisões do jogador.
- O jogo terá pontos de salvamento automáticos 