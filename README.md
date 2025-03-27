# 📦 Automação FTP e Extração de Arquivos via GitHub Actions

Este projeto tem como objetivo automatizar o processo de **download de um arquivo `arq.zip` via FTP da LocalWeb** e **extrair todos os arquivos contidos nele** diretamente dentro do ambiente do GitHub Actions.  
Tudo acontece **sem depender de hospedagens externas**, como HostGator ou Replit.

---

## ✨ Funcionalidades

- 🔽 Faz o **download automático** do arquivo `arq.zip` via FTP da LocalWeb
- 📂 **Descompacta todos os arquivos XML** diretamente no GitHub Actions
- 💾 Salva todos os arquivos como **artefato do GitHub**, disponível para download
- 📅 Executa automaticamente todos os dias às **5h da manhã (Horário de Brasília)**
- 🔘 Permite execução **manual** pela interface do GitHub

---

## 🔄 Automatização via GitHub Actions

Arquivo do workflow:  
`.github/workflows/extrair-e-commitar.yml`

### ⏰ Agendamento automático
Executado todos os dias às **5h (Horário de Brasília)**:
```yaml
schedule:
  - cron: '0 8 * * *'  # 8h UTC = 5h BRT
