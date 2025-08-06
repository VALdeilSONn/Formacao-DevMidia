# 🌴 Pousada Secreta – Site Responsivo

Este é um projeto que desenvolvi para treinar **HTML5** e **CSS3**, criando um site fictício para a **Pousada Secreta**, localizada em Angra dos Reis.  
A ideia foi criar um site bonito, organizado e funcional, simulando um ambiente real de apresentação da pousada e seus quartos.

---

## 🛠 Objetivo do Projeto

Meu objetivo com este projeto foi:

- Praticar **HTML semântico** e boas práticas de estruturação.
- Criar um layout **responsivo e bem organizado**.
- Trabalhar com **design limpo** e **paleta de cores harmoniosa**.
- Usar **Google Fonts** e imagens para dar vida ao projeto.
- Criar uma **experiência de navegação fluída** entre as páginas.

---

## 📄 Estrutura do Projeto

O projeto é composto por **duas páginas principais**:

### 1️⃣ Página Inicial – `index.html`
Na página inicial, construí:

- **Cabeçalho fixo com menu de navegação**, contendo:
  - Link para a página inicial.
  - Link interno para seção "Sobre".
  - Link interno para seção "Rota".
  - Link para a página de quartos.

- **Banner principal**:
  - Uma imagem de fundo com texto centralizado destacando o nome da pousada e o slogan.
  - Fundo semitransparente para dar contraste e facilitar a leitura.

- **Seção "Sobre"**:
  - Breve apresentação da pousada.
  - Três destaques visuais com fotos para **Quarto de Solteiro**, **Quarto de Casal** e **Quarto Família**.

- **Seção "Rota"**:
  - Mapa interativo do Google Maps para facilitar o acesso.

- **Seção "Informações"**:
  - Quatro blocos informativos sobre estrutura da pousada (piscina, restaurante, quartos e recepção).
  - Organização em **duas colunas com imagens e textos alinhados**.

- **Rodapé**:
  - Contatos, endereço, telefone e link para reserva no Booking.
  - Créditos do desenvolvedor.

---

### 2️⃣ Página de Quartos – `quartos.html`
Essa página é dedicada a apresentar **os três tipos de quartos** em detalhes:

- **Quarto de Solteiro**:
  - Galeria com 3 fotos diferentes.
  - Lista de informações (TV a cabo, camas, cozinha compacta, ar-condicionado, política de cancelamento).

- **Quarto de Casal**:
  - Galeria com 3 fotos.
  - Lista de informações específicas.
  - Destaque para cancelamento grátis.

- **Quarto Família**:
  - Galeria com fotos.
  - Lista de informações, incluindo camas adicionais e cancelamento grátis.

- **Rodapé**:
  - Mesmo padrão da página inicial, mantendo consistência visual.

---

## 🎨 Estilização – CSS

Criei dois arquivos CSS separados:

- `index.css` – Estilização da página inicial.
- `quartos.css` – Estilização da página de quartos.

### Destaques do CSS:

- **Menu**:
  - Layout com **Flexbox** para alinhamento.
  - Links com **efeito hover** e cor de destaque.
  - Nome da pousada com a palavra "Secreta" em azul para criar identidade visual.

- **Banner**:
  - Imagem de fundo ocupando **100% da altura da tela**.
  - Texto centralizado com **fundo translúcido** para contraste.

- **Seções com imagens (Quartos e Sobre)**:
  - Uso de **Flexbox** para organizar colunas e imagens.
  - **Bordas arredondadas** e **sombras sutis** para dar profundidade.
  - Títulos com **bordas coloridas** criando um detalhe elegante.

- **Mapa (iframe)**:
  - Centralizado e ajustado para ocupar largura total.
  - Design responsivo para não quebrar em telas menores.

- **Rodapé**:
  - Fundo verde escuro para remeter à natureza.
  - Textos centralizados e alinhados de forma consistente.
  - Ícones organizados com espaçamento equilibrado.

---

## 📂 Estrutura de Pastas

```bash
📁 PousadaSecreta
│
├── assets/               # Imagens e ícones
│   ├── quarto-solteiro1.jpg
│   ├── quarto-casal1.jpg
│   ├── quarto-familia1.jpg
│   ├── img-fundo.jpg
│   ├── icones/
│   │   ├── endereco.png
│   │   ├── telefone.png
│   │   ├── calendario.png
│   └── ...
│
📁 estilo/
│   ├── index.css         # Estilo da página inicial
│   ├── quartos.css       # Estilo da página de quartos
│
📄 index.html             # Página inicial
📄 quartos.html           # Página de quartos


🔍 Tecnologias Utilizadas
HTML5 – Estrutura das páginas.

CSS3 – Estilização, layout e responsividade.

Google Fonts – Fonte Source Sans Pro.

Flexbox – Layout flexível.

Google Maps Embed API – Mapa interativo.


📌 Observações Pessoais
Esse projeto foi muito importante para mim porque:

Me permitiu treinar responsividade e organização.

Aprendi a criar páginas coesas e harmônicas.

Melhorei bastante o uso de CSS para alinhamento e design.

Consegui padronizar o rodapé e menu entre páginas diferentes.

👨‍💻 Desenvolvedor
Projeto desenvolvido por Valdeilson Souza.
📧 Email: valdeilsonsouzac@gmail.com

⭐ Se gostou do projeto, não esqueça de deixar uma estrela no repositório!