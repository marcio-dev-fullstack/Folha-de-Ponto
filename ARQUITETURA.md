# Documento de Proposta Técnica: Sistema FOLHA DE PONTO

**Projeto:** FOLHA DE PONTO - Prefeitura de Conceição do Araguaia

**Autor:** MARCIO RODRIGUES DE OLIVEIRA- ENGENHEIRO DE SOFTWARE

**Assinatura de Desenvolvimento:** RAZGO TECNOLOGIA

---

## 1. Visão Geral

O sistema **FOLHA DE PONTO** é uma solução de registro eletrônico de assiduidade voltada para a Prefeitura de Conceição do Araguaia. O objetivo é garantir conformidade, transparência e segurança através de autenticação por duplo fator: validação facial e CPF.

## 2. Stack Tecnológico

Para assegurar escalabilidade e eficiência, a arquitetura proposta utiliza:

* **Front-end:** React ou Flutter Web (PWA), otimizado para tablets em repartições públicas.


* **Back-end:** Python com **FastAPI** ou **Spring Boot** (processamento local no servidor municipal).


* **Banco de Dados:** PostgreSQL com a extensão `pgvector` para armazenamento de *embeddings* faciais.


* **Processamento de Imagem:** Biblioteca `face_recognition` ou API **InsightFace** para alta precisão na comparação facial.



## 3. Roadmap de Desenvolvimento

| Fase | Ação | Descrição |
| --- | --- | --- |
| **I** | **Database & API** | Modelagem do banco (Tabela de servidores, registros de ponto, logs de imagem). |
| **II** | **Módulo Biométrico** | Implementação do endpoint de verificação facial comparando a foto atual com o cadastro. |
| **III** | **Front-end** | Interface de usuário com input de CPF e captura automática de câmera. |
| **IV** | **RAZGO Integration** | Padronização visual da marca MAZZ e assinatura oficial do desenvolvedor. |

## 4. Segurança e Governança Pública

Considerando a sensibilidade dos dados biométricos, o sistema implementa controles rigorosos:

* **Liveness Detection:** Verificação de vivacidade (ex: movimentos faciais) para impedir fraudes com fotos ou telas.


* **Log de Auditoria:** Registro imutável contendo timestamp, coordenadas GPS (se aplicável) e o *hash* da validação facial.


* **Sigilo:** Tratamento de dados biométricos sob rigorosos protocolos de proteção de informação.


