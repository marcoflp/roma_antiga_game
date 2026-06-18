# Roteiro de Desenvolvimento: Ecos do Coliseu

Este documento contém o planejamento estratégico, passos de desenvolvimento e a lista de assets necessários para a implementação do **Trabalho II de Computação Gráfica (IFSUL)**. O objetivo é garantir o cumprimento de 100% dos requisitos exigidos no enunciado.

---

## Roteiro de Desenvolvimento

### Fase 1: Modelagem e Texturização (Blender)
* [ ] **Passo 1.1:** Finalizar a modelagem da **Casa 1 (Ludus - Escola de Gladiadores)**, garantindo que ela possua pelo menos **3 cômodos** (ex: Dormitório, Arsenal e Refeitório) e **duas portas**.
* [ ] **Passo 1.2:** Modelar a **Casa 2 (Residência Comum)** com uma planta diferente da primeira casa.
* [ ] **Passo 1.3:** Abrir os vãos de portas e janelas em ambas as estruturas. 
  > **⚠️ IMPORTANTE:** A folha da porta (a parte que gira) deve ser um objeto separado da parede, e o seu *Pivot Point* (ponto de origem) deve ser movido para a lateral (onde ficam as dobradiças) para que a rotação funcione corretamente no Unity.
* [ ] **Passo 1.4:** Modelar os **6 objetos adicionais** temáticos para compor o cenário.
* [ ] **Passo 1.5:** Realizar o mapeamento UV de todos os modelos para evitar texturas esticadas. Aplicar a textura de papel de parede/mural romano em pelo menos uma das casas.
* [ ] **Passo 1.6:** Exportar todos os modelos gerados no formato `.FBX`.

### Fase 2: Configuração e Física do Cenário (Unity - Cena 1)
* [ ] **Passo 2.1:** Importar o pacote oficial **Starter Assets - Character Controller** para habilitar a navegação em primeira pessoa.
* [ ] **Passo 2.2:** Criar o terreno da **Cena 1 (Vila Romana)** e delimitá-lo utilizando barreiras naturais (montanhas) ou construídas (muralhas).
* [ ] **Passo 2.3:** Importar os arquivos `.FBX` criados no Blender.
* [ ] **Passo 2.4:** Configurar os colisores: aplicar **Mesh Collider** nas estruturas das casas (paredes) e **Box Collider** nas portas e objetos decorativos.
* [ ] **Passo 2.5:** Criar a **Animação Geométrica** (Requisito 4d) em uma coluna ou estátua central utilizando o sistema de *Animation* do Unity, aplicando transformações de rotação e translação.

### Fase 3: Interface e Programação C# (Unity - Cena 1)
* [ ] **Passo 3.1:** Desenvolver o **Menu Inicial** (com opções para iniciar a aplicação ou sair) utilizando o Unity UI.
* [ ] **Passo 3.2:** Desenvolver o **Menu de Pausa/Saída** acessível durante a gameplay.
* [ ] **Passo 3.3:** Implementar o script C# de **Abertura e Fechamento de Portas** baseado na interação e proximidade do jogador (*triggers*).
* [ ] **Passo 3.4:** Criar a interface 2D do **Quiz de História** (Canvas contendo caixas de texto e botões para as alternativas).
* [ ] **Passo 3.5:** Implementar o script C# que **restringe o acesso à Casa 1**. A porta só deve ser destrancada (e a animação geométrica ativada) após o jogador resolver corretamente o desafio do Quiz na UI.

### Fase 4: A Arena e Recursos Avançados (Unity - Cena 2)
* [ ] **Passo 4.1:** Criar a **Cena 2 (O Coliseu)** com um terreno circular cercado pelas arquibancadas da arena.
* [ ] **Passo 4.2:** Configurar o script de **Transição de Cenas** na Cena 1, liberando o gatilho de mudança para a Cena 2 somente após a conclusão dos objetivos da vila.
* [ ] **Passo 4.3:** Posicionar o NPC do Gladiador no centro da arena para interagir com o jogador por meio de um novo painel de perguntas históricas (objetivo educacional da Cena 2).
* [ ] **Passo 4.4:** Integrar os **4 Recursos Extras** do Unity que não foram abordados em aula para valorizar o projeto:
  1. *Sistema de Partículas (Particle System):* Efeito de fogo/fumaça nas tochas do Coliseu.
  2. *Inteligência Artificial (NavMesh):* Fazer o gladiador caminhar ou patrulhar a arena de forma autônoma.
  3. *Efeitos Visuais (Post-Processing):* Filtro de cor caloroso/sépia para dar identidade de época ao jogo.
  4. *Áudio 3D (Audio Source):* Som tridimensional da torcida clamando dentro do Coliseu.

---

## Lista de Objetos (Assets) Necessários

### 1. Modelagem Própria (Blender)
Estes são os objetos obrigatórios que o grupo deve construir do zero e apresentar o mapeamento de texturas:

* **Casa 1 (Ludus):** Estrutura residencial com mais de 3 cômodos divididos, com duas aberturas de portas e texturização interna de papel de parede.
* **Casa 2 (Casa Simples):** Estrutura menor com planta arquitetônica totalmente diferente da primeira.
* **6 Objetos Adicionais da Época:**
- [x] *Gladius* (Espada curta romana)
- [x] *Scutum* (Escudo retangular romano)
- [x] *Coluna/Pilar Romano* (Objeto que sofrerá a animação geométrica)
- [x] *Baú de Madeira Antigo* (Para decorar o arsenal)
- [ ] *Mesa de Madeira Rústica* (Para a cozinha)
- [ ] *Banco ou Cadeira de Pedra* (Para a sala de estar)

### 2. Modelos Prontos (Importados da Internet)
Modelos tridimensionais permitidos para complementar a composição dos cenários:

* **Muralhas de Pedra Interconectadas:** Para delimitar o espaço de navegação da Cena 1.
* **Estrutura de um Coliseu / Arquibancadas:** Para delimitar a área de navegação da Cena 2.
* **Personagem Gladiador / Soldado Romano:** Modelo 3D com rig para ser utilizado com o sistema de IA.
* **Tochas de Parede:** Modelos simples para servirem de base para as partículas de fogo.
