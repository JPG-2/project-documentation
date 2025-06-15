# Getting Started

Nesse tutorial você irá aprender a preparar o ambiente local para desenvolvimento.

## Pré-requisitos

- Python >= 3.12
- MongoDB

## Clone do projeto

Faça um fork do repositório da organização do GitHub. Em seguida, faça um clone desse fork. Você pode clonar o repositório num diretório local de sua preferência.

```bash
git clone https://github.com/doda-s/api-server-side.git
cd api-server-side
```

Agora que você está dentro do repositório local, podemos começar a preparar o ambiente de desenvolvimento.

## Inicializando uma venv Python

Para podermos desenvolver sem ter problemas de compatibilidade, é ideal utilizarmos um ambiente virtual Python (VENV). Para isso, execute os seguintes comandos:

```bash
# Windows
python -m venv .venv
./.venv/Scripts/activate
```
> Um marcador escrito (venv) deve aparecer no teminal.

```bash
# Linux
python3 -m venv .venv
source .venv/bin/activate
```
> Um marcador escrito (venv) deve aparecer no teminal.

Com isso, você já tem um ambiente criado e ativado, pronto para o desenvolvimento. Lembre-se de que toda vez que você for desenvolver, é necessário ativar o ambiente.

## Instalando as dependências

Todas as dependências do projeto estão salvos no arquivo `requirements.txt`, basta utilizar o `pip` para instalá-los.

```bash
pip install -r requirements.txt
```

Depois do pip instalar todas as dependências do projeto, você pode verificar se tudo está instalado corretamente utilizando:

```bash
pip freeze
```