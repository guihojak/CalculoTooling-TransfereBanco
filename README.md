# 🚀 Transferidor de Banco de Dados - Calculo (Calctool)

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

Ferramenta para automatizar a migração de dados entre versões do software **Calculo (Calctool)**, utilizado pela Tooling Equipamentos Ópticos para cálculo das curvas na surfassagem de lentes em máquinas Geradoras.

---

## 🧩 Problema

Usuários do Calctool, ao atualizarem o software para versões mais recentes (exemplo: da 2.0.0 para 2.0.10), precisam manter seus dados previamente salvos — como Ordens de Serviço, Espessuras, Valores de Cliente, Números de Ordem e outras configurações armazenadas no banco de dados `TOOLINGLINK.GDB`.

A transferência manual desses dados, feita simplesmente copiando e substituindo o arquivo `.GDB` local, não funciona. Isso ocorre porque as versões mais recentes do Calculo possuem alterações no banco (novas tabelas, campos, procedimentos SQL, etc.) que tornam a substituição direta inconsistente, causando erros no SQL.

---

## 💡 Solução Proposta

O projeto automatiza o processo de migração dos dados entre versões diferentes do banco Firebird/Interbase do Calculo, realizando:

- Leitura e exportação dos dados existentes na versão antiga;
- Aplicação dos scripts SQL necessários para atualizar a estrutura do banco na versão nova;
- Inserção e adaptação dos dados conforme o novo modelo, preservando as informações importantes do usuário.

Isso minimiza erros manuais, evita perda de dados e permite que o usuário atualize o Calculo com segurança e facilidade.

---

## ⚙️ Tecnologias Utilizadas

- Python 3.x  
- Firebird/Interbase  
- Biblioteca `fdb` para conexão e manipulação do banco via Python  
- Scripts SQL para atualização da estrutura do banco

---

## 📁 Estrutura do Projeto

src/ → Scripts Python para execução da migração

scripts/ → Scripts SQL para atualização do banco

docs/ → Documentação e imagens

README.md → Documentação principal

requirements.txt → Dependências Python

config.ini → Configuração para conexão com banco


---

## 🚀 Como Usar

1. Clone o repositório:

```bash
git clone https://github.com/SEU_USUARIO/calculo-transferidor-db.git
cd calculo-transferidor-db

Instale as dependências:

pip install -r requirements.txt

Configure o arquivo config.ini com os dados de conexão para as versões antiga e nova do banco.

Execute o script principal para iniciar a transferência:

python src/main.py

```
---

## 🎯 Objetivo do Projeto

- Facilitar a atualização do Calculo sem perda ou corrupção de dados;

- Reduzir o tempo e esforço do usuário na migração manual;

- Garantir integridade e compatibilidade dos dados entre versões;

- Servir como estudo prático de automação e manipulação de bancos Firebird via Python.

---

## 📄 Licença

- Projeto licenciado sob os termos da MIT License.

---

## 👨‍💼 Desenvolvido por

Guilherme Xavier Hojak
Tooling Equipamentos Ópticos
LinkedIn

---