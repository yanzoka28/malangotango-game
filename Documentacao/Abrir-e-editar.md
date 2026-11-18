---
tags: [malangotango, desenvolvimento]
---

# Abrir, editar e compilar

1. Extraia o ZIP inteiro. Dentro de `segundo-game`, abra `game/Malangotango/Malangotango.gbsproj` no **GB Studio 4.2.2**.
2. Use **Run / ▶** para iniciar pela tela de título. As sete cenas aparecem no editor de mundo. Nas quatro cenas de plataforma, o fundo, as colisões, os atores e a zona de saída são editáveis separadamente.
3. Para gerar outra ROM, use **Game → Export As → Export ROM** (o nome do menu varia com o idioma). A ROM desta entrega também está em `Jogavel/Malangotango.gbc`.
4. No Obsidian, abra a pasta `segundo-game` como cofre. A página [[README]] é o índice e o [[Documentacao/Fluxo-da-campanha.canvas|Canvas]] mostra as transições. Não é preciso instalar plugins da comunidade.

| Quero mudar… | Onde mexer no projeto |
|---|---|
| Texto de entrada | **On Init** da cena correspondente → evento de diálogo. |
| Quantidade de vida e reinício | Inicialização da tela **00 · Início** e da tela **06 · Derrota**. A variável global **Corações** começa em 3. |
| Alcance dos ataques | Evento **B · Golpear** em cada uma das quatro cenas. O soco e o chicote usam projéteis distintos; velocidade, duração e deslocamento inicial determinam o alcance. |
| Conduta e resistência de um inimigo | Atores **Saposo verde**, **Saposo vermelho** e **Guarda Rubro**. A patrulha e a preparação da linguada ficam no update; o golpe de Malango chega ao grupo **2**. O Guarda cai no terceiro acerto. |
| Banana e língua | Atores próprios em cada fase. A banana verifica a vida. A queda de cada vermelho posiciona e habilita sua língua naquele ponto; a coleta muda **Chicote equipado**. |
| Saída e bloqueio final | Gatilho **Saída → ...**, no extremo direito. Na quarta fase ele lê **Guarda Rubro vencido**. |
| Colisões do terreno | Camada de colisão da cena. Chão e obstáculos são sólidos; as plataformas altas só bloqueiam pelo topo. |
| Paletas e cenários | Ativos `assets/backgrounds/vazante/`, `assets/sprites/vazante/` e paletas do projeto em `project/palettes/vazante/`. |

**Dados de uma tentativa.** A fase registra o valor de **Chicote equipado** na entrada. Na derrota, restaura esse valor e enche a vida. As patrulhas, bananas e línguas da fase recomeçam. Os nomes das variáveis são visíveis no editor.

[[Documentacao/Arte-e-paletas|Editar os sprites]] · [[Documentacao/Testes|Conferir o comportamento]] · [[README|Início]]
