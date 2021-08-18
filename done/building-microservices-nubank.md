# Microservices at Nubank, An Overview

- Have tried other ways but ended with **Kubernetes**
- Use **async communication** on large scales to prevent data loss and communication issues between microservices (**reliable message broker**)
- Quando ocorre alguma falha no processamento da mensagem tem um esquema de **dead letter** que garante que o dado nao será perdido
- Para extração de dados criaram uma camada que chamam de 'Contracts' onde ficam as **interfaces do microservicos** com os dados que serão usados para analise
