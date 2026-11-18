---
tags: [malangotango, arte]
---

# Arte e paletas

![[Documentacao/Imagens/sprites.png|820]]

Os **11 arquivos .aseprite** em `artes/` mantêm as camadas, transparências, tempos, tags e tamanhos enviados. As correções reaproveitam tons da paleta **Gameboy Color** do arquivo. Nos Saposos, os quadros já pintados serviram de modelo para os quadros que ainda trocavam luz e sombra. A banana ganhou brilhos sem azul, e a ponta da língua ficou consistente nas duas direções. A cópia sem correções está em `artes/originais_enviados.zip`.

| Fonte editável | Tamanho e uso |
|---|---|
| `artes/personagem_princi/malango/` | Malango, 16 × 32 px por quadro: duas direções, 22 quadros em cada arquivo, mais a folha de referência. |
| `artes/vilao/saposo/` | Verdes com 18 quadros e vermelhos com 19 em cada direção. Todos com 16 × 32 px. |
| `artes/itens/` | Banana e língua caída: 16 × 16. Chicote estendido: 32 × 16. |
| `game/Malangotango/assets/sprites/vazante/` | PNGs de importação e estados montados no GB Studio. O Guarda deriva do Saposo vermelho, com crista, faixa e paleta próprias. |

| Elemento | Contorno | Tom principal | Luz |
|---|---|---|---|
| Malango | `#000000` | `#833100` | `#FFAD63` |
| Saposo verde | `#000000` | `#008300` | `#7BFF30` |
| Saposo vermelho | `#000000` | `#E60000` | `#FF4200` |
| Banana | `#3A2802` | `#FFDE00` | `#FFFFA5` |
| Língua / chicote | `#5B315B` | `#FF00FE` | `#FE9494` |
| Guarda Rubro | `#000000` | `#E60000` | `#FFDE00` |

**Por que o PNG do projeto é verde?** Ele codifica três intensidades e um índice transparente. A paleta de objeto da cena produz as cores finais do cartucho. Para reexportar, use transparente `#65FF00`, escuro `#071821`, médio `#86C06C` e claro `#E0F8CF`. No painel de sprites do GB Studio, preserve o índice da paleta de cada tile. O jogo usa os estados necessários de cada folha e espelha a direção esquerda durante a execução.

[[Documentacao/Abrir-e-editar|Onde editar]] · [[README|Início]]
