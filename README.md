# sistema-de-leilao


# 1. Definição do Projeto
Um sistema web onde usuários podem criar e participar de leilões online em tempo real. O sistema permite que vendedores cadastrem itens para leilão e compradores façam lances até o encerramento do prazo.

# 2. Requisitos do Sistema
# 2.1 Funcionais
✅ Cadastro e login de usuários (clientes e administradores)
✅ Criar e gerenciar leilões
✅ Permitir lances em tempo real
✅ Notificar usuários sobre lances e encerramento do leilão
✅ Processar pagamento do lance vencedor

# 2.2 Não Funcionais
✅ Interface intuitiva e responsiva
✅ Segurança para evitar lances fraudulentos
✅ Escalabilidade para suportar múltiplos leilões simultâneos

# 3. Tecnologias Utilizadas
Backend: Django (Django REST Framework para API)

Banco de Dados: PostgreSQL

Frontend: React.js ou Vue.js

WebSockets: Django Channels (para lances em tempo real)

Autenticação: Django Allauth ou JWT

Pagamento: Stripe ou PayPal API

# 4. Estrutura do Banco de Dados
## Usuário (User)
ID

Nome

Email

Senha (hash)

## Leilão (Auction)
ID

Título

Descrição

Imagem

Preço inicial

Data de início e fim

Criador (relacionado ao usuário)

Status (ativo, encerrado)

## Lance (Bid)
ID

Usuário

Leilão

Valor

Timestamp

# 5. Fluxo do Sistema
1️⃣ Cadastro/Login
O usuário cria uma conta e acessa o sistema.

2️⃣ Criação de Leilão
Um usuário vendedor adiciona um novo item para leilão com preço inicial e duração.

3️⃣ Lances em Tempo Real
Usuários compradores podem fazer lances enquanto o leilão está aberto. O sistema avisa quando há um novo maior lance.

4️⃣ Encerramento do Leilão
Quando o tempo acaba, o usuário com o maior lance é declarado vencedor.

5️⃣ Pagamento e Conclusão
O vencedor faz o pagamento e o vendedor envia o item.