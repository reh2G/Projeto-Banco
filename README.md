# Meu primeiro projeto na graduação - Sistema Bancario em Python

## Descricao

Projeto desenvolvido na disciplina CC1612 - FUNDAMENTOS DE ALGORITMOS (graduacao).
Implementa um sistema bancario simples em Python com persistencia em arquivos .txt.

Funcionalidades:

- Criar conta
- Apagar conta
- Debitar (com tarifa)
- Depositar
- Mostrar saldo
- Mostrar extrato

## Tipos de conta

Tipo 1 - Salario: Tarifa 5%, limite negativo R$ 0,00
Tipo 2 - Comum: Tarifa 3%, limite negativo ate -R$ 500,00
Tipo 3 - Plus: Tarifa 1%, limite negativo ate -R$ 5.000,00

## Estrutura de arquivos

Cada conta gera uma sequencia de arquivos:

    CPF(0).txt   -> criacao da conta
    CPF(1).txt   -> primeira transacao
    CPF(2).txt   -> segunda transacao
    ...

Conteudo de cada arquivo (uma linha por campo):

1. Nome
2. CPF
3. Senha
4. Saldo apos operacao
5. Tipo (1,2,3)
6. Valor da operacao
7. Tipo da acao (Criar Conta, Debito, Deposito)
8. Data e hora
9. Tarifa

## Como executar

Requisitos: Python 3.x

Passos:

1. Baixe o arquivo projeto1.py
2. No terminal, va ate a pasta do arquivo
3. Execute: python projeto1.py
4. Siga o menu interativo.

## Estrutura do codigo

- criarConta(): Cria novo cliente e arquivo inicial
- apagarConta(): Remove todos os arquivos da conta
- debitar(): Aplica tarifa, verifica limite e gera novo arquivo
- depositar(): Atualiza saldo com deposito
- saldo(): Exibe saldo atual (ultimo arquivo)
- extrato(): Mostra historico (do mais recente ao mais antigo)
- main(): Menu principal e direcionamento

## Exemplo de uso

Ao executar, o menu exibe:

    1 - Criar nova conta
    2 - Apagar conta
    3 - Debitar
    4 - Deposito
    5 - Saldo
    6 - Extrato
    0 - Sair

Apos criar uma conta com CPF 12345678900, serao gerados:

    12345678900(0).txt   (criacao)
    12345678900(1).txt   (primeira movimentacao)

Exemplo de extrato:

    Nome: Joao Silva
    CPF: 12345678900
    Conta: Comum

    15/05/2025 14:23:01 | - 100.00 ; Tarifa: 3.00 -> Saldo: 397.00
    14/05/2025 09:15:42 | + 500.00 ; Tarifa: 0.00 -> Saldo: 500.00

## Autoria

- Disciplina: CC1612 - FUNDAMENTOS DE ALGORITMOS
- Linguagem: Python 3
- Ano: 2022
