<div align="center">

# 📊 Folha de Ponto

**Sistema de Controle de Frequência Biométrica para Administração Pública**

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Framework-green.svg)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue.svg)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-Container-blue.svg)](https://www.docker.com/)

---

</div>

## 📌 Visão Geral
O **Folha de Ponto** é uma solução de engenharia voltada para a automação e transparência. Desenvolvido para atuar com alta disponibilidade, utiliza reconhecimento facial para garantir que o registro seja seguro e inviolável.

## ⚙️ Stack Tecnológico
| Categoria | Tecnologia |
| :--- | :--- |
| **Backend** | Python / FastAPI |
| **Banco de Dados** | PostgreSQL + pgvector |
| **Biometria** | InsightFace API |
| **Container** | Docker |

## 🏗 Arquitetura
O sistema opera através de um fluxo otimizado:
* **Captura**: Tablet (GitHub Pages/Front-end) envia a foto e o CPF do servidor.
* **Processamento**: O Servidor FastAPI processa a biometria via InsightFace e consulta o PostgreSQL.
* **Resultado**: Confirmação do ponto registrada e retornada para o usuário final.

```mermaid
graph TD
    A["Tablet/Front-end"] -->|Envia Foto + CPF| B["Servidor FastAPI"]
    B -->|Consulta DB| C["PostgreSQL + pgvector"]
    B -->|Processa Biometria| D["InsightFace API"]
    C -->|Retorna Resultado| B
    B -->|Confirma Ponto| A

```

## 🚀 Requisitos Funcionais e Não Funcionais

* **RNF01 (Segurança)**: Criptografia de ponta a ponta para dados biométricos e senhas.
* **RNF02 (Desempenho)**: Validação facial concluída em menos de 3 segundos.
* **RNF03 (Disponibilidade)**: Operação local independente de internet externa.
* **RNF04 (Usabilidade)**: Interface responsiva para repartições públicas.
* **RNF05 (Escalabilidade)**: Estrutura preparada para o crescimento da base de servidores.

---

### 👤 Desenvolvedor

**Autor**: Márcio Rodrigues de Oliveira

**Assinatura**: RAZGO TECNOLOGIA

Desenvolvido com excelência técnica
