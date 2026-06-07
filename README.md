# Folha de Ponto

Este sistema foi desenvolvido para atender às necessidades de controle de frequência de servidores públicos, integrando tecnologias modernas para garantir segurança, precisão e eficiência na gestão de pessoal.

## 📑 Visão Geral

O projeto **Folha-de-Ponto** é uma solução robusta focada na automação e transparência do registro de jornada de trabalho. Utiliza biometria facial para assegurar a autenticidade e evitar fraudes, com processamento local para garantir a disponibilidade do sistema mesmo em ambientes com instabilidade de rede.

## 🛠 Tecnologias Utilizadas

O ecossistema do projeto é composto pelas seguintes tecnologias:

* **Backend**: Python com **FastAPI** para alta performance e escalabilidade nas requisições.
* **Banco de Dados**: **PostgreSQL** com extensão **pgvector** para indexação e busca eficiente de vetores biométricos.
* **Biometria**: Integração com **InsightFace API** para reconhecimento facial de alta precisão.
* **Infraestrutura**: Projetado para rodar em ambientes conteinerizados (**Docker**).
* **Interface**: Desenvolvimento focado em tablets e dispositivos móveis (Responsividade).

## 🏗 Arquitetura

O sistema opera através de um fluxo otimizado:

1. **Captura**: Tablet (GitHub Pages/Front-end) envia a foto e o CPF do servidor.
2. **Processamento**: O Servidor FastAPI processa a biometria via InsightFace e consulta o PostgreSQL.
3. **Resultado**: Confirmação do ponto registrada e retornada para o usuário final.

## 🚀 Requisitos Funcionais e Não Funcionais

* **RNF01 (Segurança)**: Criptografia de ponta a ponta para dados biométricos e senhas.
* **RNF02 (Desempenho)**: Validação facial concluída em menos de 3 segundos.
* **RNF03 (Disponibilidade)**: Operação local independente de internet externa.
* **RNF04 (Usabilidade)**: Interface responsiva para repartições públicas.
* **RNF05 (Escalabilidade)**: Estrutura preparada para o crescimento da base de servidores.

## 👤 Desenvolvedor

* **Autor**: Márcio Rodrigues de Oliveira
* **Assinatura**: RAZGO TECNOLOGIA

