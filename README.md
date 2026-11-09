<h1 align="center" style="font-weight: bold;">API Escola</h1>

[PYTHON__BADGE]: https://img.shields.io/badge/Python-%233776AB.svg?style=for-the-badge&logo=python&logoColor=white
[DJANGO__BADGE]: https://img.shields.io/badge/Django_REST-ff1744?style=for-the-badge&logo=django&logoColor=white
[SQLITE__BADGE]: https://img.shields.io/badge/SQLite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white

<p align="center">
  • <a href="#technologies">Tecnologias</a> •
  <a href="#started">Iniciando</a> •
  <a href="#routes">API Endpoints</a> •
  <a href="#colab">Colaboradores</a> •
  <a href="#contribute">Contribua</a> •
</p>

<p align="center">
    <b>API RESTful desenvolvida com Django Rest Framework para o gerenciamento de um ambiente escolar.</b>
</p>

<h2 id="technologies">💻 Tecnologias</h2>

<div>

![Python][PYTHON__BADGE]
![Django REST Framework][DJANGO__BADGE]
![SQLite][SQLITE__BADGE]

</div>

<h2 id="started">🚀 Iniciando</h2>

Siga os passos abaixo para executar o projeto localmente em sua máquina.

<h3>Pré-requisitos</h3>

- [Python 3.x](https://www.python.org/)
- [Git](https://git-scm.com/)

<h3>Clonando</h3>

```bash
git clone https://github.com/JoaoxVictorMS/API_Escola_DJango.git
cd API_Escola_DJango
```

<h3>Criando e Ativando o Ambiente Virtual</h3>

No Windows (Git Bash):

```bash
python -m venv venv
source venv/Scripts/activate.ps1
```

<h3>Instalando as Dependências</h3>

```bash
pip install -r requirements.txt
```

<h3>Executando</h3>

Aplique as migrações e inicie o servidor local:

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

_(Opcional)_ Para popular o banco SQLite com dados fictícios para testes:

```bash
python seed.py
```

A API estará acessível em `http://127.0.0.1:8000/`.

<h2 id="routes">📍 API Endpoints</h2>

| rota                                    | descrição                                                          |
| --------------------------------------- | ------------------------------------------------------------------ |
| <kbd>GET /alunos/</kbd>                 | Lista todos os alunos cadastrados                                  |
| <kbd>POST /alunos/</kbd>                | Cadastra um novo aluno na API                                      |
| <kbd>GET /alunos/?version=v2</kbd>      | Lista alunos utilizando a versão 2 da API (inclui o campo celular) |
| <kbd>GET /cursos/</kbd>                 | Lista todos os cursos disponíveis                                  |
| <kbd>POST /cursos/</kbd>                | Cadastra um novo curso                                             |
| <kbd>GET /matriculas/</kbd>             | Lista todas as matrículas cadastradas                              |
| <kbd>POST /matriculas/</kbd>            | Realiza a matrícula de um aluno em um curso                        |
| <kbd>GET /alunos/{id}/matriculas/</kbd> | Retorna as matrículas associadas a um aluno específico             |
| <kbd>GET /cursos/{id}/matriculas/</kbd> | Retorna todos os alunos matriculados em um curso específico        |

<h3 id="post-aluno-detail">POST /alunos/</h3>

**REQUISIÇÃO**

```json
{
  "nome": "João Victor",
  "rg": "123456789",
  "cpf": "12345678901",
  "data_nascimento": "2000-01-01"
}
```

**RESPOSTA**

```json
{
  "id": 1,
  "nome": "João Victor",
  "rg": "123456789",
  "cpf": "12345678901",
  "data_nascimento": "2000-01-01"
}
```

<h3 id="get-alunos-v2-detail">GET /alunos/?version=v2</h3>

**RESPOSTA**

```json
[
  {
    "id": 1,
    "nome": "João Victor",
    "celular": "11999999999",
    "rg": "123456789",
    "cpf": "12345678901",
    "data_nascimento": "2000-01-01"
  }
]
```

<h3 id="post-matricula-detail">POST /matriculas/</h3>

**REQUISIÇÃO**

```json
{
  "aluno": 1,
  "curso": 2,
  "periodo": "M"
}
```

**RESPOSTA**

```json
{
  "id": 1,
  "aluno": 1,
  "curso": 2,
  "periodo": "M"
}
```

<h2 id="colab">🤝 Colaboradores</h2>

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/JoaoxVictorMS">
        <img src="https://github.com/JoaoxVictorMS.png" width="100px;" alt="Foto de perfil do João Victor"/><br>
        <sub>
          <b>João Victor</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

<h2 id="contribute">📫 Contribua</h2>

Para contribuir com o projeto, siga os passos abaixo:

1. `git clone https://github.com/JoaoxVictorMS/API-Escola.git`
2. `git checkout -b feature/sua-feature`
3. Siga os padrões de commit (`feat: adiciona nova funcionalidade`)
4. Abra um Pull Request explicando as alterações realizadas!

<h3>Documentações de apoio</h3>

[📝 Como criar um Pull Request](https://www.atlassian.com/br/git/tutorials/making-a-pull-request)

[💾 Padrão de commit](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
