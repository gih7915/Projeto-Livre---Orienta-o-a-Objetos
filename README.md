# Projeto-Livre---Orienta-o-a-Objetos
# Controle Financeiro da Gih

## Definição do problema

Este projeto tem como objetivo desenvolver um sistema para controle financeiro pessoal que permita ao usuário registrar receitas e despesas, consultar o saldo atual e gerenciar suas transações financeiras de forma simples e eficiente. O sistema deve possibilitar adicionar, visualizar e excluir transações, além de salvar e carregar os dados localmente.

---

## Casos de Uso

1. **Adicionar Transação**  
   O usuário pode adicionar uma nova receita ou despesa, informando descrição, valor, data, categoria e tipo (receita ou despesa).

2. **Visualizar Transações**  
   O usuário pode visualizar uma lista de todas as transações cadastradas, mostrando descrição, valor, tipo e categoria.

3. **Excluir Transação**  
   O usuário pode excluir uma transação previamente adicionada, caso se arrependa ou queira corrigir um erro.

4. **Visualizar Saldo**  
   O sistema calcula e exibe o saldo atual, considerando receitas como valores positivos e despesas como valores negativos.

5. **Salvar Dados**  
   O sistema salva as transações em arquivo local usando serialização (pickle), para persistência entre execuções.

6. **Carregar Dados**  
   Ao iniciar, o sistema carrega as transações salvas previamente, recuperando o estado anterior.

---

## Tecnologias Utilizadas

- Linguagem Python  
- Framework Flask (interface web)  
- Serialização com pickle  
- Front-end HTML, CSS e JavaScript (simples e responsivo)

---

## Modelagem Orientada a Objetos

- Classes principais: `Transacao` (superclasse abstrata), `Receita`, `Despesa`, `Carteira`, `Categoria`  
- Uso de herança: Receita e Despesa herdam de Transacao  
- Polimorfismo: método `get_valor()` com comportamento específico em Receita e Despesa  
- Composição: Carteira contém várias transações  
- Associação: Categoria associada às transações  

---

## Instruções para execução

1. Instalar dependências com `pip install flask`  
2. Executar `python main.py`  
3. Acessar `http://localhost:5000` no navegador

---

