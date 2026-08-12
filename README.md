# Hacker Rangers - Notificações de Pendências via Power Automate

Repositório contendo os templates para automação de notificações de missões pendentes na plataforma Hacker Rangers, integrados via Microsoft Power Automate.

## 📦 Conteúdo do Repositório

- `email-template.html`: Template HTML otimizado para Outlook com visualização prévia (preheader), botão ajustado e estilos corporativos.
- `adaptive-card-teams.json`: Payload do Adaptive Card para envio de alertas via Microsoft Teams.

## 🛠️ Como Utilizar no Power Automate

### E-mail HTML
1. Em seu fluxo do power automate adicione e abra a ação **Enviar um e-mail (V2)** no Power Automate.
2. Alterne a exibição do corpo da mensagem para o modo **HTML** (`</>`).
3. Copie todo o conteúdo do arquivo `email-template.html` e cole na ação.

### Adaptive Card (Teams)
1. Em seu fluxo do power automate adicione e abra a ação **Postar card adaptável em um chat ou canal** no Teams.
2. Copie o conteúdo do arquivo `adaptive-card-teams.json` e cole no campo **Adaptive Card**.
3. Não se esqueça de calcular a quantidade de cursos e quizzes pendentes, para isso utilize os endpoints `/api/adm/report/tabular/30` e `/api/adm/report/tabular/26`, respectivamente.
