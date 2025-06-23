# Descrição do jogo

Este é um jogo educativo voltado para estudantes de Direito, com foco na disciplina de Fundamentos e Aplicação do Direito. A proposta é transformar conceitos jurídicos abstratos em experiências práticas e interativas, utilizando casos reais como base. Mediante decisões complexas e dilemas morais, o jogador é desafiado a aplicar o conhecimento aprendido em sala de aula. A jogabilidade é inspirada em Papers Please (jogo), misturando análise crítica, interpretação legal e tomada de decisão sob pressão, tudo em um ambiente envolvente que simula o cotidiano jurídico.

# Tecnologias utilizada

## Principais Libs

- FastAPI
- Beanie - ODM
- Pydantic
- PyJWT - Geração de token JWT
- bcrypt

## Integrações

API roda em cima de uma aplicação FastAPI. Os dados são armazenados em um banco de dados MongoDB, por meio de uma ODM (Object Document Model). As ODMs são criadas a partir da biblioteca **Beanie**, e permite manipular os dados dos documentos, e organizar as collections. Tanto FastAPI quanto Beanie utilizam Pydantic como base, permitindo uma integração sólida entre essas libs. Para a geração de tokens JWT, a biblioteca utilizada é a PyJWT, o qual é muito compatível com FastAPI. Para encriptar os dados, está sendo utilizado a lib **bcrypt**.

Fluxo lógico: [https://excalidraw.com/#json=DWpBwkpmliBQM-M8Z0FB4,OW-y4d6iwgQREMDBsaS7mw](https://excalidraw.com/#json=DWpBwkpmliBQM-M8Z0FB4,OW-y4d6iwgQREMDBsaS7mw)

# Sincronização de dados

O cliente envia os dados via requisição HTTP/HTTPS. Toda vez que o progresso do jogador for salvo, todos os dados do usuário serão atualizados. Os dados que poderão ser atualizados são:

- Progresso do jogador.
    - Nível de confiança
    - Número de casos vencidos
    - Número de casos perdidos
- Achievements.
- Badges.
- Títulos.

Como o objetivo da API é somente demonstrar status sobre os usuários/jogadores, ela não sincroniza os dados de progresso entre clientes (apesar de salvar alguns dados de progresso), e somente salva os dados gerais de estatísticas de desempenho dos jogadores.

# Segurança e Autenticação

O método de autenticação é baseado em JWT, onde o usuário informa o user (usuário) e a senha, e a API retorna um token de autenticação JWT. Ao criar um usuário, os dados de registro são salvos no banco de dados. A senha de acesso é encriptada com a lib **bcrypt** para aumentar a segurança.

Pelo fato de ser utilizado DTOs as requests para a API, a chance de ocorrer injeções de códigos mal intencionados e querys indesejados ao banco de dados, são drasticamente reduzidos.

## Pontos de melhoria:

- Tempo de duração de token reduzido.
- Implementação de token refresh.

Implementar um método de token refresh reduz a chance do token JWT ser capturado e utilizado sem a ciência do usuário real maliciosamente, visto que o token JWT pode ter uma duração menor.

# Insígnias - Emblemas - Recompensas

O usuário pode desbloquear insígnias e emblemas (através de conquista). As insígnias podem ser desbloqueados ao passar de nível, demonstrando o progresso do jogador. Ao realizar feitos específicos no jogo, achievements são desbloqueados. Os achievements são representados por emblemas. Ao completar certas ações e tarefas, o jogador receberá títulos. Os títulos são baseados em prefixo e sufixo.

# Ranking Geral

O nosso jogo não foca em competitividade, e sim no desempenho individual dos jogadores. Optamos por não implementar um ranking pelo motivo de não condizer com a proposta do jogo. Porém, decidimos adicionar outras formas de apresentar o desempenho dos jogadores. Isso será feito através dos seguintes sistemas:

## Status Globais

- Porcentagem global de jogadores que desbloquearam cada emblema.
- Porcentagem global de jogadores que desbloquearam cada insígnia.

## Status Individuais

Todos os status de progresso dos jogadores serão acessíveis publicamente. Informações como: Nível de Confiança, Número de Casos Vencidos e Número de Casos Perdidos.

Também será acessível publicamente as informações de emblemas e insígnias desbloqueadas dos jogadores.