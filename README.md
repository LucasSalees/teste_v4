# Teste Técnico — Desenvolvedor Frontend (V4 Company | Colli&Co)

Este repositório contém a entrega do teste técnico para a vaga de Desenvolvedor Frontend. O projeto foca em alta compatibilidade para e-mail marketing e boas práticas de semântica e acessibilidade para Landing Pages.

📂 Estrutura do Projeto


teste_v4/
  ├── email/
  │   └── index.html      # Código do E-mail Marketing (Table-based)
  ├── lp/
  │   ├── index.html      # HTML5 Semântico da Landing Page
  │   └── styles.css      # CSS Moderno (Variáveis + Grid/Flexbox)
  └── README.md           # Documentação do projeto

---

## 🚀 Como abrir e testar localmente

Clone este repositório ou baixe os arquivos.

Landing Page: Abra o arquivo lp/index.html em qualquer navegador moderno. Recomenda-se o uso da extensão Live Server no VS Code para uma melhor experiência.

E-mail Marketing: Abra o arquivo email/index.html. Para testar a responsividade, utilize o modo de inspeção do navegador simulando dispositivos móveis.

---

## 📧 Parte 1 — E-mail Marketing (Mesa 4X)

### Decisões Técnicas

Table-based Layout: Utilizei uma estrutura de tabelas aninhadas para garantir que o layout não quebre em clientes de e-mail legados (como Outlook 2010-2019).

CSS Híbrido: Apliquei o CSS crítico de forma inline (cores, fontes, larguras) para garantir a renderização no Gmail e Outlook, mantendo Media Queries no <head> exclusivamente para a transição de layout no mobile.

Double CTA Strategy: Implementei dois botões de ação estrategicamente posicionados (Hero e Final) para otimizar a taxa de conversão (CTR).

Bulletproof Buttons: Os botões foram construídos com preenchimento em células de tabela (<td>) e links em bloco, garantindo que funcionem mesmo com imagens desativadas.

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

Semântica: Uso rigoroso de tags HTML5 "(<header>, <main>, <section>, <footer>)".

Navegação: Hierarquia de títulos (h1-h3) lógica e estados de :focus-visible customizados para navegação via teclado.

---

## 🏆 Parte 3 — Desafio Extra Escolhido

Opção Escolhida: B) LP v2 - Seção FAQ com Acordeão sem JS

Para este desafio, decidi demonstrar o poder do HTML5 nativo:

Implementação: Utilizei as tags <details> e <summary>.

Diferencial: O acordeão funciona perfeitamente sem nenhuma linha de JavaScript, garantindo performance máxima, menor tempo de carregamento e acessibilidade nativa para leitores de tela.

Estilização: Personalizei os ícones de abertura e fechamento (+ / -) utilizando pseudo-elementos ::after e seletores de estado do CSS.

---

## Conclusão e Considerações

O projeto foi desenvolvido com foco em código limpo e funcionalidade real. No e-mail, a prioridade foi a entregabilidade; na Landing Page, a prioridade foi a experiência do usuário (UX) e performance.
