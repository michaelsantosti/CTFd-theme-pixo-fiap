# FIAP Pixo Theme

Tema retro para [CTFd](https://github.com/CTFd/CTFd) com visual CRT dos anos 90, adaptado e estendido para uso nas plataformas de CTF da **FIAP**.

Este projeto é um **fork** do tema original [CTFd-theme-pixo](https://github.com/hmrserver/CTFd-theme-pixo) criado por [PRI4CE / hmrserver](https://github.com/hmrserver).

## Funcionalidades adicionadas

### Challenge Solution (Resolução)
- Aba "Resolução" no modal do desafio para exibir writeups publicados pelo administrador
- Suporte completo ao fluxo de unlock da API de Solutions
- Exibida apenas quando o admin publica uma solução (estado "visible" ou "solved")

### Challenge Ratings (Avaliação de Desafios)
- Exibição de ratings agregados (thumbs up/down com percentual) abaixo do valor do desafio
- Formulário de avaliação (thumbs up/down + review opcional) que aparece após resolver um desafio
- Pré-preenche avaliação existente do usuário
- Controlado pela config `challenge_ratings` (public/private/disabled)

### View Self Submissions (Histórico de Submissões)
- Aba "Submissões" no modal do desafio com histórico de tentativas do usuário
- Exibe flag mascarada com toggle de visibilidade (eye icon), tipo e data
- Controlado pela config `view_self_submissions`

### Scoreboard com Brackets
- Suporte completo a brackets (grupos/categorias de participantes)
- Tabs de navegação para filtrar por bracket (ex: "Todos", "Universitário", "Profissional")
- Gráfico Top 10 atualiza dinamicamente ao trocar de bracket
- Badges com nome do bracket na view "Todos"

### Internacionalização (i18n)
- Suporte completo a tradução pt_BR via Flask-Babel
- Tradução de strings hardcoded no JavaScript via `window._i18n` com patches de runtime
- Strings traduzidas: abas, mensagens de submissão (Correto, Incorreto, etc.), alertas, dicas, diálogos

### Tokens de API
- Campo de descrição na criação de tokens
- Coluna de descrição na tabela de tokens ativos
- Modal com API key gerada + botão de copiar

### Melhorias gerais
- Página de erro 401 (Unauthorized)
- Snackbar de verificação de email (lembrete para confirmar e-mail)
- Navbar: suporte a `link_target` em páginas de plugin + verificação correta de visibilidade do Scoreboard
- Título dinâmico por página no navegador
- Suporte a `{{ meta | safe }}` para meta tags SEO
- `window.init` completo com `userName`, `userEmail`, `userVerified`, `teamId`, `teamName`
- Página de confirmação de email com tratamento do fluxo `?flow=init`
- Indicadores de campos obrigatórios (`*`) em login e registro
- Atributos `autocomplete` em formulários de login, registro e reset de senha
- Opções de tema expandidas: ordenação customizada de categorias/desafios + syntax highlighter

## Instalacao

### Via Docker
```bash
git clone https://github.com/michaelsantosti/ctfd-theme-pixo.git /opt/CTFd/CTFd/themes/fiap-pixo
```

### Manual
Copie o conteudo do tema para a pasta de temas do CTFd:
```bash
cp -r . /caminho/para/CTFd/CTFd/themes/fiap-pixo
```

Em seguida, acesse **Painel Admin > Config > Themes** e selecione `fiap-pixo`.

## Compatibilidade

- CTFd **3.8.x**
- Bootstrap **4.3.1** (incluido no bundle do tema)
- jQuery (incluido no bundle do tema)

## Creditos

- [PRI4CE / hmrserver](https://github.com/hmrserver) - Criador do tema original [CTFd-theme-pixo](https://github.com/hmrserver/CTFd-theme-pixo)
- [CTFd](https://github.com/CTFd/CTFd) - Plataforma de CTF
- [Freepik](https://www.freepik.com) - Imagens (seta e moeda)
- [FIAP](https://www.fiap.com.br) - Adaptacoes e extensoes para uso interno

## Licenca

Este tema e um fork do trabalho original de PRI4CE. Consulte o repositorio original para termos de licenciamento.
