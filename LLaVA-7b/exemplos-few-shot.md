### Prompt 3 - Few-shot (alguns exemplos calibram tom e nível técnico)

**Contexto:**
Estou escrevendo mensagens de commit seguindo Conventional Commits. 
Veja meus exemplos:

"Adiciona validação de CPF no cadastro de usuário" 
→ feat(auth): add CPF validation on user registration

"Corrige erro 500 quando token JWT está expirado" 
→ fix(auth): handle expired JWT token error

"Remove console.log esquecido no módulo de pagamento" 
→ chore(payment): remove debug console.log

Agora converta: "Muda o timeout das chamadas pra API de pagamento 
de 5 para 15 segundos"

**Resposta:**
Refactor(payment): modify timeout from 5 to 15 seconds for payment API calls
