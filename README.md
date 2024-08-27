# Jogo da Velha - Android

Este projeto é um aplicativo de Jogo da Velha desenvolvido em Kotlin, utilizando Android Studio e Firebase Firestore para funcionalidade online. O aplicativo permite que os jogadores disputem partidas offline no mesmo dispositivo ou online com sincronização em tempo real.

## Funcionalidades

- **Jogo Offline**: Dois jogadores podem jogar localmente no mesmo dispositivo.
- **Jogo Online**: Dois jogadores podem jogar em dispositivos diferentes com o estado do jogo sincronizado via Firebase.
- **Interface Intuitiva**: Design simples e fácil de usar.

## Estrutura do Projeto

### Layouts

1. **activity_main.xml**:
    - Layout principal onde o jogador escolhe entre jogar offline, criar uma sala online ou entrar em uma sala online.
    - Contém botões e campos de entrada para navegação.

2. **activity_game.xml**:
    - Layout da tela de jogo.
    - Contém o tabuleiro do jogo (grade de 3x3) e a interface de controle do jogo.

### Classes Kotlin

1. **MainActivity**:
    - Gerencia a navegação inicial do aplicativo.
    - Possibilita o início de partidas offline ou online.
    - Conecta o aplicativo ao Firebase para criação e entrada em salas de jogo online.

2. **GameActivity**:
    - Gerencia a lógica do jogo.
    - Implementa a interação dos jogadores e atualiza a interface do usuário conforme o jogo progride.
    - Verifica as condições de vitória ou empate e sincroniza o estado do jogo com o Firebase.

3. **GameModel**:
    - Modelo de dados representando o estado do jogo.
    - Contém informações sobre o ID do jogo, posições preenchidas, vencedor, status do jogo e jogador atual.

4. **GameData**:
    - Responsável por gerenciar o estado do jogo em tempo real.
    - Integração com Firebase Firestore para salvar e recuperar o estado do jogo.

5. **GameStatus**:
    - Enumeração que define os possíveis estados do jogo: `CREATED`, `JOINED`, `INPROGRESS`, `FINISHED`.

## Como Jogar

### Modo Offline
1. Na tela inicial, clique em "Jogar offline".
2. O jogo será iniciado, e os jogadores podem alternar suas jogadas tocando nos botões do tabuleiro.

### Modo Online
1. Para criar uma sala online, clique em "Criar sala online". Um ID será gerado.
2. Compartilhe o ID com outro jogador.
3. O segundo jogador deve inserir o ID e clicar em "Iniciar partida online".
4. O jogo será sincronizado entre os dispositivos e jogado em tempo real.

## Configuração do Projeto

### Requisitos

- **Android Studio**: Versão 4.0 ou superior.
- **Kotlin**: Versão 1.3 ou superior.
- **Firebase**: Projeto configurado com Firestore.

### Instruções

1. Clone este repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
