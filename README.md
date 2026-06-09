# 🧩 Sudoku CLI (Command Line Interface) em Java

Este é um jogo de Sudoku totalmente funcional baseado em console, desenvolvido em **Java 21**. O projeto foi estruturado utilizando conceitos de Programação Orientada a Objetos (POO), Streams API do Java e manipulação de matrizes para representar o tabuleiro.

O jogo permite iniciar uma partida a partir de configurações pré-definidas via argumentos de inicialização, inserir/remover números, validar o progresso e verificar se o desafio foi concluído corretamente.

---

## 🚀 Tecnologias Utilizadas

*   **Java 21** (Compatível com JDK 21+)
*   **IDE IntelliJ IDEA** (Configurações inclusas na pasta `.idea`)
*   **Java Streams** para manipulação de coleções de forma funcional.

---

## 🛠️ Como Funciona o Tabuleiro

O tabuleiro é uma matriz de $9 \times 9$, composto por 81 posições (`Spaces`). Cada espaço possui:
*   Um valor **esperado** (gabarito).
*   Um valor **atual** (inserido pelo jogador).
*   Uma flag indicando se o valor é **fixo** (números iniciais do jogo que não podem ser alterados).

---

## 🎮 Como Executar o Jogo

O programa inicializa o tabuleiro dinamicamente através dos argumentos de linha de comando (`args`). Cada argumento representa uma célula no formato:
`coluna,linha;valorEsperado,isFixo`

### Exemplo de Inicialização

Para rodar o projeto via terminal, compile os arquivos e passe as 81 posições como argumento. 

Aqui está um exemplo simplificado de comando para iniciar o programa (com algumas posições definidas):

```bash
# Compilar o projeto
javac -d out src/br/com/dio/**/*.java src/br/com/dio/*.java

# Executar passando os argumentos de configuração do tabuleiro
java -cp out br.com.dio.Main "0,0;5,true" "0,1;3,false" "0,2;4,false" ... (até completar as 81 posições)
```

> **Nota:** O programa exige que todas as 81 posições (de `0,0` a `8,8`) sejam passadas nos argumentos para que o jogo seja montado perfeitamente.

---

## 🕹️ Menu de Opções (Como Jogar)

Ao iniciar, o jogo exibirá o seguinte menu interativo no console:

```text
Selecione uma das opções a seguir
1 - Iniciar um novo Jogo
2 - Colocar um novo número
3 - Remover um número
4 - Visualizar jogo atual
5 - Verificar status do jogo
6 - Limpar jogo
7 - Finalizar jogo
8 - Sair
```

### Detalhes das Opções:

1.  **Iniciar um novo Jogo:** Monta o tabuleiro com base nos argumentos passados na inicialização do programa.
2.  **Colocar um novo número:** Solicita a coluna (0-8), a linha (0-8) e o valor (1-9). Se a posição for um número fixo de início, o sistema impedirá a alteração.
3.  **Remover um número:** Limpa o valor digitado em uma coordenada específica (desde que não seja um número fixo).
4.  **Visualizar jogo atual:** Renderiza um lindo tabuleiro formatado em ASCII no console.
5.  **Verificar status do jogo:** Informa se o jogo está *não iniciado*, *incompleto* ou *completo*, além de avisar se há erros (números incorretos de acordo com o gabarito).
6.  **Limpar jogo:** Reseta todo o seu progresso, mantendo apenas os números fixos iniciais (pede confirmação "sim" ou "não").
7.  **Finalizar jogo:** Valida se você preencheu todas as casas corretamente. Se sim, exibe a mensagem de parabéns e encerra a partida.
8.  **Sair:** Fecha a aplicação.
---

## 📝 Licença

Este projeto foi desenvolvido para fins educacionais pela DIO, documentado por mim.
```

---
