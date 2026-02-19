# Teste Técnico — Desenvolvedor Frontend (V4 Company | Colli&Co)

Este repositório contém a entrega do teste técnico para a vaga de Desenvolvedor Frontend. O projeto foca em alta compatibilidade para e-mail marketing e boas práticas de semântica e acessibilidade para Landing Pages.

📂 Estrutura do Projeto

```text
teste_v4/
  ├── email/
  │   └── index.html      # Código do E-mail Marketing (Table-based)
  ├── lp/
  │   ├── index.html      # HTML5 Semântico da Landing Page
  │   └── styles.css      # CSS Moderno (Variáveis + Grid/Flexbox)
  └── README.md           # Documentação do projeto
```

---

## 🚀 Como abrir e testar localmente

Existem duas formas principais de acessar o projeto em sua máquina:

## 1. Preparação

Escolha uma das opções abaixo para obter os arquivos:

Via Git: Clone o repositório com o comando:

Bash

```text
git clone https://github.com/seu-usuario/teste_v4.git
```

Download Direto: Clique no botão verde "Code" no topo desta página e selecione "Download ZIP". Após baixar, extraia os arquivos em uma pasta de sua preferência.

## 2. Execução dos Componentes

A estrutura do projeto é simples e não requer a instalação de compiladores ou servidores pesados.

📄 Landing Page (LP)

A página principal utiliza HTML5 moderno e CSS Grid/Flexbox.

Navegue até a pasta lp/.

Clique duas vezes no arquivo index.html.

O projeto abrirá automaticamente no seu navegador padrão.

📧 E-mail Marketing

O e-mail foi construído utilizando a técnica de tabelas (table-based) para garantir compatibilidade com diversos gerenciadores (Outlook, Gmail, etc).

Navegue até a pasta email/.

Abra o arquivo index.html no navegador.

Para testar a responsividade: * Pressione F12 (ou clique com o botão direito e vá em Inspecionar).

Clique no ícone de dispositivos móveis (Toggle Device Toolbar) no topo do console para simular a visualização em smartphones.

---

## 📧 Parte 1 — E-mail Marketing (Mesa 4X)

### Decisões Técnicas

Table-based Layout: Utilizei uma estrutura de tabelas aninhadas para garantir que o layout não quebre em clientes de e-mail legados (como Outlook 2010-2019).

CSS Híbrido: Apliquei o CSS crítico de forma inline (cores, fontes, larguras) para garantir a renderização no Gmail e Outlook, mantendo Media Queries no 

```text 
<head> 
``` 

textexclusivamente para a transição de layout no mobile.

Double CTA Strategy: Implementei dois botões de ação estrategicamente posicionados (Hero e Final) para otimizar a taxa de conversão (CTR).

Bulletproof Buttons: Os botões foram construídos com preenchimento em células de tabela 

```text  
(<td> )
```

e links em bloco, garantindo que funcionem mesmo com imagens desativadas.

### Compatibilidade e Limitações

Fonts: Utilizei a stack de fontes web-safe (Arial, Helvetica) para evitar falhas de carregamento de fontes externas em ambientes corporativos.

Dark Mode: Implementei suporte básico via color-scheme para garantir legibilidade em temas escuros.

### O que eu faria com mais tempo?

Implementação de VML para botões com bordas arredondadas perfeitas no Outlook Desktop.

Uso de imagens em 2x (Retina) para garantir nitidez em displays de alta densidade.

---

## 🌐 Parte 2 — Landing Page (Mesa 4X)

### Decisões Técnicas e Arquitetura

CSS Variables (Design Tokens): Defini tokens de cores e espaçamentos no :root, facilitando a manutenção e garantindo a consistência visual (Design System mínimo).

Layout Moderno: * Flexbox: Utilizado no Header e Hero para alinhamentos flexíveis.

CSS Grid: Utilizado nas seções "Como Funciona" e "Planos" para um controle preciso do grid responsivo.

Mobile-First: A página foi desenhada para priorizar dispositivos móveis, adaptando o grid para 1 coluna e ajustando escalas de fonte via clamp().

### Acessibilidade (A11y)

Semântica: Uso rigoroso de tags HTML5 

```text
"(<header>, <main>, <section>, <footer>)".
```

Navegação: Hierarquia de títulos (h1-h3) lógica e estados de :focus-visible customizados para navegação via teclado.

---

## 🏆 Parte 3 — Desafio Extra Escolhido

Opção Escolhida: B) LP v2 - Seção FAQ com Acordeão sem JS

Para este desafio, decidi demonstrar o poder do HTML5 nativo:

Implementação: Utilizei as tags 

```text
<details> e <summary>.
```

Diferencial: O acordeão funciona perfeitamente sem nenhuma linha de JavaScript, garantindo performance máxima, menor tempo de carregamento e acessibilidade nativa para leitores de tela.

Estilização: Personalizei os ícones de abertura e fechamento (+ / -) utilizando pseudo-elementos ::after e seletores de estado do CSS.

---

## Conclusão e Considerações

O projeto foi desenvolvido com foco em código limpo e funcionalidade real. No e-mail, a prioridade foi a entregabilidade; na Landing Page, a prioridade foi a experiência do usuário (UX) e performance.
