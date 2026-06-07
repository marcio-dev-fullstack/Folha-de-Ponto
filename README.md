<div align="center">

# 📊 Folha de Ponto

**Sistema de Controle de Frequência biométrica para Administração Pública**

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Framework-green.svg)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue.svg)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-Container-blue.svg)](https://www.docker.com/)

---

</div>

## 📌 Visão Geral
O **Folha-de-Ponto** é uma solução de engenharia voltada para a automação e transparência. Desenvolvido para atuar com alta disponibilidade, utiliza reconhecimento facial para garantir que o registro seja seguro e inviolável.

## ⚙️ Stack Tecnológico
| Categoria | Tecnologia |
| :--- | :--- |
| **Backend** | Python / FastAPI |
| **Banco de Dados** | PostgreSQL + pgvector |
| **Biometria** | InsightFace API |
| **Container** | Docker |

## 🏗 Arquitetura do Sistema
```mermaid
graph TD
    A["Tablet/Front-end"] -->|Envia Foto + CPF| B["Servidor FastAPI"]
    B -->|Consulta DB| C["PostgreSQL + pgvector"]
    B -->|Processa Biometria| D["InsightFace API"]
    C -->|Retorna Resultado| B
    B -->|Confirma Ponto| A