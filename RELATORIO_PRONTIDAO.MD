# Relatório de Prontidão Técnica: Onboarding SecOps

**Disciplina:** Engenharia de Produto de Software (FGA0316) - 2026.1
**Aluno:** Luis Eduardo Carneiro Miranda | **Matrícula:** 21/1063200

## 1. Configuração do Ambiente (Zero Trust & Isolamento)
Conforme as diretrizes de Soberania Técnica, as seguintes configurações foram aplicadas:
- [X] **Python 3.12:** Instalado e verificado.
- [X] **Poetry:** Configurado para criar `.venv` dentro do projeto (`virtualenvs.in-project true`).
- [X] **Determinismo:** Arquivos `pyproject.toml` e `poetry.lock` gerados com sucesso.

### Comandos feitos

```bash
$ python3 --version   
Python 3.14.0

$ poetry --version                           
Poetry (version 2.3.3)

$ ls -la
.github
.venv/
poetry.lock
pyproject.toml
RELATORIO_PRONTIDAO.MD 
```

## 2. Logs de Auditoria e Qualidade (Security Gate)
Abaixo constam os resumos das execuções dos comandos de segurança:

### 2.1. Auditoria Estática (Bandit)

```json
{
  "errors": [],
  "generated_at": "2026-04-02T00:13:12Z",
  "metrics": {
    "./main.py": {
      "CONFIDENCE.HIGH": 0,
      "CONFIDENCE.LOW": 0,
      "CONFIDENCE.MEDIUM": 0,
      "CONFIDENCE.UNDEFINED": 0,
      "SEVERITY.HIGH": 0,
      "SEVERITY.LOW": 0,
      "SEVERITY.MEDIUM": 0,
      "SEVERITY.UNDEFINED": 0,
      "loc": 0,
      "nosec": 0,
      "skipped_tests": 0
    },
    "_totals": {
      "CONFIDENCE.HIGH": 0,
      "CONFIDENCE.LOW": 0,
      "CONFIDENCE.MEDIUM": 0,
      "CONFIDENCE.UNDEFINED": 0,
      "SEVERITY.HIGH": 0,
      "SEVERITY.LOW": 0,
      "SEVERITY.MEDIUM": 0,
      "SEVERITY.UNDEFINED": 0,
      "loc": 0,
      "nosec": 0,
      "skipped_tests": 0
    }
  },
  "results": []
}
```

*Comando: `poetry run bandit -r .`*

### 2.2. Verificação de Dependências (Safety)

+===========================================================================================================================================================================================+


+=======================================================================================================================================+

                               /$$$$$$            /$$
                              /$$__  $$          | $$
           /$$$$$$$  /$$$$$$ | $$  \__//$$$$$$  /$$$$$$   /$$   /$$
          /$$_____/ |____  $$| $$$$   /$$__  $$|_  $$_/  | $$  | $$
         |  $$$$$$   /$$$$$$$| $$_/  | $$$$$$$$  | $$    | $$  | $$
          \____  $$ /$$__  $$| $$    | $$_____/  | $$ /$$| $$  | $$
          /$$$$$$$/|  $$$$$$$| $$    |  $$$$$$$  |  $$$$/|  $$$$$$$
         |_______/  \_______/|__/     \_______/   \___/   \____  $$
                                                          /$$  | $$
                                                         |  $$$$$$/
  by safetycli.com                                        \______/

+=======================================================================================================================================+

 REPORT 

  Safety v3.7.0 is scanning for Vulnerabilities...
  Scanning dependencies in your environment:

  -> /home/luismiranda/workspace/luis-pessoal-repos/eps/eps-g17-buscador-osint/.venv/lib/python3.14/site-packages

  Using open-source vulnerability database
  Found and scanned 46 packages
  Timestamp 2026-04-01 21:03:58
  0 vulnerabilities reported
  0 vulnerabilities ignored

*Comando: `poetry run safety check`*

### 2.3. Qualidade e Conformidade (Ruff)

```
All checks passed!
```

*Comando: `poetry run ruff check .`*

## 3. Evidência de Integração Contínua (CI)
O pipeline automatizado foi executado com sucesso no GitHub Actions:
- **Link da Action de Sucesso:** [COLE AQUI O LINK DO SEU GITHUB ACTIONS]

## 4. Declaração de Soberania Técnica (CISSP Domain 8)
Eu, Luis Eduardo Carneiro Miranda, declaro que auditei manualmente as ferramentas e dependências deste projeto. Confirmo que o código gerado via IA (GitHub Copilot) passou pela minha revisão humana (*Human-in-the-loop*), garantindo que não há vazamento de segredos ou falhas lógicas críticas antes da migração para o ecossistema da PCDF.

---
**Data de Entrega:** 01/04/2026

Observacoes gerais e especificas: inserir texto com suas observacoes sobre aspectos outros que valem a pena considerar ou que voce identificou como necessarios a serem realizados no futuro. 