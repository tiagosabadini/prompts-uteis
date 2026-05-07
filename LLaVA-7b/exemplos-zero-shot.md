### Prompt 1 - Zero-shot (sem exemplo, mas com contexto rico)

**Contexto:**
Você é um dev sênior revisando o código de um colega júnior. O código abaixo é um endpoint REST em Node.js com Express. Aponte problemas de segurança, performance e legibilidade. Seja direto e explique o motivo de cada problema encontrado.
```javascript
app.get('/users', (req, res) => {
    db.query('SELECT * FROM users WHERE id=' + req.query.id, (err, result) => {
       res.send(result);
    });
});
```

**Resposta:**
 Olá! Como dev sênior revisando o código de um colega júnior, posso ajudar a identificar alguns problemas de segurança, performance e legibilidade no código abaixo:
```javascript
app.get('/users', (req, res) => {
  db.query('SELECT * FROM users WHERE id=' + req.query.id, (err, result) => {
    res.send(result);
  });
});
```
1. **Problemas de segurança**:
   - Ao utilizar `req.query.id` diretamente na consulta SQL, você está expondo informações sensíveis ao usuário. Isso pode ajudar atacantes a determinar o ID de outros usuários e acessar suas informações pessoais.
   - Além disso, a concatenação do id na consulta é vulnerável a SQL Injection, que pode permitir atacantes a inserir código malicioso na consulta e obter resultados imprevistos ou mesmo executar comandos do banco de dados.

2. **Problemas de performance**:
   - O uso de `SELECT * FROM users WHERE id=` + req.query.id pode ser ineficiente, pois pode retornar todos os campos de uma tabela inteira, incluindo campos desnecessários e que podem ter impacto negativo na performance do banco de dados e da aplicação.
   - Além disso, o uso de `SELECT *` pode causar problemas de desempenho ao retornar muitos dados inutilizados para a requisição. Isso pode afetar negativamente a performance do banco de dados e da aplicação.

3. **Problemas de legibilidade**:
   - O código é bem curto e difícil de ler, o que pode fazer com que você ou outros desenvolvedores tenham dificuldade em entender como funciona a consulta SQL e como a solicitação HTTP está sendo tratada no back-end.
   - A ausência de uma descrição do código, bem como comentários, torna mais difícil revisar o código e fazer alterações ou correções futuras.

Para resolver esses problemas, sugiro que você faça as seguintes mudanças:

1. **Segurança**:
   - Use a consulta SQL com parâmetros definidos para evitar SQL Injection e evitar expor informações sensíveis ao usuário. Por exemplo, poderia usar um método de segurança como o `mysql2` que oferece a funcionalidade de escape strings para proteger contra ataques SQL.
   - Se você estiver trabalhando em um ambiente de desenvolvimento ou teste e não precisar da máxima performance, é recomendável adotar consultas SQL mais otimizadas para melhorar a performance do banco de dados e da aplicação.

2. **Performance**:
   - Use uma consulta SQL mais otimizada para selecionar apenas os campos necessários para a requisição atual, o que pode melhorar a performance do banco de dados e da aplicação. Por exemplo, você poderia usar `SELECT nome, email FROM users WHERE id=` + req.query.id.
   - Adicione um índice no campo ID para melhorar o desempenho da consulta SQL.

3. **Legibilidade**:
   - Crie um comentário explicando a finalidade do código e como funciona a solicitação HTTP e o tratamento do banco de dados no back-end. Isso pode facilitar entender a funcionalidade da página e fazer alterações ou correções futuras.
   - Organize o código em blocos e use variáveis adequadas para melhorar a legibilidade do código e evitar erros de digitação.

Estas mudanças podem garantir que seu código seja mais seguro, performante e legível, o que pode resultar em uma melhor experiência de usuário. 
