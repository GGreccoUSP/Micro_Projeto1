# Entrega final - Projeto 1
O projeto foi desenvolvido e testado na plataforma EdSim. Ele implementa, em Assembly para o microcontrolador 8051, o controle e display do sentido de rotação de um motor com contagem de voltas.

O sistema funciona a partir da utilização de pontos-chave:
- SW0 (P2.0): alterna o sentido do motor (toggle)
- P3.0 / P3.1: realiza o controle do motor
- Timer1: contador de pulsos (voltas)
- Display 7 segmentos (P1): mostra valores de 0 a 9 com base na quantidade de voltas
- LED7 (P1.7): mostra o sentido de rotação do motor (P1.7 = 1 : sentido horário ; P1.7 = 0 : sentido anti-horário)

Além disso, algumas considerações a serem feitas a respeito do código final:

- Timer 1 opera como contador de eventos externos, como apresentado no checkpoint 3
- O display de 7 segmentos é limitado a valores de 0 a 9, assim, quando a contagem de voltas passa de 9 o display retorna para 0
- A entrada SW0 do sistema funciona como um toggle, atuando sempre que esta estiver em nível lógico alto. Ou seja, sempre que o botão 0 do simulador é pressionado, as ações abaixo são realizadas:
    - O motor inverte de sentido
    - A contagem do display é reiniciada assim que a volta do motor for completada
    - O LED7 (ponto no display de 7 segmentos) é atualizado de acordo com o sentido de rotação atual do motor

Por fim, vale ressaltar que a única mudança feita em relação ao checkpoint anterior foi de implementar a entrada P1.7 do display de 7 segmentos no código, esse que se encontra no arquivo src.

-- Giovanne Tomaszewski Grecco
-- n° usp: 16228852
