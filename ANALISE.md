# Criando o conteúdo dos arquivos .md solicitados

# 1. Analise Funcional (requisitos_funcionais.md)
req_func = """# Requisitos Funcionais - FOLHA DE PONTO
**Projeto:** FOLHA DE PONTO - Prefeitura de Conceição do Araguaia
**Autor:** MARCIO

## Requisitos Funcionais (RF)

| ID | Nome | Descrição |
|----|------|-----------|
| RF01 | Cadastro de Servidores | O sistema deve permitir o cadastro de servidores com CPF único e captura de biometria facial. |
| RF02 | Registro de Ponto | O sistema deve permitir o registro de ponto (entrada/saída) mediante validação facial e CPF. |
| RF03 | Validação Facial | O sistema deve comparar a foto enviada com o embedding facial cadastrado no banco de dados. |
| RF04 | Autenticação por CPF | O sistema deve exigir a senha (CPF) como segundo fator de autenticação. |
| RF05 | Logs de Auditoria | O sistema deve registrar data, hora e evidência fotográfica de todas as tentativas de registro. |
| RF06 | Gestão de Relatórios | O sistema deve gerar relatórios de frequência para a administração pública. |
"""

# 2. Analise Não Funcional (requisitos_nao_funcionais.md)
req_nao_func = """# Requisitos Não Funcionais - FOLHA DE PONTO
**Projeto:** FOLHA DE PONTO - Prefeitura de Conceição do Araguaia
**Autor:** MARCIO

## Requisitos Não Funcionais (RNF)

| ID | Categoria | Descrição |
|----|-----------|-----------|
| RNF01 | Segurança | O sistema deve criptografar os dados biométricos e senhas (CPF). |
| RNF02 | Desempenho | O tempo de processamento para validação facial não deve exceder 3 segundos. |
| RNF03 | Disponibilidade | O sistema deve estar acessível localmente mesmo sem conexão com a internet externa. |
| RNF04 | Usabilidade | A interface deve ser responsiva, adequada para tablets em repartições públicas. |
| RNF05 | Escalabilidade | O banco de dados deve suportar o crescimento da base de servidores da prefeitura. |
"""

# 3. Diagramas (arquitetura_diagramas.md)
diagramas = """# Diagramas de Arquitetura - FOLHA DE PONTO
**Autor:** MARCIO

## 1. Visão Geral (Mermaid)

```mermaid
graph TD
    A["Tablet/Front-end (GitHub Pages)"] -->|Envia Foto + CPF| B["Servidor Local (FastAPI)"]
    B -->|Consulta DB| C["PostgreSQL + pgvector"]
    B -->|Processa Biometria| D["InsightFace API"]
    C -->|Retorna Resultado| B
    B -->|Confirma Ponto| A