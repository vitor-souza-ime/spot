# Spot Robot Controller - Webots

Este repositório contém um controlador para o robô quadrúpede **Spot** no ambiente de simulação **Webots**. O código implementa movimentos como levantar, sentar e dar a pata, demonstrando a capacidade de controlar articulações individuais de forma suave e contínua.

Repositório: [https://github.com/vitor-souza-ime/spot](https://github.com/vitor-souza-ime/spot)

---

## Arquivos

- `main.c`: controlador principal do Spot, implementando as funções de movimento e o loop de execução contínuo.

---

## Funcionalidades

O controlador implementa as seguintes primitivas de movimento:

1. **Stand Up (Levantar)**: Transição para postura ereta.
2. **Sit Down (Sentar)**: Postura intermediária, mantendo estabilidade.
3. **Give Paw (Dar a Pata)**: Movimento oscilatório de uma pata dianteira combinado com estabilização postural.

O algoritmo central utilizado é a função `movement_decomposition`, que realiza interpolação linear temporal entre a posição atual das articulações e a posição-alvo desejada, garantindo movimentos suaves e contínuos.

---

## Dependências

- [Webots](https://cyberbotics.com/) versão 2023 ou superior
- Robô Spot disponível na biblioteca de modelos do Webots

---

## Estrutura do Código

- **Dispositivos**: motores (`motors`), câmeras (`cameras`) e LEDs (`leds`) do Spot são inicializados automaticamente.
- **Loop de Controle**: o robô executa as primitivas de movimento em sequência contínua, com intervalos de pausa programados.
- **Funções de Movimento**:
  - `stand_up(double duration)`
  - `sit_down(double duration)`
  - `give_paw()`

---

## Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/vitor-souza-ime/spot.git
````

2. Abra o Webots e carregue o mundo contendo o robô Spot.
3. Configure o controlador do robô para usar `main.c`.
4. Execute a simulação e observe o robô realizando os movimentos definidos.

---

## Licença

O código é distribuído sob a **Apache License 2.0**, conforme especificado pelo Webots.
