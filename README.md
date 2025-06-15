# 🦾 UiPath REFramework em C#

Este projeto é uma adaptação do REFramework (Robotic Enterprise Framework) do UiPath, recriado em **C#** e **VB.Net** como forma de estudo e documentação. Ele simula o fluxo de um robô RPA estruturado, com boas práticas de controle de exceções, logs, separação de responsabilidades e modularidade.

---

## 📸 Fluxo do Robô

![Fluxo do robô](./fluxo.png)

> A imagem acima representa o ciclo de vida do robô, inspirado no REFramework tradicional.

---

## 📌 Estrutura Geral

O projeto segue a estrutura básica:

```text
src/

├── GetTransactionData.cs
├── InitAllApplications.cs
├── InitAllSettings.cs
├── send_emails.cs
├── ProcessTransaction.cs
├── Send_manifest.cs
├── signers_manipulation.cs


```
---

## 🧠 Lógica de Execução

1. **InitAllSettings.cs**  
   Lê configurações de um arquivo `config.txt`. Esse arquivo tem todo o direcionamento para o orquestrador do Uipath

2. **InitAllApplications.cs**  
   Simula a inicialização de aplicativos necessários para o processo.

3. **GetTransactionData.cs**  
   Busca itens de uma lista simulando uma fila de transações. Todos os itens estão em uma fila do orquestrador

4. **ProcessTransaction.cs**  
   Processa uma transação individual.

5. **send_emails.cs**  
   Envio de emails para os assinantes com os links de assinatura ao fim da transação processada.

6. **signers_manipulation.cs**  
   Formatação de um Json em VB.net, usado com invokecode no Uipath para tratar os dados da fila e enviar o json para api do portal de assinatura.

7. **Send_manifest.cs**  
   Processa uma transação de conferência dos documentos assinados, envia alerta para assinates ou anexa os documentos já assinados na solicitação inicial.

---



