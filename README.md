# fallback_developer_AWS-

🌩️ Explicando no jeitinho AWS Developer:
Fallback é quando você cria um mecanismo de contingência pra quando algo dá ruim. Na prática, quando um serviço falha, o fallback entra em ação pra não deixar o usuário na mão.

💡 Exemplos na AWS e que podem cair na prova AWS Developer:
API Gateway + Lambda:
Se uma API chama um Lambda e esse Lambda falha, você pode configurar uma "Lambda Function Error Handling" que faz fallback pra outra função ou até pra uma resposta padrão.

EventBridge com Fallback:
Se um evento falha na entrega, ele pode cair numa Dead Letter Queue (DLQ) no SQS, que funciona como um fallback pra capturar erros.

Step Functions:
Você pode configurar nos fluxos uma etapa de fallback pra quando algum passo falha. Tipo assim: "Se o passo X falhar, vai pro Y que lida com erros".

Route 53 - Failover Routing:
Se a sua aplicação principal cai, o Route 53 faz fallback automaticamente pra um endpoint secundário saudável. É literalmente um failover configurado.

SNS/SQS:
Se um subscriber não consegue processar a mensagem, ela pode ir pra uma DLQ, que é uma forma de fallback pra não perder a mensagem.

🧠 Resumo na lata pro dia da prova:
Fallback na AWS é um mecanismo de contingência pra quando uma função, serviço ou fluxo falha, garantindo alta disponibilidade, resiliência e continuidade dos processos.

⚡ Na prática, na prova AWS Developer tu vê fallback ligado a:
Retry (tentativas automáticas)

DLQ (Dead Letter Queue)

Step Functions Catch/Fail states

API Gateway com resposta padrão em erros

Route 53 com Failover Routing Policy
