# Vuejs & Nuxt & Pinia

## Quizzes
### [W3 School](https://www.w3schools.com/vue/vue_quiz.php)

## Vuejs
- Vue utiliza programação declarativa, ou seja, é descrito cenários e o componente reage "reativamente" ao descrito. Exemplo: Quando `logged` for falso, exiba o texto `notLogged` e quando atualizar para verdadeiro, exiba `isLogged`.
Diferente da programação imperativa, que é preciso mandar uma ação ser executada. Exemplo: Quando o botão `logged` é clicado, a mensagem `userLogged` é atualizada. Não é possível atualizar a mensagem sem que o usuário execute uma ação.
- É um framework progressivo, já que cresce conforme sua demanda
- É baseado, principalmente, em SFC (single-file component), que é o conceito de isolar os componentes em arquivos únicos, contendo a lógica do componente, o seu HTML e seu estilo.

### Maneiras que o Vue pode ser usado
| Conceito | O que é | Quando usar |
|-|-|-|
| Enhancing static HTML w/o build | Usar JS via CDN para interatividade sem build | Sites simples, protótipos rápidos |
| Embedding as Web Components | Criar elementos HTML customizáveis reutilizáveis | Componentes isolados em vários sites |
| SPA | Navegação dinâmica sem reload, 1 página HTML | Apps interativos, dashboards |
| SSR | Renderização do HTML no servidor | SEO, performance, conteúdo dinâmico |
| Jamstack / SSG | Gerar site estático no build | Blogs, portfólios, docs |

### props x ref
Para lidar com a dinamicidade do componente, assim como fazer o bind de suas propriedades, o componente pode utilizar dessas duas estratégias:
| Aspecto | defineProps() | ref() |
|-|-|-|
| O que é? | Mecanismo para receber dados do componente pai | Cria uma variável reativa interna |
| Origem do valor | Vem do pai (via props) | Definido dentro do componente |
| Reatividade | Reativo, mas controlado pelo pai | Reativo, controlado pelo próprio componente |
| Mutabilidade | O componente filho não deve alterar o valor recebido | O componente pode alterar livremente o valor |

### ref x reactive
| Aspecto | ref | reactive |
|-|-|-|
| Uso | valores simples ou refs únicos | objetos/arrays |
| Acesso | .value | direto |
| Reatividade | rastro por .value | rastro por propriedade |

### Ciclo de vida
O Vue conta com os seguintes ciclos de vida:
- beforeCreated
- created
- ---------> Antes do template ser compilado
- beforeMount
- mounted
- ---------> Template foi adicionado na DOM
- beforeUpdate
- updated
- ---------> Os dados do componente foram alterados
- beforeUnmount
- unmounted
- ---------> O componente foi extinto

[Referência](https://vuejs.org/guide/essentials/lifecycle.html)

### Computed x Watch
| Aspecto | computed | watch |
|-|-|-|
| Retorna valor? | sim, valor derivado reativo | não |
| Uso | valores derivados | efeitos colaterais |
| Cacheado? | sim | não |
| Executa quando? | ao acessar e dependências mudarem | sempre que dependências mudam |

### Slots, Props, Emits.

### Diretivas e Diretivas customizadas

### Componentes globais vs locais.

### Vue Router

### Vuex ou Pinia

### Options API x Composition API
| Aspecto | Options API | Composition API |
|-|-|-|
| Estrutura| Organiza por opções (data, methods, etc.)| Organiza por lógica dentro de setup() |
| Legibilidade| Fácil para iniciantes| Melhor em projetos grandes |
| Reutilização de lógica| Mixins (pouco claros)| Composables (claros e reutilizáveis) |
| TypeScript| Suporte mais limitado| Suporte mais completo |
| Código em componentes grandes| Pode ficar fragmentado| Agrupa lógica relacionada |
| Performance| Similar| Similar |

#### setup x script setup
| Aspecto | `setup()` | `<script setup>` |
|-|-|-|
| Local | Dentro de export default {} | Top-level do componente |
| Retorno explícito | Precisa retornar tudo ao template | Automaticamente exposto ao template |
| Verboso | Mais verboso | Código mais limpo |
| Compatibilidade | Pode ser usado junto com Options API | Exclusivo Composition API |
| TypeScript | Funciona bem | Melhor DX com inferência automática |
| Uso recomendado | Para projetos que misturam Options API | Para novos projetos Vue 3 |

### Composable x Components x Mixins

## Nuxt
### Arquivo nuxt.config:

### Configuração de plugins, módulos, metas.

### Middleware de autenticação.

### Utilização de asyncData e fetch para pré-carregar dados.

### Roteamento

## SEO

### Core Web Vitals
São métricas de performance focadas em UX, como:
- LCP (Largest Contentful Paint): mede o tempo de carregamento do maior elemento visível (ideal: <= 2,5s)
- FID (First Input Delay): tempo de resposta à primeira interação do usuário (ideal: <= 100ms)
- CLS (Cumulative Layout Shift): estabilidade visual durante carregamento (ideal: <= 0.1)

### Técnicas de otimização
- Lazy loading (loading="lazy", import() dinâmico)
- Otimização de imagens (formatos WebP/AVIF, dimensionamento correto)
- Uso de Critical CSS e evitar grandes CSS bloqueantes
- Minimizar JS e dividir em chunks (webpack, vite)
- Evitar layout shift usando tamanho fixo para imagens e iframes
- Utilização de server-side rendering (SSR) e static site generation (SSG) para melhorar LCP.

<!-- JavaScript
Revise:
ES6+:
Arrow functions, spread/rest, destructuring.
Promises, async/await.
Classes e modules.
Event Loop e Call Stack (como JS gerencia tarefas assíncronas).
Manipulação de DOM.
Debounce e throttle (para performance em scroll/input).
Diferenciar null, undefined, NaN.

TypeScript
Você deve:
Entender tipagens básicas: string, number, boolean, any, unknown, void, never.
Diferença entre interface e type.
Union Types (string | number).
Generic types (<T>).
Inferência e type narrowing.
Usar enums e tuples.
Configuração básica do tsconfig.json -->