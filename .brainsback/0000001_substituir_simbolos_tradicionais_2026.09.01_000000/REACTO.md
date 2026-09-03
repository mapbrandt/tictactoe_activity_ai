# Proof of Mastery (REACTO)

> Explain it to prove you own it.

**Hard rule**: AI agents must not edit this file and must not draft paste-ready content for it.

## R — The Problem

_Why is this change necessary?_

O jogo usava X e O como símbolos dos jogadores no tabuleiro e nas mensagens. A mudança necessária foi substituir esses símbolos por (gato) para o primeiro jogador e (cachorro) para o segundo, mantendo as regras originais do jogo da velha.

## E — Examples

_One happy path, one edge case._

Caminho normal:

- **Input**: iniciar uma partida e clicar em uma sequência de casas até o jogador (gato) formar uma linha
  **Output**: o tabuleiro mostra (gato) e (cachorro) nas casas jogadas, e a mensagem final indica que o jogador (gato) venceu

Edge case:

- **Input**: clicar em uma casa ocupada
  **Output**: a jogada não é aceita, o valor da casa não muda e o jogo continua normalmente

## A — Approach

_High-level strategy._

Foi basicamente trocar os caracteres de 'X' e 'O' para os emojis e ajustar os testes. A IA acabou também trocando o espaço branco ' ' por '.' para deixar mais claro, eu concordei com a mudança. A lógica do jogo em si não precisou mudar.

## C — Code

_Interesting patterns or trade-offs._

## T — Tests

_How are we verifying this?_

Além dos teste manuais que conferi, os testes automatizados passam e verificam que:

- o jogador inicial é (gato)
- a vez se alterna de forma que (gato) → (cachorro) e (cachorro) → (gato)
- uma jogada válida coloca o emoji correto
- uma casa ocupada não pode ser remarcada
- condições de vitória e empate continuam funcionando

## O — Optimization

_Complexity checks (sometimes don't apply)._

Acho que não houve mudança relevante nesse sentido, continua o mesmo jogo e não tentei melhorar performance nem nada do tipo.
