# Bit by Bit Blog

## Descrição do Projeto
O **Bit by Bit Blog** é um projeto desenvolvido em Python utilizando o framework Django. O blog permite que usuários visualizem notícias em diferentes categorias, comentem em publicações e interajam com os conteúdos. Ele também conta com um sistema de autenticação para gerenciar login de usuários, além de um painel administrativo que permite a criação, atualização, e exclusão de posts pelo usuário administrador.

## Visão Geral
O objetivo do projeto é fornecer uma plataforma de publicação de notícias simples e eficiente, destacando-se pelas funcionalidades administrativas do Django, como a gestão de posts e usuários. A interface apresenta um design limpo e direto, permitindo que os usuários naveguem facilmente pelos conteúdos.

- A página principal exibe artigos em destaque, com seções específicas para notícias recentes e categorias relevantes.
- Usuários autenticados podem comentar nos posts, promovendo a interação e discussão.
- A administração do site é gerenciada por um painel admin robusto, característico do Django, que facilita o controle dos conteúdos e das permissões de usuários.

## Imagens do Projeto
A seguir, estão algumas capturas de tela do blog:

1. **Página Principal** - Mostra artigos em destaque e uma lista de posts recentes em diferentes categorias.
   
2. **Tela de Login** - Interface simples para autenticação de usuários.
![Imagem da Web](https://drive.google.com/uc?export=view&id=11XZqrmNVC6wU03cKIqD8XXEHn2faYQ9S)

4. **Sistema de Comentários** - Permite que os usuários autenticados comentem nas publicações.
![Imagem da Web](https://drive.google.com/uc?export=view&id=17PtdSGUcMXSvx8T7-5iGPN97AimpI-Sp)
  
6. **Painel Administrativo** - Controle completo de posts, categorias, comentários e gerenciamento de usuários.
![Imagem da Web](https://drive.google.com/uc?export=view&id=1-Y9sPCV6TvuP2snUJHfLm6hCo-py5ec2)



## Requisitos do Sistema
Para executar o projeto, você precisará das seguintes versões e bibliotecas:

- **Python**: 3.12.3
- **Django**: 5.1.2
- **Bibliotecas Adicionais**:
  - `asgiref==3.8.1` : Fornece suporte para funcionalidades assíncronas no Django, essenciais para rodar servidores e aplicações modernas com capacidade de lidar com conexões simultâneas.

  - `backports.zoneinfo==0.2.1` : Garante suporte a fusos horários se estiver usando Python abaixo da versão 3.9, necessário para o correto gerenciamento de horários no projeto.

  - `crispy-bootstrap4==2024.10` : Simplifica o estilo e a formatação de formulários Django usando o Bootstrap 4, melhorando a aparência e a responsividade sem esforço manual.

  - `django-crispy-forms==2.3` : Facilita a renderização de formulários customizados e bem organizados no Django, tornando a criação de interfaces de usuário mais intuitiva.

  - `pillow==11.0.0` : Permite trabalhar com imagens (redimensionar, salvar, e converter formatos) no projeto, útil para funcionalidades que envolvem upload e manipulação de imagens.

  - `sqlparse==0.5.1` : Utilizado para formatar e analisar consultas SQL, garantindo que o Django gerencie e exiba as consultas de forma eficiente e compreensível.

  - `tzdata==2024.2` : Fornece atualizações de fusos horários globais, essencial para garantir que datas e horários estejam corretos em diferentes regiões.


---

### Explicação dos Principais Pontos da Estrutura de Diretórios e Arquivos do Projeto

- **blog_main/**: Contém as configurações principais do projeto Django, como `settings.py` para configurações globais, `urls.py` para o roteamento de URLs, e `views.py` para a lógica de exibição das páginas principais.

- **blogs/**: Diretório que representa um aplicativo Django específico, onde a lógica de negócios do blog é definida. Inclui:
  - **admin.py**: Configura o painel administrativo para gerenciar o conteúdo do blog.
  - **apps.py**: Configurações do aplicativo `blogs`.
  - **models.py**: Define a estrutura dos dados (modelos) armazenados no banco de dados, como Posts, Categorias, e Comentários.
  - **views.py**: Contém a lógica para renderizar as páginas do blog e gerenciar as ações dos usuários.
  - **migrations/**: Pasta que armazena scripts de migração do banco de dados, necessários para aplicar mudanças no modelo.

- **media/uploads/**: Diretório usado para armazenar arquivos de mídia carregados, como imagens de posts. Subdiretórios são organizados por ano e mês.

- **templates/**: Contém os arquivos HTML do projeto, com diferentes templates para cada página, como a página inicial (`home.html`), a página de blogs (`blogs.html`), e formulários de autenticação como `login.html` e `register.html`.

- **db.sqlite3**: O banco de dados SQLite usado para desenvolvimento e testes. Contém todos os dados persistentes, como posts de blogs, usuários, e comentários.

- **manage.py**: Utilitário do Django para executar várias tarefas administrativas, como rodar o servidor de desenvolvimento, fazer migrações, e criar superusuários.

- **requirements.txt**: Lista as bibliotecas e suas versões específicas que precisam ser instaladas para o projeto funcionar corretamente.

---

## Instalação e Configuração

### Pré-requisitos
- **Python 3.7 ou superior** instalado.
- **pip** (gerenciador de pacotes do Python) instalado.
- **Git** instalado para clonar o repositório.

### 1. Clonar o Repositório
Abra o terminal (ou Prompt de Comando no Windows) e execute:

`git clone git@github.com:SEU_USUARIO/NOME_DO_REPOSITORIO.git`
Substitua SEU_USUARIO e NOME_DO_REPOSITORIO pela URL correta do seu repositório no GitHub.

### 2. Navegar até o Diretório do Projeto

`cd NOME_DO_REPOSITORIO`

### 3. Criar e Ativar um Ambiente Virtual

**No Windows:**

Criar o ambiente virtual:
`python -m venv env`
Ativar o ambiente virtual:
`env\Scripts\activate`

**No Linux:**
Criar o ambiente virtual:

`python3 -m venv env`
Ativar o ambiente virtual:

`source env/bin/activate`

### 4. Instalar as Dependências
Com o ambiente virtual ativo, execute:

`pip install -r requirements.txt`

### 5. Configurar o Banco de Dados
Execute as migrações para configurar o banco de dados:

`python manage.py migrate`

### 6. Criar um Superusuário (Opcional, mas recomendado)
Para acessar o painel administrativo do Django, crie um superusuário:

`python manage.py createsuperuser`
Siga as instruções para definir um nome de usuário, e-mail e senha.

### 7. Rodar o Servidor de Desenvolvimento
`python manage.py runserver`
Acesse o projeto no navegador:
URL padrão: http://127.0.0.1:8000/

### 8. Notas Importantes
Ambiente Virtual: Sempre ative o ambiente virtual antes de rodar comandos relacionados ao projeto.
Painel Administrativo: Acesse http://127.0.0.1:8000/admin/ e faça login com o superusuário.

---


