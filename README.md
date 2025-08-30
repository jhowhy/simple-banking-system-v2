# Desafio Apresentação - Sistema Bancário em Python

## Objetivo Geral
Separar as funções existentes de saque, depósito e extrato em funções. Criar duas novas funções: cadastrar usuário (cliente) e cadastrar conta bancária.

## Desafio
Precisamos deixar nosso código mais modularizado, criando funções para as operações existentes: **sacar, depositar e visualizar histórico (extrato)**.  
Além disso, para a versão 2 do sistema, precisamos criar duas novas funções: **criar usuário** (cliente do banco) e **criar conta corrente** (vinculada a um usuário).

---

## Separação em Funções
Todas as operações do sistema devem ser implementadas em funções.  
Cada função terá regras específicas para a passagem de argumentos. O retorno e a forma como serão chamadas podem ser definidos de acordo com sua implementação.

### Saque
- Deve receber **apenas argumentos por nome** (keyword-only).
- **Sugestão de argumentos:** `saldo`, `valor`, `extrato`, `limite`, `numero_saques`, `limite_saques`.
- **Sugestão de retorno:** `saldo` e `extrato`.

### Depósito
- Deve receber **apenas argumentos por posição** (positional-only).
- **Sugestão de argumentos:** `saldo`, `valor`, `extrato`.
- **Sugestão de retorno:** `saldo` e `extrato`.

### Extrato
- Deve receber **argumentos por posição e por nome** (positional-only e keyword-only).
- **Argumentos posicionais:** `saldo`
- **Argumentos nomeados:** `extrato`

---

## Novas Funções
Além das funções existentes, precisamos criar:

### Criar Usuário (Cliente)
- O programa deve armazenar usuários em uma **lista**.
- Cada usuário é composto por:
  - `nome`
  - `data de nascimento`
  - `CPF` (apenas números)
  - `endereço` (formato: `logradouro, numero - bairro - cidade/sigla estado`)
- **Restrições:**
  - Não cadastrar dois usuários com o mesmo CPF.

### Criar Conta Corrente
- O programa deve armazenar contas em uma **lista**.
- Cada conta é composta por:
  - `agência` (fixo: "0001")
  - `número da conta` (sequencial, iniciando em 1)
  - `usuário` (vinculado a um usuário existente)
- **Regras:**
  - Um usuário pode ter mais de uma conta.
  - Uma conta pertence a apenas um usuário.
- **Dica:** Para vincular a conta ao usuário, filtre a lista de usuários pelo CPF informado.

### Funções Extras (Opcional)
Você pode adicionar funções extras, como:
- `listar_contas`  
- `buscar_usuario`  
- `remover_conta`  

---

## Estrutura Sugerida
```python
# Usuários e contas
usuarios = []
contas = []

# Funções
def criar_usuario(...):
    ...

def criar_conta(...):
    ...

def deposito(...):
    ...

def saque(...):
    ...

def extrato(...):
    ...
