# Doctor N.1348

Aventura medieval de diagnóstico ambientada na **Peste Negra**, feita numa **Game Jam de 1 semana** (5 a 12 de dezembro de 2025) por uma equipa de 5 pessoas, em **Unity / C#**.

O jogador é o médico da aldeia: observa os sintomas de cada doente, prepara o tratamento com ingredientes e gere moedas, inventário e a população da aldeia.

Jogo e vídeo de gameplay: [portefólio](https://rafael-dev-lime.vercel.app/) · [itch.io](https://rafapincarvalho.itch.io/)

## O meu papel
Programação. Este repositório contém **apenas os scripts C#** do jogo (a arte e o áudio são da equipa e não estão aqui).

## O que o código faz
| Sistema | Scripts |
|---|---|
| **Doentes e doenças**: cada doente recebe doenças aleatórias e indicadores visuais (febre, nódoas, muco, suor); cada doença tem a sua lista de tratamentos (gripe, fadiga, tuberculose, erisipela, infeção da pele, peste negra) | `PatientController`, `CharacterManager`, `CharacterSpawner` |
| **Preparação do tratamento**: arrastar ingredientes para a taça (drag and drop com deteção de clique vs. arrasto) | `DragAndDrop`, `DragBowl`, `Bowl`, `TreatmentArea` |
| **Estado do jogo**: moedas, população, inventário inicial (padrão Singleton, persiste entre cenas) | `GameManager`, `Inventory`, `InventoryUI`, `ItemData` (ScriptableObject) |
| **Loja**: comprar ingredientes com moedas, bloqueio de input quando a loja está aberta | `ShopManager`, `Shop`, `ShopItemButton`, `ShopItemUI`, `InputLock` |
| **Isolar ou mandar embora**: regras de recompensa e perda de população (ex.: isolar um doente com peste negra dá moedas mas reduz a população) | `IsolationManager`, `SendAwayManager` |
| **Diálogos e menus** | `DialogueUI`, `DialogueButtons`, `MainMenu`, `SettingsMenu`, `PotionMenu` |
| **Som** | `FootstepIntro`, `IngredientSound` |

## Tecnologias
Unity · C# · TextMesh Pro · ScriptableObjects

## Autor
Rafael Carvalho · [LinkedIn](https://www.linkedin.com/in/rafaelcarvalho2005/) · [Portefólio](https://rafael-dev-lime.vercel.app/)
