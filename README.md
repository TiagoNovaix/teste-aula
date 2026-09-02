# Aurora Orbital — Cena 3D com Three.js

## Integrantes

> **PREENCHER ANTES DA ENTREGA:** nomes completos de todos os integrantes do grupo.

- Integrante 1: ______________________________
- Integrante 2: ______________________________
- Integrante 3: ______________________________
- Integrante 4: ______________________________
- Integrante 5: ______________________________

## Descrição da cena

O projeto apresenta uma composição tridimensional generativa chamada **Aurora Orbital**. A cena possui uma escultura abstrata central editável, eixos cartesianos X, Y e Z, piso, grade, anéis orbitais, partículas, fragmentos geométricos, iluminação e fundo procedural. O usuário pode alterar a geometria, o material, as cores e as transformações do objeto principal e exportar a composição como imagem PNG.

## Geometrias utilizadas

- `PlaneGeometry`: plano de fundo que acompanha a câmera.
- `CircleGeometry`: piso circular da composição.
- `CylinderGeometry`: hastes dos eixos X, Y e Z.
- `ConeGeometry`: pontas dos eixos e opção de forma central.
- `TorusGeometry`: anéis orbitais.
- `TetrahedronGeometry`: fragmentos distribuídos pela cena.
- `IcosahedronGeometry`: núcleo luminoso e opção de forma central.
- `SphereGeometry`: componentes da base e opção de forma central.
- `BoxGeometry`: opção de cubo para o objeto central.
- `TorusKnotGeometry`: opção de nó toroidal.
- `BufferGeometry`: armazenamento eficiente das posições das partículas.

## Transformações utilizadas

### `position`

- A câmera é posicionada em `(7.4, 5.6, 9.2)` para enquadrar a composição.
- As luzes são posicionadas em pontos diferentes para iluminar o objeto.
- Os 34 fragmentos recebem coordenadas X, Y e Z próprias.
- O objeto central pode ser deslocado nos três eixos pelos controles do painel.

### `rotation`

- O piso recebe rotação de `-90°` no eixo X para ficar horizontal.
- Os três anéis orbitais possuem rotações iniciais diferentes.
- Os fragmentos recebem rotações aleatórias e continuam girando durante a animação.
- O objeto central pode ser rotacionado nos eixos X, Y e Z.

### `scale`

- O objeto central recebe escala uniforme controlada por um slider.
- As etiquetas dos eixos e a aura luminosa utilizam escalas próprias.
- O contorno do objeto é ligeiramente ampliado para aparecer sobre a superfície.

## Principais conceitos do Three.js

- `THREE.Scene`: contém todos os elementos tridimensionais.
- `THREE.PerspectiveCamera`: define o ponto de vista e a perspectiva.
- `THREE.WebGLRenderer`: renderiza a cena no elemento `<canvas>`.
- `THREE.Mesh`: combina uma geometria e um material.
- `scene.add()`: adiciona câmera, luzes, objetos e grupos à cena.
- `requestAnimationFrame()`: atualiza continuamente movimento e renderização.

## Como executar

O projeto utiliza módulos JavaScript e deve ser aberto por um servidor local.

### Opção 1 — Live Server

1. Abra a pasta do projeto no Visual Studio Code.
2. Instale a extensão **Live Server**.
3. Clique com o botão direito em `index.html`.
4. Escolha **Open with Live Server**.

### Opção 2 — Python

Na pasta do projeto, execute:

```bash
python -m http.server 4173
```

Depois acesse `http://localhost:4173` no navegador.

## Estrutura do projeto

```text
teste-aula/
├── index.html
└── README.md
```

## Observações para a apresentação

- Mostrar o painel alterando `position`, `rotation` e `scale`.
- Explicar que o objeto central é um `Mesh` formado por geometria e material.
- Mostrar os fragmentos como exemplo de múltiplos objetos em coordenadas diferentes.
- Explicar que `animate()` atualiza os objetos e renderiza cada quadro.
- Todos os integrantes devem estudar os comentários do `index.html` e compreender os recursos avançados usados.
