# Mini Cidade 3D

## Integrantes

- **Integrante 1:** Tiago Abreu Novaes — 2625924
- **Integrante 2:** Raphael Galiaço da Cunha — 2631785
- **Integrante 3:** Herick Luccas Lemos Rocha — 2663928

## Descrição da cena

O projeto apresenta uma **mini cidade futurista estática**, criada com JavaScript e Three.js. A composição possui uma torre central com cobertura e domo, três prédios, dois painéis solares, três árvores, uma rua e um terreno. Os eixos X, Y e Z e uma grade auxiliam na visualização do espaço tridimensional.

A cena foi planejada para demonstrar de forma direta os requisitos da atividade. Ela não possui animação: o desenho é realizado uma vez ao carregar a página e novamente apenas quando o tamanho da janela muda.

## Tecnologias utilizadas

- HTML5;
- CSS3;
- JavaScript com módulos ES;
- Three.js.

## Geometrias utilizadas

- `PlaneGeometry`: terreno;
- `BoxGeometry`: rua, prédios, torre e painéis solares;
- `ConeGeometry`: cobertura da torre;
- `SphereGeometry`: domo e copas das árvores;
- `CylinderGeometry`: antena e troncos das árvores.

## Transformações utilizadas

- `position`: posiciona os elementos em diferentes coordenadas dos eixos X, Y e Z;
- `rotation`: rotaciona o terreno, a rua, a cobertura, prédios, painéis solares e um tronco;
- `scale`: altera as proporções da torre, do domo, de prédios e das copas das árvores.

## Objetos visíveis

A composição possui **17 objetos do tipo `THREE.Mesh`**, portanto supera o mínimo de 10 objetos 3D visíveis:

1. terreno da cidade;
2. rua principal;
3. corpo da torre central;
4. cobertura da torre;
5. domo de observação;
6. antena;
7. prédio esquerdo;
8. prédio direito;
9. prédio do fundo;
10. painel solar esquerdo;
11. painel solar direito;
12. tronco da árvore esquerda;
13. copa da árvore esquerda;
14. tronco da árvore direita;
15. copa da árvore direita;
16. tronco da árvore do fundo;
17. copa da árvore do fundo.

## Conferência dos requisitos

| Requisito | Como foi atendido |
| --- | --- |
| 10 objetos 3D visíveis | A cena possui 17 objetos `Mesh`. |
| 2 tipos de geometria | Foram utilizados 5 tipos de geometria. |
| 4 cores diferentes | Há pelo menos 8 cores nos materiais. |
| Coordenadas X, Y e Z diferentes | Os objetos usam diferentes valores em `position.set(x, y, z)`. |
| 3 objetos com rotação | Mais de 3 objetos usam `rotation`. |
| 3 objetos com escala | Mais de 3 objetos usam `scale`. |
| Câmera adequada | A `PerspectiveCamera` está em `(9, 7, 12)` e aponta para o centro da composição. |
| Scene, Camera e Renderer | O código cria `THREE.Scene`, `THREE.PerspectiveCamera` e `THREE.WebGLRenderer`. |
| Geometry, Material e Mesh | Cada elemento visual combina uma geometria, um material e um `THREE.Mesh`. |
| `scene.add()` | Todos os objetos e auxiliares são adicionados explicitamente à cena. |
| `position`, `rotation` e `scale` | As três transformações aparecem de forma explícita no código. |
| Funcionamento no navegador | O projeto usa Three.js por CDN e pode ser aberto com um servidor local. |
| Sem animação | Não há `requestAnimationFrame`, relógio ou laço de animação. |

## Estrutura do projeto

```text
projeto-threejs/
├── index.html
└── README.md
```

O JavaScript e o CSS permanecem dentro do arquivo `index.html`, deixando a entrega simples e compatível com a estrutura mínima solicitada.

## Como executar

Como o Three.js é carregado como módulo, abra o projeto por meio de um servidor local. Duas opções simples são:

1. Abrir a pasta no Visual Studio Code e utilizar a extensão **Live Server** no arquivo `index.html`.
2. Com Python instalado, executar `python -m http.server 8000` dentro da pasta e acessar `http://localhost:8000`.

É necessário estar conectado à internet para carregar o Three.js pelo CDN.

## Roteiro curto para apresentação

1. **Cena:** “Criamos uma mini cidade 3D estática usando Three.js.”
2. **Estrutura:** mostrar a criação de `Scene`, `PerspectiveCamera` e `WebGLRenderer`.
3. **Objetos:** explicar que cada objeto combina `Geometry`, `Material` e `Mesh`.
4. **Geometrias:** apontar caixa, esfera, cilindro, cone e plano na composição.
5. **Transformações:** mostrar exemplos de `position`, `rotation` e `scale` no código.
6. **Resultado:** destacar que há 17 objetos, mais de 4 cores e nenhum laço de animação.
