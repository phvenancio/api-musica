# 🎵 Musique

Projeto web desenvolvido com **Flask** e **Flask-SQLAlchemy** para gerenciamento de músicas e artistas, além de integração com a **API pública do iTunes** para consulta, listagem e detalhes de músicas.

O sistema permite:
- Cadastro, edição e remoção de músicas
- Cadastro, edição e remoção de artistas
- Paginação de dados
- Consumo de API externa (iTunes Search API)
- Visualização de destaques, lançamentos recentes e sugestões aleatórias

---

## 🚀 Tecnologias Utilizadas

- **Python 3**
- **Flask 3.1.2**
- **Flask-SQLAlchemy 3.1.1**
- **MySQL**
- **PyMySQL 1.1.2**
- **Jinja2** (templates HTML)

---

## 📂 Estrutura do Projeto

```text
musique/
│
├── app.py                  # Arquivo principal da aplicação
├── requirements.txt        # Dependências do projeto
│
├── controllers/
│   └── routes.py           # Rotas e regras de negócio
│
├── models/
│   └── database.py         # Configuração do banco e models (Musics, Artists)
│
├── views/                  # Templates HTML (Jinja2)
│   ├── index.html
│   ├── musics.html
│   ├── artists.html
│   ├── apimusic.html
│   ├── musicInfo.html
│   ├── editmusic.html
│   └── editartist.html
│
└── static/                 # Arquivos estáticos (CSS, JS, imagens)
```

---

## ⚙️ Configuração do Ambiente

### 1️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

Conteúdo do `requirements.txt`:

```txt
Flask==3.1.2
Flask-SQLAlchemy==3.1.1
PyMySQL==1.1.2
```

---

## 🗄️ Banco de Dados

O projeto utiliza **MySQL**.

Ao executar o projeto, o banco de dados será criado automaticamente caso não exista.

### Configuração padrão

```python
DB_NAME = "musique"
SQLALCHEMY_DATABASE_URI = "mysql+pymysql://root:@localhost/musique"
```

> ⚠️ Caso seu MySQL utilize senha ou outro usuário, ajuste a string de conexão no arquivo `app.py`.

---

## ▶️ Executando o Projeto

```bash
python app.py
```

A aplicação estará disponível em:

```
http://localhost:4000
```

---

## 🌐 Funcionalidades Principais

### 🎶 Músicas
- Listagem com paginação
- Cadastro de novas músicas
- Edição e exclusão
- Associação com artistas

### 👤 Artistas
- Cadastro, edição e exclusão
- Relacionamento com músicas

### 🔎 Integração com API (iTunes)
- Busca por gênero
- Ordenação dinâmica
- Paginação manual
- Página de detalhes da música
- Navegação entre músicas
- Destaques aleatórios por gênero

---

## 📡 API Externa Utilizada

- **iTunes Search API**
  - Endpoint: `https://itunes.apple.com/search`
  - Endpoint: `https://itunes.apple.com/lookup`

---

## 📌 Observações

- O projeto foi desenvolvido com fins **acadêmicos**.
- Utiliza boas práticas iniciais de organização MVC.
- Não possui autenticação de usuários.

---

## 👨‍💻 Autor

**Pedro Venâncio**

---

## 📄 Licença

Este projeto é livre para uso educacional.

