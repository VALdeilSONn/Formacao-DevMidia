# 🌐 AlfaTech - Soluções em Hospedagem

**Projeto completo de um site institucional moderno e responsivo para uma empresa fictícia de hospedagem de sites.**  
Criado com **HTML5** e **CSS3 puro**, este projeto simula uma empresa chamada **AlfaTech**, oferecendo soluções de hospedagem com diversos planos e diferenciais.

---

## 📌 Objetivo do Projeto

Este site foi desenvolvido com o intuito de praticar e demonstrar habilidades de front-end em HTML e CSS, explorando:

- Estruturação semântica de páginas HTML.
- Criação de layout responsivo e elegante.
- Organização modular de CSS.
- Experiência do usuário com navegação clara e fluída.
- Tabelas comparativas com design profissional.

---

## 📄 O que foi desenvolvido?

### 1. Página Inicial (`home.html`)

Essa página é o **cartão de visitas da empresa**, com os seguintes destaques:

- **Cabeçalho com navegação** responsiva e links internos com rolagem suave.
- **Banner institucional** com frase de impacto e imagem promocional.
- **Seção de chamada para ação** com destaque para o valor promocional e botão de acesso à tabela de preços.
- **Seção de diferenciais** da empresa, com três blocos explicando os benefícios: configuração fácil, servidores 100% online e suporte 24/7.
- **Tabela de planos** bem estruturada com ícones, descrições e recursos visuais para facilitar a comparação.
- **Rodapé com informações de contato**, redes sociais e créditos ao desenvolvedor.

### 2. Página de Preços (`preco.html`)

Uma página complementar focada **100% na comparação entre os planos**, contendo:

- Uma **tabela responsiva** com comparação direta entre os planos: Pessoal, Profissional, Empresarial e Big Techs.
- Cada linha da tabela representa uma funcionalidade (ex: número de redes, dashboards, suporte, API, retenção de dados etc).
- Os valores dos planos estão destacados junto com suas vantagens técnicas.
- Rodapé com contato direto via WhatsApp e email.

---

## 🎨 O que foi feito no CSS?

Criei dois arquivos CSS separados:

| Arquivo       | Função                                                   |
|---------------|----------------------------------------------------------|
| `home.css`    | Estiliza toda a página inicial (`home.html`)             |
| `preco.css`   | Estiliza a página de tabela de preços (`preco.html`)     |

Principais características da estilização:

- **Responsividade** com `flexbox` e `grid` para garantir boa visualização em diferentes tamanhos de tela.
- **Paleta de cores profissional** com tons de azul, branco e cinza.
- **Animações sutis em botões** e links para interatividade.
- **Tipografia limpa e moderna** usando a fonte Google *Poppins*.
- **Ícones personalizados e ilustrações** para reforçar a identidade visual da marca.

---

## 🧩 Estrutura de Diretórios

```bash
📁 Mini-Mundo
│
├── assets/                 # Imagens e ícones do projeto
│   ├── logo-icone.png
│   ├── logo-icone-escuro.png
│   ├── imagem-banner.png
│   ├── ...
│
📁 CSS/
│   ├── home.css            # Estilos da página principal
│   └── preco.css           # Estilos da página de preços
│
📄 home.html                # Página inicial
📄 preco.html               # Página de planos com tabela comparativa
