# Cheat Sheet AI102 - Visão Computacional

## Visão Personalizada do Azure em Dispositivos de Borda

- Tipos de modelo:
  - Geral -> Cenários diversos
  - Comida -> Aplicações de gastronomia
  - Compacto -> IoT, drones, Smartphone sem internet
  - Varejo -> Lojas e inventários
- Quando usar cada um?
  - Dispositivos com internet -> Geral, comida, varejo
  - Dispositivos em internet -> Compacto

## Azure Face API (Detecção de Rostos Desfocados)

- Modelos do Face API:
  - Detection 01 - modelo mais antigo, menos preciso para rostos desfocados ou em condições adversas
  - Detection 02 - modelo mais recente e avançado, com melhor desempenho em imagens de baixa qualidade
- Palavras chave:
  - Detection 02: Rostos desfocados, imagens de baixa qualidade, condições adversas
- Armadilhas
  - Detection 1 -> Sempre incorreto
  - Usar modelo personalizado -> Face api não tem modelo personalizado
 