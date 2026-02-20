# Teste Técnico — Desenvolvedor Frontend

## V4 Company | Colli&Co

Olá! 👋
Este repositório contém a minha entrega para o teste técnico da vaga de Desenvolvedor Frontend.

O objetivo do projeto foi demonstrar boas práticas em dois cenários bem comuns no dia a dia do front-end:

### 📧 E-mail Marketing, com foco em compatibilidade entre clientes

### 🌐 Landing Page, com HTML semântico, acessibilidade e layout responsivo

```text
teste_v4/
 ├── email/
 │   └── index.html      # Template de E-mail Marketing
 ├── lp/
 │   ├── index.html      # Landing Page em HTML5 semântico
 │   └── styles.css      # Estilos CSS
 └── README.md           # Documentação do projeto
```

## 🚀 Como visualizar o projeto localmente

O projeto é bem simples de rodar e não exige build, servidor ou dependências.

### Obter os arquivos

Você pode escolher uma das opções abaixo:

1️⃣ Clonar o repositório

Abra o terminal (Git Bash, Terminal ou PowerShell) e execute:

```text
git clone https://github.com/LucasSalees/teste_v4.git
```

2️⃣ Entrar na pasta do projeto

Após o clone, navegue até o diretório criado:

```text
cd teste_v4
```

3️⃣ Verificar os arquivos (opcional)

Se quiser conferir se tudo foi clonado corretamente:

```text
ls
```

Você deverá ver algo parecido com:

```text
email/
lp/
README.md
```

4️⃣ Abrir os arquivos no navegador

🌐 Landing Page

Entre na pasta da landing page:

```text
cd lp
```

Abra o arquivo index.html:

Clique duas vezes no arquivo ou arraste para o navegador

💡 Dica: pressione Ctrl + F5 para evitar cache.

📧 E-mail Marketing

Volte para a pasta principal:

```text
cd ..
```

entre na pasta do email: 

```text
cd email
```

Abra o arquivo index.html no navegador

Para testar a responsividade:

Pressione F12

Ative o modo mobile (Toggle Device Toolbar)

### Não é necessário instalar nada

Este projeto não usa build, bundler ou dependências externas.
Basta clonar, abrir os arquivos e testar no navegador.

## 📧 Decisões técnicas — E-mail Marketing

O foco principal do e-mail foi compatibilidade e entregabilidade, não estética extrema.

Principais decisões:

### Layout baseado em tabelas (table-based)
Utilizei tabelas aninhadas porque ainda são o padrão mais confiável para e-mails, principalmente em clientes legados como Outlook Desktop.

CSS híbrido (inline + media queries)

Estilos críticos (cores, fontes, espaçamentos) ficam inline

Media queries são usadas apenas para adaptação mobile

### Botões “bulletproof”
Os botões foram construídos com td + a, garantindo funcionamento mesmo com imagens bloqueadas.

### Dois pontos de conversão (CTAs)
Um CTA no hero e outro no final do e-mail, aumentando a chance de clique.

### Fontes web-safe
Uso de Arial/Helvetica para evitar falhas de carregamento em ambientes corporativos.

## 🌐 Decisões técnicas — Landing Page

A Landing Page foi desenvolvida com foco em clareza de código, boa experiência do usuário e facilidade de manutenção, simulando um cenário real de produto.

Estrutura e semântica: 

### HTML5 semântico
Uso de tags como header, main, section e footer para deixar a estrutura clara tanto para desenvolvedores quanto para mecanismos de busca e leitores de tela.

### Hierarquia correta de títulos
Utilização de h1 a h3 de forma lógica, evitando quebras na hierarquia de conteúdo.

Layout e responsividade:

### Abordagem mobile-first
A página foi pensada inicialmente para mobile e depois adaptada para telas maiores, garantindo boa experiência em qualquer dispositivo.

### Flexbox
Utilizado principalmente no header e na seção hero para alinhamento e distribuição dos elementos.

### CSS Grid
Aplicado nas seções de cards (“Como funciona”, “Planos” e FAQ), oferecendo maior controle do layout em telas maiores e facilitando a responsividade.

Organização e manutenção do CSS: 

### CSS separado do HTML
Todo o estilo fica no arquivo styles.css, mantendo separação de responsabilidades.

### CSS Variables (Design Tokens simples)
Variáveis definidas no :root para cores, espaçamentos e fontes, facilitando ajustes futuros e garantindo consistência visual.

### Classes reutilizáveis
Botões, grids e cards seguem padrões reutilizáveis para evitar duplicação de código.

Acessibilidade (A11y):

### Textos alternativos (alt) nas imagens
Todas as imagens possuem descrição adequada.

### Uso de aria-label quando necessário
Principalmente em botões e elementos de navegação.

### Componentes navegáveis via teclado
Estrutura pensada para funcionar corretamente sem mouse.

### FAQ sem JavaScript
Uso de details e summary, garantindo acessibilidade nativa e melhor performance.

## ⏱️ O que eu faria diferente com mais tempo

Se tivesse mais tempo para evoluir o projeto, eu adicionaria:

### No E-mail Marketing

Implementação de VML para botões perfeitos no Outlook Desktop

Imagens em 2x (Retina) para telas de alta densidade

Testes em ferramentas como Litmus ou Email on Acid

### Na Landing Page

Pequenas animações com prefers-reduced-motion

Lazy loading de imagens

Validação de acessibilidade com Lighthouse / Axe

Versão alternativa focada em performance extrema (Core Web Vitals)

### ✅ Considerações finais

Este projeto foi desenvolvido pensando em cenários reais de front-end:

No e-mail, a prioridade foi compatibilidade e entregabilidade

Na landing page, o foco foi clareza, acessibilidade e organização do código

A ideia foi escrever código simples, legível e fácil de manter, simulando um ambiente de trabalho colaborativo.

Obrigado pela oportunidade 🙌