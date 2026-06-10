# 🏦 Banco QuemPoupaTem (meu primeiro projeto na graduação) - Sistema Bancário em Python

## 📌 Descrição

Projeto desenvolvido na disciplina **CC1612 - FUNDAMENTOS DE ALGORITMOS** (graduação).  
Implementa um sistema bancário simples em Python com persistência em arquivos .txt.

### ✅ Funcionalidades

- 🆕 Criar conta
- 🗑️ Apagar conta
- 💸 Debitar (com tarifa)
- 💰 Depositar
- 📊 Mostrar saldo
- 📜 Mostrar extrato

---

## 🗂️ Tipos de conta

- **Tipo 1 - Salário:** Tarifa 5%, limite negativo R$ 0,00
- **Tipo 2 - Comum:** Tarifa 3%, limite negativo até -R$ 500,00
- **Tipo 3 - Plus:** Tarifa 1%, limite negativo até -R$ 5.000,00

---

## 📁 Estrutura de arquivos

Cada conta gera uma sequência de arquivos:

    CPF(0).txt   -> criação da conta
    CPF(1).txt   -> primeira transação
    CPF(2).txt   -> segunda transação
    ...

Conteúdo de cada arquivo (uma linha por campo):

1. Nome
2. CPF
3. Senha
4. Saldo após operação
5. Tipo (1, 2, 3)
6. Valor da operação
7. Tipo da ação (Criar Conta, Débito, Depósito)
8. Data e hora
9. Tarifa

---

## 🖥️ Como executar

**Requisitos:** Python 3.x

**Passos:**

1. Baixe o arquivo `projeto1-comentado.py`
2. No terminal, vá até a pasta do arquivo
3. Execute: `python projeto1-comentado.py`
4. Siga o menu interativo.

---

## 🧠 Estrutura do código

- `criarConta()` → Cria novo cliente e arquivo inicial
- `apagarConta()` → Remove todos os arquivos da conta
- `debitar()` → Aplica tarifa, verifica limite e gera novo arquivo
- `depositar()` → Atualiza saldo com depósito
- `saldo()` → Exibe saldo atual (último arquivo)
- `extrato()` → Mostra histórico (do mais recente ao mais antigo)
- `main()` → Menu principal e direcionamento

---

## 📋 Exemplo de uso

Ao executar, o menu exibe:

    1 - Criar nova conta
    2 - Apagar conta
    3 - Debitar
    4 - Depósito
    5 - Saldo
    6 - Extrato
    0 - Sair

Após criar uma conta com CPF `12345678900`, serão gerados:

    12345678900(0).txt   (criação)
    12345678900(1).txt   (primeira movimentação)

Exemplo de extrato:

    Nome: João Silva
    CPF: 12345678900
    Conta: Comum

    15/05/2025 14:23:01 | - 100.00 ; Tarifa: 3.00 -> Saldo: 397.00
    14/05/2025 09:15:42 | + 500.00 ; Tarifa: 0.00 -> Saldo: 500.00

---

## 👨‍🎓 Autoria

- **Disciplina:** CC1612 - FUNDAMENTOS DE ALGORITMOS
- **Instituição:** Centro Universitário FEI
- **Período:** Graduação
- **Linguagem:** Python 3
- **Ano:** 2021
