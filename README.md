# 🚀 Transferidor de Banco de Dados - Calculo

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

Sistema para transferir dados entre versões do software **Calculo**, utilizado pela Tooling Equipamentos Ópticos para cálculos de curvas aplicadas na surfassagem de lentes por máquinas Geradoras.

---

## 🧠 Objetivo

Automatizar a transferência e atualização do banco de dados entre versões do sistema Calculo, minimizando erros manuais e otimizando o processo de migração.

---

## ⚙️ Tecnologias Utilizadas

- Python 3.x
- Firebird/Interbase
- Biblioteca `fdb` (Python)
- Scripts SQL automatizados

---

## 📁 Estrutura

src/ → Scripts em Python
scripts/ → Scripts SQL
docs/ → Documentação e imagens

---

## 🛠️ Como usar

```bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/calculo-transferidor-db.git

# Entre na pasta
cd calculo-transferidor-db

# Instale as dependências
pip install -r requirements.txt

# Execute o script principal
python src/main.py
