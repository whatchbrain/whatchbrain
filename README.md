⌚ WatchBrain
Tu cerebro para la relojería independiente.
Pegas una URL. La IA investiga, clasifica y enriquece. Tú descubres.
https://openai.com
https://nextjs.org
https://supabase.com
La visión
Descubrir una marca de relojes independiente debería ser tan fácil como compartir un link.
Pegas una URL de Horology Planet, una review o la web de un microbrand. La IA investiga automáticamente: país, fundador, movimiento, rango de precio, complicaciones, distribución. Cada dato lleva un confidence score — porque la IA nunca debería fingir que todo es igual de fiable.
Con el tiempo, WatchBrain aprende qué te gusta. Independientes chinos con tourbillon < $2.000? Microbrands suizas GMT sin distribuidor en España? Te encuentra lo que ni sabías que buscabas.
No es un bookmark manager. Es un cerebro que piensa en relojes por ti.
Cómo funciona
plain
Tú:    https://horologyplanet.com/gearmagus-ms10

IA:    GEARMAGUS
       🇨🇳 China | Independent
       Precio: $1.499 – $2.999
       Movimiento: mecánico, ST8230
       Complicación: tourbillon 3D
       Confidence: 94%

       Match contigo: 91/100
       → independiente | complicación rara | precio contenido
Stack
Hojas
Capa	Tecnología	Por qué
Frontend	Next.js 15 + TypeScript + Tailwind + shadcn/ui	App Router, DX excepcional
Backend	Next.js API Routes + Edge Runtime	Sin servidor separado
Base de datos	Supabase (PostgreSQL + pgvector)	Auth nativo, vector search
IA	OpenAI GPT-4o + Embeddings	Extracción estructurada
Scraping	cheerio + Firecrawl fallback	Robusto, con fallback
Bot	Telegram (grammy.js)	Más barato y rápido que WhatsApp
Deploy	Vercel	Zero-config, edge global
Filosofía: Vibe Coding
No escribo código línea a línea. Pienso en problemas humanos, diseño soluciones, y orquesto IA para construirlas.
"El trabajo de programador no va a desaparecer. Lo que no puede desaparecer es el pensamiento de programador: la capacidad de identificar una necesidad humana real y orquestar herramientas para resolverla."
Este repo es mi currículum vivo. Documento cada decisión de arquitectura, cada prompt que evoluciona, cada trade-off técnico. No construyo en silencio. Construyo en público.
Arquitectura
plain
Telegram Bot → /api/analyze → OpenAI GPT-4o + Web Search
                              ↓
                         cheerio scraper
                              ↓
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
          brands         watches         sources
              └───────────────┴───────────────┘
                              │
                         Supabase PostgreSQL
Progreso
Hojas
Fase	Estado	Qué incluye
0 — Arquitectura	🟡 En curso	Schema SQL, setup repo, env vars
1 — Backend Core	⚪ Pendiente	/api/analyze, scraper, prompt agente
2 — Web MVP	⚪ Pendiente	Auth, Discover, Add Watch, fichas
3 — Bot Telegram	⚪ Pendiente	Webhook, comandos, respuestas
4 — Inteligencia IA	⚪ Pendiente	Match score, radar, Brand Graph
5 — Escala	⚪ Pendiente	WhatsApp, extensión Chrome, API
Documentación del proceso
./docs/prompts/ — Historial completo de prompts
./docs/decisions/ — Architecture Decision Records
./docs/retro/ — Retrospectivas mensuales
./PROCESS.md — Diario vivo del proyecto
Demo
🚧 En construcción. La demo pública estará disponible en la Fase 2.
Mientras tanto, sigue el proceso en tiempo real:
🧵 Hilos de construcción en X
🎥 Demos semanales en YouTube
📝 Retros mensuales en el blog
Por qué relojes
La relojería independiente es el nicho perfecto:
Datos dispersos — información en foros, blogs, tiendas, sin estandarizar
Comunidad apasionada — gente que valora el descubrimiento
Atributos complejos — movimientos, complicaciones, manufactura, historia
Descubrimiento difícil — las mejores marcas no tienen marketing industrial
Si funciona aquí, funciona en cualquier nicho de pasión.
Contribuir
Este es un proyecto de aprendizaje tutorizado con IA. No busco contribuciones de código (aún), pero sí:
🐛 Bug reports cuando la demo esté lista
💡 Ideas de marcas/relojes para testear
🔗 URLs interesantes para enriquecer la base de datos
Licencia
MIT — porque el conocimiento compartido crece. Pero el proceso documentado es lo que realmente tiene valor.
Construido con ☕, curiosidad y una IA que nunca duerme.
Ver commits recientes
