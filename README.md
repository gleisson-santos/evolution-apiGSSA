# 🦍 Evolution API (Versão GSSA)

**Fork oficial mantido por Gleisson Santos.**

A Evolution API é uma API Rest completa para controle de funções do WhatsApp, baseada na biblioteca [Baileys](https://github.com/WhiskeySockets/Baileys). Este projeto expandiu para se tornar uma plataforma de integração multi-canal, conectando WhatsApp, OpenAI, Typebot, Chatwoot e muito mais.

![Docker](https://img.shields.io/badge/Docker-Compatible-blue)
![NodeJS](https://img.shields.io/badge/Node.js-v20-green)
![WhatsApp](https://img.shields.io/badge/Network-WhatsApp-25D366)

## 🚀 Funcionalidades Principais

*   **API RESTful**: Controle total do WhatsApp via requisições HTTP (Enviar mensagens, mídia, criar grupos).
*   **Múltiplas Conexões**: Gerencie várias instâncias do WhatsApp simultaneamente.
*   **Integrações Nativas**:
    *   **Typebot**: Crie fluxos conversacionais inteligentes.
    *   **Chatwoot**: Centralize o atendimento ao cliente.
    *   **OpenAI**: Inteligência artificial para respostas e transcrição de áudio.
    *   **Webhooks**: Receba eventos em tempo real (mensagens, status) em seu sistema.

## 🛠️ Instalação (Docker)

A maneira mais recomendada de rodar a Evolution API é via Docker Compose.

1.  **Baixe o docker-compose.yaml**
    ```yaml
    version: '3.3'
    services:
      evolution-api:
        container_name: evolution_api
        image: attias/evolution-api:latest
        restart: always
        ports:
          - "8080:8080"
        env_file:
          - .env
        volumes:
          - evolution_store:/evolution/store
    volumes:
      evolution_store:
    ```

2.  **Configure o .env**
    Crie um arquivo `.env` com sua `AUTHENTICATION_API_KEY` e outras configurações.

3.  **Execute**
    ```bash
    docker-compose up -d
    ```

## 📚 Documentação

Para documentação completa dos endpoints e configurações, acesse a [Documentação Oficial](https://doc.evolution-api.com).

## 📄 Licença

Este projeto é licenciado sob a Apache License 2.0.
Mantido e customizado por [Gleisson Santos](https://github.com/gleisson-santos).