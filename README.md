# 🛡️ Comnect Guardians

Plataforma gamificada **multi-tenant** de conscientização e treinamento em cibersegurança para empresas. Desenvolvida para transformar a educação em segurança da informação em uma experiência prática, competitiva e envolvente, com isolamento completo de dados e rankings por organização e departamento.

---

## 🚀 Principais Funcionalidades

### 🏢 Arquitetura Multi-Tenant Corporativa
- **Disputa Interdepartamental:** Colaboradores somam pontos tanto para o ranking individual quanto para a média/total de seu departamento dentro da empresa.

### 🎮 Minigames & Desafios Táticos
- **Simulações de Quiz (`/minigames/quiz/:id/play`):** Cenários de Phishing & Engenharia Social, Gestão de Senhas & MFA e Segurança de Redes/Criptografia, com limite de tempo e cálculo dinâmico de recompensas.
- **Cofre de Senhas (`/minigames/cofre`):** Desafio interativo de criação de senhas fortes baseado em regras progressivas de complexidade.
- **Decriptar (`/minigames/decriptar/play`):** Minigame de decodificação de termos técnicos e conceitos de cibersegurança com dicas e controle de tempo.
- **LogScan (`/minigames/logscan/play`):** Caça-palavras tático voltado à identificação rápida de ameaças em matrizes de logs.
- **Patrulha Diária:** Desafio rápido integrado ao dashboard principal para coleta diária de XP e moedas.

### ⚔️ Progressão, Classes e Economia
- **Sistema de Classes:** Escolha entre **Guardião**, **Analista**, **Sentinela** e **Hacker Ético**, cada uma com *perks* exclusivos (tempo extra, bônus de XP forense, multiplicador de ofensiva ou bônus de moedas).
- **Loja & Inventário (`/loja`):** Compra, venda, *reroll* de catálogo e uso de itens **Passivos** (ex.: *CPU 128 Cores*, *Cold Wallet*, *Firewall Camada 7*) e **Consumíveis** (ex.: *Injetor de Overclock*, *Backup de Memória*).
- **Missões Diárias, Ofensiva (Streak) & Conquistas:** Acompanhamento de metas diárias, níveis de certificação e desbloqueio automático de conquistas.
- **Rankings (`/rankings`):** Classificação isolada por empresa filtrável por XP, Moedas e Ofensiva, além do ranking de departamentos.
- **Central de Treinamentos & Feedback (`/treinamentos`, `/feedback`):** Glossário de termos de segurança, galeria de quizzes e canal para reporte de bugs/vulnerabilidades com recompensa em moedas.

---

