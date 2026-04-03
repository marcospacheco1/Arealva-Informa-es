# 📰 Arealva Informações — Portal de Notícias com Ecossistema Digital Completo

![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Mercado Pago](https://img.shields.io/badge/Mercado%20Pago-009EE3?style=for-the-badge&logo=mercadopago&logoColor=white)
![PIX](https://img.shields.io/badge/PIX-32BCAD?style=for-the-badge&logo=pix&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

> Portal de notícias hiperlocal com ecossistema digital próprio: moeda virtual (Coins)
> ganhas por leitura, apostas esportivas, rifas com sorteio automatizado, vitrines
> comerciais para lojistas, enquetes, fórum, guia de utilidades e painel administrativo
> completo com controle financeiro e múltiplos operadores.

🔗 **[Acessar portal](https://arealvainformacoes.com.br)**

---

## 📌 Sobre o projeto

O Arealva Informações é uma plataforma digital hiperlocal desenvolvida do zero em PHP puro,
pensada para ser o hub de informação e serviços de uma cidade.

Além do portal de notícias tradicional, o sistema possui uma economia virtual própria baseada
em Coins — moeda interna que os usuários ganham ao ler conteúdo e utilizam para participar
de apostas e rifas. Os pagamentos são processados via PIX com integração real à API do
Mercado Pago. O painel administrativo cobre publicação de conteúdo, gestão financeira completa,
controle de usuários, lojistas parceiros e utilidades da cidade.

Todo o sistema foi desenvolvido de forma autônoma, sem frameworks ou CMS externos.

---

## 🚀 Módulos do sistema

### 📝 Conteúdo & editorial

- **Publicação de notícias** — editor de matérias com upload de fotos, categorias e
  controle do feed da página inicial
- **Métricas de leitura** — usuários online em tempo real e ranking das notícias
  mais lidas do dia
- **Enquetes** — criação de pesquisas de opinião com apuração e exibição de
  resultados em tempo real
- **Fórum de comentários** — sistema de comentários por notícia com moderação
  pelo painel
- **Mensagens** — caixa de mensagens recebidas pelo formulário de contato do portal

---

### 🪙 Sistema de Coins (economia virtual)

O portal possui uma moeda virtual própria chamada **Coins**, que cria um ciclo de
engajamento entre leitura de conteúdo e participação em jogos e prêmios.

**Fluxo dos Coins:**
```
Usuário lê uma notícia
        │
        ▼
Sistema credita Coins automaticamente
(valor configurável pelo admin)
        │
        ▼
Usuário acumula saldo de Coins
        │
        ├──► Usa Coins para apostar em jogos de futebol
        │
        └──► Usa Coins para comprar cotas de rifas
```

- Valor dos Coins por leitura é definido pelo administrador
- Saldo individual de cada usuário visível no painel master
- Histórico de ganhos e gastos registrado no banco de dados

---

### 💳 Financeiro & gestão

- **Fluxo de caixa** — lançamento de entradas e saídas operacionais
  (servidores, despesas) com histórico completo
- **Relatório financeiro mensal** — faturamento total e lucro líquido
  por período, gerado automaticamente
- **Planos de assinatura** — gestão de valores de planos para lojistas
  e usuários com diferentes níveis de acesso

---

### 🎲 Jogos & prêmios

#### Apostas esportivas (Bets)

- Cadastro de jogos de futebol com odds e data
- Usuários apostam com Coins ou via pagamento direto em PIX
- Admin confirma comprovantes de pagamento recebidos
- Sistema registra ganhadores e processa pagamento automático via PIX

#### Rifas

- Criação de rifas com definição de cotas, valor e prêmio
- Venda de cotas com controle de disponibilidade em tempo real
- Gestão completa de compradores por rifa
- Sorteio final automatizado pelo sistema com registro do ganhador

---

### 💰 Pagamento PIX (Mercado Pago)
```
Usuário escolhe pacote / aposta / cota de rifa
        │
        ▼
Backend gera cobrança via API Mercado Pago
        │
        ▼
QR Code PIX + código copia-e-cola exibidos na tela
        │
        ▼
Usuário paga pelo app bancário
        │
        ▼
Mercado Pago dispara webhook para o servidor
        │
        ▼
Backend valida assinatura do webhook
        │
        ▼
Crédito de Coins / confirmação de aposta / cota registrada
        │
        ▼
Usuário notificado em tela via AJAX
```

---

### 🏪 Utilidades & lojas

- **Vitrines comerciais** — mini-sites para lojistas parceiros dentro do portal,
  com planos de assinatura gerenciados pelo admin
- **Guia de telefones úteis** — diretório de emergência e serviços da cidade,
  editável pelo painel
- **Horários de ônibus** — tabela de circulares e linhas interurbanas
  atualizada pelo admin
- **Links úteis** — curadoria de links relevantes para a cidade

---

### 👥 Controle de usuários (Master)

- **Lista de usuários** — visão completa de todos os cadastros com saldo de Coins,
  plano ativo e histórico de atividade
- **Gerenciar admins** — cadastro de administradores auxiliares com
  permissões por módulo
- **Controle de acesso por nível** — separação entre admin master e
  operadores com escopos limitados

---

## 🛡️ Segurança aplicada

- Prepared statements contra SQL Injection (PDO)
- Hash de senhas com `password_hash()` (bcrypt)
- Sanitização e validação de inputs no frontend e backend
- Validação de assinatura dos webhooks do Mercado Pago
- Controle de sessão com timeout automático
- Proteção CSRF em todos os formulários
- Upload de imagens com validação de tipo MIME e tamanho máximo

---

## 🗂️ Stack tecnológico

| Camada | Tecnologia |
|---|---|
| Backend | PHP 8, PDO, sessões nativas |
| Banco de dados | MySQL |
| Frontend | jQuery, AJAX, CSS3 puro |
| Pagamentos | Mercado Pago API — PIX |
| Tempo real | AJAX polling |
| E-mail | PHPMailer |
| Servidor | Apache, Linux |

---

## 📐 Arquitetura de módulos
```
arealvainformacoes.com.br/
├── Portal público
│   ├── Feed de notícias
│   ├── Enquetes & comentários
│   ├── Vitrines comerciais
│   └── Utilidades (telefones, ônibus, links)
│
├── Área do usuário
│   ├── Saldo de Coins
│   ├── Apostas & rifas
│   └── Histórico de transações
│
└── Painel admin
    ├── Editorial (notícias, métricas, mensagens)
    ├── Financeiro (caixa, relatórios, planos)
    ├── Jogos (bets, rifas, sorteios)
    ├── Lojas (vitrines, telefones, ônibus)
    └── Master (usuários, admins, Coins)
```

---

## 👨‍💻 Papel no projeto

Desenvolvedor solo — responsável por 100% do projeto: concepção, arquitetura,
modelagem do banco de dados, backend, frontend, economia virtual, integração com
API de pagamentos PIX, deploy e manutenção em produção.

---

## 📷 Preview

![Painel administrativo](https://arealvainformacoes.com.br/img/Captura%20de%20tela%20de%202026-04-02%2021-43-15.png)



---

## 📬 Contato

Desenvolvido por **Marcos Pacheco**
🌐 [pachecotec.com.br](https://pachecotec.com.br)
