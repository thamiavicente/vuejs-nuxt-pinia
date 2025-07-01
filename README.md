# Vuejs & Nuxt & Pinia

## Vuejs
Ciclo de vida (mounted, created, beforeUnmount).

Reatividade (ref, reactive).

Computed vs Watch.

Slots, Props, Emits.

Diretivas (v-if, v-for, v-show, v-model).

Componentes globais vs locais.

Vue Router: rotas dinâmicas, lazy loading.

Vuex ou Pinia: estado global, actions, mutations, getters.

Hooks do Composition API (onMounted, watchEffect, computed).

Boas práticas para performance (Lazy load de componentes, evitar watchers desnecessários).

Options API x Composition API

| Aspecto | Options API | Composition API |
|-|-|-|
| Estrutura| Organiza por opções (data, methods, etc.)| Organiza por lógica dentro de setup() |
| Legibilidade| Fácil para iniciantes| Melhor em projetos grandes |
| Reutilização de lógica| Mixins (pouco claros)| Composables (claros e reutilizáveis) |
| TypeScript| Suporte mais limitado| Suporte mais completo |
| Código em componentes grandes| Pode ficar fragmentado| Agrupa lógica relacionada |
| Performance| Similar| Similar |

| Aspecto | `setup()` | `<script setup>` |
|-|-|-|
| Local | Dentro de export default {} | Top-level do componente |
| Retorno explícito | Precisa retornar tudo ao template | Automaticamente exposto ao template |
| Verboso | Mais verboso | Código mais limpo |
| Compatibilidade | Pode ser usado junto com Options API | Exclusivo Composition API |
| TypeScript | Funciona bem | Melhor DX com inferência automática |
| Uso recomendado | Para projetos que misturam Options API | Para novos projetos Vue 3 |

Composable x Components x Mixins

## Nuxt
Diferença SSR vs SSG vs SPA no Nuxt.

Estrutura de pastas (pages, components, layouts, store).

Arquivo nuxt.config:

Configuração de plugins, módulos, metas.

Middleware de autenticação.

Utilização de asyncData e fetch para pré-carregar dados.

Roteamento automático via pages.

Geração de sites estáticos (nuxt generate).

Como o Nuxt melhora Core Web Vitals:

SSR reduz LCP.

Split de código automático.

Prefetch de links automáticos.