# Roteiro de Desenvolvimento: Ecos do Coliseu

[cite_start]Este documento contém o planejamento estratégico, passos de desenvolvimento e a lista de assets necessários para a implementação do **Trabalho II de Computação Gráfica (IFSUL)**[cite: 3, 4]. [cite_start]O objetivo é garantir o cumprimento de 100% dos requisitos exigidos no enunciado[cite: 6].

---

## Roteiro de Desenvolvimento

### Fase 1: Modelagem e Texturização (Blender)
* [cite_start][ ] **Passo 1.1:** Finalizar a modelagem da **Casa 1 (Ludus - Escola de Gladiadores)**, garantindo que ela possua pelo menos **3 cômodos** (ex: Dormitório, Arsenal e Refeitório) [cite: 14, 15] [cite_start]e **duas portas**[cite: 17].
* [cite_start][ ] **Passo 1.2:** Modelar a **Casa 2 (Residência Comum)** com uma planta diferente da primeira casa[cite: 14].
* [cite_start][ ] **Passo 1.3:** Abrir os vãos de portas e janelas em ambas as estruturas[cite: 17]. 
  > **⚠️ IMPORTANTE:** A folha da porta (a parte que gira) deve ser um objeto separado da parede, e o seu *Pivot Point* (ponto de origem) deve ser movido para a lateral (onde ficam as dobradiças) para que a rotação funcione corretamente no Unity.
* [cite_start][ ] **Passo 1.4:** Modelar os **6 objetos adicionais** temáticos para compor o cenário[cite: 18].
* [cite_start][ ] **Passo 1.5:** Realizar o mapeamento UV de todos os modelos para evitar texturas esticadas[cite: 20]. [cite_start]Aplicar a textura de papel de parede/mural romano em pelo menos uma das casas[cite: 16, 20].
* [cite_start][ ] **Passo 1.6:** Exportar todos os modelos gerados no formato `.FBX`[cite: 19].

### Fase 2: Configuração e Física do Cenário (Unity - Cena 1)
* [cite_start][ ] **Passo 2.1:** Importar o pacote oficial **Starter Assets - Character Controller** para habilitar a navegação em primeira pessoa[cite: 26].
* [cite_start][ ] **Passo 2.2:** Criar o terreno da **Cena 1 (Vila Romana)** e delimitá-lo utilizando barreiras naturais (montanhas) ou construídas (muralhas)[cite: 25].
* [cite_start][ ] **Passo 2.3:** Importar os arquivos `.FBX` criados no Blender[cite: 23].
* [cite_start][ ] **Passo 2.4:** Configurar os colisores: aplicar **Mesh Collider** nas estruturas das casas (paredes) e **Box Collider** nas portas e objetos decorativos[cite: 27].
* [cite_start][ ] **Passo 2.5:** Criar a **Animação Geométrica** (Requisito 4d) em uma coluna ou estátua central utilizando o sistema de *Animation* do Unity, aplicando transformações de rotação e translação[cite: 37].

### Fase 3: Interface e Programação C# (Unity - Cena 1)
* [cite_start][ ] **Passo 3.1:** Desenvolver o **Menu Inicial** (com opções para iniciar a aplicação ou sair) utilizando o Unity UI[cite: 29, 30].
* [cite_start][ ] **Passo 3.2:** Desenvolver o **Menu de Pausa/Saída** acessível durante a gameplay[cite: 30].
* [cite_start][ ] **Passo 3.3:** Implementar o script C# de **Abertura e Fechamento de Portas** baseado na interação e proximidade do jogador (*triggers*)[cite: 33, 36].
* [cite_start][ ] **Passo 3.4:** Criar a interface 2D do **Quiz de História** (Canvas contendo caixas de texto e botões para as alternativas)[cite: 29].
* [cite_start][ ] **Passo 3.5:** Implementar o script C# que **restringe o acesso à Casa 1**[cite: 35]. [cite_start]A porta só deve ser destrancada (e a animação geométrica ativada) após o jogador resolver corretamente o desafio do Quiz na UI[cite: 35, 37].

### Fase 4: A Arena e Recursos Avançados (Unity - Cena 2)
* [cite_start][ ] **Passo 4.1:** Criar a **Cena 2 (O Coliseu)** com um terreno circular cercado pelas arquibancadas da arena[cite: 22, 25].
* [cite_start][ ] **Passo 4.2:** Configurar o script de **Transição de Cenas** na Cena 1, liberando o gatilho de mudança para a Cena 2 somente após a conclusão dos objetivos da vila[cite: 34].
* [cite_start][ ] **Passo 4.3:** Posicionar o NPC do Gladiador no centro da arena para interagir com o jogador por meio de um novo painel de perguntas históricas (objetivo educacional da Cena 2)[cite: 6, 29].
* [cite_start][ ] **Passo 4.4:** Integrar os **4 Recursos Extras** do Unity que não foram abordados em aula para valorizar o projeto[cite: 28]:
  1. *Sistema de Partículas (Particle System):* Efeito de fogo/fumaça nas tochas do Coliseu.
  2. *Inteligência Artificial (NavMesh):* Fazer o gladiador caminhar ou patrulhar a arena de forma autônoma.
  3. *Efeitos Visuais (Post-Processing):* Filtro de cor caloroso/sépia para dar identidade de época ao jogo.
  4. *Áudio 3D (Audio Source):* Som tridimensional da torcida clamando dentro do Coliseu.

---

## Lista de Objetos (Assets) Necessários

### 1. Modelagem Própria (Blender)
[cite_start]Estes são os objetos obrigatórios que o grupo deve construir do zero e apresentar o mapeamento de texturas[cite: 13, 52]:

* [cite_start]**Casa 1 (Ludus):** Estrutura residencial com mais de 3 cômodos divididos, com duas aberturas de portas e texturização interna de papel de parede[cite: 14, 15, 16, 17].
* [cite_start]**Casa 2 (Casa Simples):** Estrutura menor com planta arquitetônica totalmente diferente da primeira[cite: 14].
* [cite_start]**6 Objetos Adicionais da Época[cite: 18]:**
    1. *Gladius* (Espada curta romana)
    2. *Scutum* (Escudo retangular romano)
    3. [cite_start]*Coluna/Pilar Romano* (Objeto que sofrerá a animação geométrica) [cite: 37]
    4. [cite_start]*Baú de Madeira Antigo* (Para decorar o arsenal) [cite: 16]
    5. [cite_start]*Mesa de Madeira Rústica* (Para a cozinha) [cite: 16]
    6. [cite_start]*Banco ou Cadeira de Pedra* (Para a sala de estar) [cite: 16]

### 2. Modelos Prontos (Importados da Internet)
[cite_start]Modelos tridimensionais permitidos para complementar a composição dos cenários[cite: 24]:

* [cite_start]**Muralhas de Pedra Interconectadas:** Para delimitar o espaço de navegação da Cena 1[cite: 25].
* [cite_start]**Estrutura de um Coliseu / Arquibancadas:** Para delimitar a área de navegação da Cena 2[cite: 25].
* [cite_start]**Personagem Gladiador / Soldado Romano:** Modelo 3D com rig para ser utilizado com o sistema de IA[cite: 28].
* [cite_start]**Tochas de Parede:** Modelos simples para servirem de base para as partículas de fogo[cite: 28].
