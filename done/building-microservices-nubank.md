# Microservices at Nubank, An Overview

- Tentaram outras alternativas mas caíram no **Kubernetes**
- Apostam em **comunicação async** para evitar perda de dados devido a falhas nas comunicações entre os microservicos (**reliable message broker**)
- Quando ocorre alguma falha no processamento da mensagem tem um esquema de **dead letter** que garante que o dado nao será perdido
- Para extração de dados criaram uma camada que chamam de 'Contracts' onde ficam as **interfaces do microservicos** com os dados que serão usados para analise
